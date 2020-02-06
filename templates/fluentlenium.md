# FluentLenium

## FluentWebElement field with @Findby
    
```java
@org.openqa.selenium.support.FindBy(css = "$SELECTOR$")
public org.fluentlenium.core.domain.FluentWebElement $ELEMENT_NAME$;
```

### General configuration
- Abbreviation: *fluentwebelement*
- Scope: Java
- Other options enabled:
    - Reformat according to style
    - Shorten FQ names

## FluentList field with @FindBy

```java
@org.openqa.selenium.support.FindBy(css = "$SELECTOR$")
public org.fluentlenium.core.domain.FluentList<org.fluentlenium.core.domain.FluentWebElement> $ELEMENT_LIST_NAME$;
```

### General configuration
- Abbreviation: *fluentlist*
- Scope: Java
- Other options enabled:
    - Reformat according to style
    - Shorten FQ names
