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

# Selenium

## WebElement with @FindBy

```java
@org.openqa.selenium.support.FindBy($str$ = "$SELECTOR$")
public org.openqa.selenium.WebElement $ELEMENT_NAME$;
```

| Config | Config value |
|---|---|
| General | Abbreviation: *webelement*<br>Options enabled: Reformat according to style, Shorten FQ names |
| <pre>$str$</pre> | Expression: `enum("css", "id", "className")`<br>Default value: `"css"` |
|  | $str$ includes only the most used locator strategies.<br>You can also use `completeSmart()` if you'd like to have all available methods suggested. |

## List with @FindBy

```java
@org.openqa.selenium.support.FindBy($str$ = "$SELECTOR$")
public java.util.List<org.openqa.selenium.WebElement> $ELEMENT_LIST_NAME$;
```

| Config | Config value |
|---|---|
| General | Abbreviation: *webelementlist*<br>Options enabled: Reformat according to style, Shorten FQ names |
| <pre>$str$</pre> | Expression: `enum("css", "id", "className")`<br>Default value: `"css"` |
|  | $str$ includes only the most used locator strategies.<br>You can also use `completeSmart()` if you'd like to have all available methods suggested. |  

## By.cssSelector/id/className()

```java
final org.openqa.selenium.By $by$ = By.$strategy$("$selector$");
```

| Config | Config value |
|---|---|
| General | Abbreviation: *by*, *bycss*<br>Scope: Java declaration<br>Options enabled: Shorten FQ names |
| <pre>$strategy$</pre> | Expression: `enum("cssSelector", "id", "className")`<br>Default value: `"cssSelector"` |
|  | `$strategy$` includes only the most used locator strategies.<br>You can also use `completeSmart()` if you'd like to have all available methods suggested. |
