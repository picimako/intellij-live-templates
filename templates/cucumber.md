<!--
Copyright 2021 Tamás Balog

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

# Cucumber

## Given (When, Then, And, But) step definitions

```java
@io.cucumber.java.en.Given("$step_pattern$")
public void $method_name$($params$) {
    $END$
}
```

### Variables configuration

**$step_pattern$**

```
regularExpression(
    regularExpression(
        regularExpression(
            regularExpression(
                regularExpression(clipboard(), "\"", "#"),
                    "#(?:[^#])*#", "{string}"),
                    "-?\\d*\\.\\d+", "{float}"),
                    "\\d+", "{int}"),
                    "[A-Z_]{2,}", "{}")
```

Given that a step description is copied to the clipboard from a Gherkin file, this script replaces some parts of it to generate a step definition pattern with as a valid Cucumber expression:
1. Replaces each " character to a # in the value from the clipboard. (This makes it easier to replace quoted String values and create a {string} placeholder from that, instead of doing black magic with escaped quotes.)
2. Replaces the parts of the step enclosed by # characters to the value {string}
3. Replaces floating points numbers to the value {float}
4. Replaces integers to the value {int}
5. Replaces any, at least 2-character long, all uppercase char sequences to the value {}. Such values are considered as an enum entry name.

**$method_name$**

```
snakeCase(
	regularExpression(
	    regularExpression(
	        regularExpression(
	            regularExpression(
	                regularExpression(clipboard(), "\"", "#"),
	                 "#(?:[^#])*#", "x"),
	                  "\\d+", "x"),
	                  "-?\\d*\.\\d+", "x"), 
	                  "[A-Z_]{2,}", "x"))
```

Given that a step description is copied to the clipboard from a Gherkin file, this script replaces some parts of it to generate a step definition method name having replaced placeholders with lowercase x-es:
1. Replaces each " character to a # in the value from the clipboard. (This makes it easier to replace quoted String values instead of doing black magic with escaped quotes.)
2. Replaces the parts of the step enclosed by # characters to an lowercase x.
3. Replaces floating point numbers to a lowercase x.
4. Replaces integers to a lowercase x.
5. Replaces any, at least 2-character long, all uppercase char sequences to an lowercase x.
6. Converts the value at this point to a snake case format.

### General configuration
- Abbreviation: *given*
- Options enabled: Shorten FQ names

### Example
A step

`Given the EDITOR user tries to edit the content named "Homepage" 2 times`

becomes

```java
@Given("the {} user tries to edit the content named {string} {int} times")
public void the_x_user_tries_to_edit_the_content_named_x_x_times() {

}
```

### Notes
Method arguments generation is not yet implemented, that requires more effort to figure out how that would work.

## Given (When, Then, And, But) Java8 step definitions

```java
Given("$step_pattern$", () -> {$step_definition$});
```

### Variables configuration

**$step_pattern$**

```
regularExpression(
    regularExpression(
        regularExpression(
            regularExpression(
                regularExpression(clipboard(), "\"", "#"),
                    "#(?:[^#])*#", "{string}"),
                    "-?\\d*\\.\\d+", "{float}"),
                    "\\d+", "{int}"),
                    "[A-Z_]{2,}", "{}")
```

Given that a step description is copied to the clipboard from a Gherkin file, this script replaces some parts of it to generate a step definition pattern with as a valid Cucumber expression:
1. Replaces each " character to a # in the value from the clipboard. (This makes it easier to replace quoted String values and create a {string} placeholder from that, instead of doing black magic with escaped quotes.)
2. Replaces the parts of the step enclosed by # characters to the value {string}
3. Replaces floating points numbers to the value {float}
4. Replaces integers to the value {int}
5. Replaces any, at least 2-character long, all uppercase char sequences to the value {}. Such values are considered as an enum entry name.

### General configuration
- Abbreviation: *given*
- Options enabled: Reformat according to style, Shorten FQ names

### Example
A step

`Given the EDITOR user tries to edit the content named "Homepage" 2 times`

becomes (within a class constructor)

```java
Given("the {} user tries to edit the content named {string} {int} times", () -> {});
```

## Tagged Hooks

All of the following templates assume that a Scenario parameter is needed.

| Annotation | Template |
|---|---|
| <pre>@Before</pre> | <pre>@io.cucumber.java.Before("$tags$")<br>public void beforeScenario(io.cucumber.core.api.Scenario scenario) {<br>    $code$<br>}</pre> |
| <pre>@BeforeStep</pre> | <pre>@io.cucumber.java.BeforeStep("$tags$")<br>public void beforeStep(io.cucumber.core.api.Scenario scenario) {<br>    $code$<br>}</pre> |
| <pre>@After</pre> | <pre>@io.cucumber.java.After("$tags$")<br>public void afterScenario(io.cucumber.core.api.Scenario scenario) {<br>    $code$<br>}</pre> |
| <pre>@AfterStep</pre> | <pre>@io.cucumber.java.AfterStep("$tags$")<br>public void afterStep(io.cucumber.core.api.Scenario scenario) {<br>    $code$<br>}</pre> |

### General configuration
- Abbreviation: *before*, *beforestep*, *after*, *afterstep*
- Options enabled: Reformat according to style, Use static import if possible, Shorten FQ names
