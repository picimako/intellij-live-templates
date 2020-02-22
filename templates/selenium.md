# Selenium

## WebElement with @FindBy

```java
@org.openqa.selenium.support.FindBy(css = "$SELECTOR$")
public org.openqa.selenium.WebElement $ELEMENT_NAME$;
```

### General configuration
- Abbreviation: *webelement*
- Options enabled: Reformat according to style, Shorten FQ names

## List with @FindBy

```java
@org.openqa.selenium.support.FindBy(css = "$SELECTOR$")
public java.util.List<org.openqa.selenium.WebElement> $ELEMENT_LIST_NAME$;
```

### General configuration
- Abbreviation: *webelementlist*
- Options enabled: Reformat according to style, Shorten FQ names

## By.cssSelector()

```java
final org.openqa.selenium.By $by$ = By.cssSelector("$selector$");
```

As additional ones can also create templates for other locator strategies like `By.id()` and `By.className()` as well.

### General configuration
- Abbreviation: *by*, *bycss*
- Scope: Java declaration
- Options enabled: Shorten FQ names
