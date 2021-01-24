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

# FluentLenium

## FluentWebElement field with @FindBy
    
```java
@org.openqa.selenium.support.FindBy($str$ = "$SELECTOR$")
public org.fluentlenium.core.domain.FluentWebElement $ELEMENT_NAME$;
```

| Config | Config value |
|---|---|
| General | Abbreviation: *fluentwebelement*<br>Options enabled: Reformat according to style, Shorten FQ names |
| <pre>$str$</pre> | Expression: `enum("css", "id", "className")` - Includes only the most used locator strategies.<br>Default value: `"css"` |

## FluentList field with @FindBy

```java
@org.openqa.selenium.support.FindBy($str$ = "$SELECTOR$")
public org.fluentlenium.core.domain.FluentList<org.fluentlenium.core.domain.FluentWebElement> $ELEMENT_LIST_NAME$;
```

| Config | Config value |
|---|---|
| General | Abbreviation: *fluentlist*<br>Options enabled: Reformat according to style, Shorten FQ names |
| <pre>$str$</pre> | Expression: `enum("css", "id", "className")` - Includes only the most used locator strategies.<br>Default value: `"css"` |

## Await at most

```java
await().atMost($time$, java.util.concurrent.TimeUnit.$timeunit$).until($element$).$condition$;
```

| Config | Config value |
|---|---|
| General | Abbreviation: *atmost*<br>Scope: Java - Statement<br>Options enabled: Reformat according to style, Shorten FQ names |
| <pre>$timeunit$</pre> | Expression: `completeSmart()`<br>Default value: `"SECONDS"` |
