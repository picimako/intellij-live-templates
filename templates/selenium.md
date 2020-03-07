# Selenium

## WebElement with @FindBy

```java
@org.openqa.selenium.support.FindBy($str$ = "$SELECTOR$")
public org.openqa.selenium.WebElement $ELEMENT_NAME$;
```

| Config | Config value |
|---|---|
| General | Abbreviation: *webelement*<br>Options enabled: Reformat according to style, Shorten FQ names |
| <pre>$str$</pre> | Expression: `enum("css", "id", "className")` - Includes only the most used locator strategies.<br>Default value: `"css"` |

## List with @FindBy

```java
@org.openqa.selenium.support.FindBy($str$ = "$SELECTOR$")
public java.util.List<org.openqa.selenium.WebElement> $ELEMENT_LIST_NAME$;
```

| Config | Config value |
|---|---|
| General | Abbreviation: *webelementlist*<br>Options enabled: Reformat according to style, Shorten FQ names |
| <pre>$str$</pre> | Expression: `enum("css", "id", "className")` - Includes only the most used locator strategies.<br>Default value: `"css"` |

## By.cssSelector/id/className()

```java
final org.openqa.selenium.By $by$ = By.$strategy$("$selector$");
```

| Config | Config value |
|---|---|
| General | Abbreviation: *by*, *bycss*<br>Scope: Java declaration<br>Options enabled: Shorten FQ names |
| <pre>$strategy$</pre> | Expression: `enum("cssSelector", "id", "className")` - Includes only the most used locator strategies.<br>Default value: `"cssSelector"` |
