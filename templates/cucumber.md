# Cucumber

## Given (When, Then, And, But) step definitions

```java
@io.cucumber.java.en.Given("$step_pattern$")
public void $method_name$() {
    $code$
}
```

### Variables configuration

**$step_pattern$**

```java
regularExpression(
    regularExpression(
        regularExpression(
            regularExpression(clipboard(), "\"", "#"),
             "#(?:[^#])*#", "{string}"),
               "\\d+", "{int}"),
                "[A-Z_]{2,}", "{}")
```

Given that a step description is copied to the clipboard from a Gherkin file, this script replaces some parts of it to generate a step definition pattern with as a valid Cucumber expression:
1. Replaces each " character to a # in the value from the clipboard. (This makes it easier to replace quoted String values and create a {string} placeholder from that, instead of doing black magic with escaped quotes.)
2. Replaces the parts of the step enclosed by # characters to the value {string}
3. Replaces integers to the value {int}
4. Replaces any, at least 2-character long, all uppercase char sequences to the value {}. Such values are considered as an enum entry name.

**$method_name$**

```java
snakeCase(
    regularExpression(
        regularExpression(
            regularExpression(
                regularExpression(clipboard(), "\"", "#"),
                 "#(?:[^#])*#", "X"),
                  "\\d+", "X"), 
                  "[A-Z_]{2,}", "X"))
```

Given that a step description is copied to the clipboard from a Gherkin file, this script replaces some parts of it to generate a step definition method name having replaced placeholders with lowercase x-es:
1. Replaces each " character to a # in the value from the clipboard. (This makes it easier to replace quoted String values instead of doing black magic with escaped quotes.)
2. Replaces the parts of the step enclosed by # characters to an lowercase x.
3. Replaces integers to an lowercase x.
4. Replaces any, at least 2-character long, all uppercase char sequences to an lowercase x.
5. Converts the value at this point to a snake case format.

### General configuration
- Abbreviation: *given*
- Scope: Java
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
