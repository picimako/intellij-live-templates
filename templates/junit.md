# JUnit

## @Test annotated method

The first template is a more generic one in which the whole method name can be customized at hand.
In my experience this works better with the keyword *test*.

```java
@org.junit.Test
public void $methodName$() {
    $code$
}
```

The other template populates the word *should* at the beginning of the test method, which could be something like
*shouldValidateJsonString*. The keyword *should* works better with the option because this way you can type the method name in
a more fluent way.

```java
@org.junit.Test
public void should$doSomething$() {
    $code$
}
```

### General configuration
- Abbreviation: *should*, *test*
- Scope: Java - declaration
- Other options enabled:
    - Reformat according to style
    - Use static import if possible
    - Shorten FQ names

## @Before and @BeforeClass annotated methods

```java
@org.junit.Before
public void before() {
    $code$
}
```

```java
@org.junit.BeforeClass
public void beforeClass() {
    $code$
}
```

### General configuration
- Abbreviation: *before*, *beforeClass*, *setup*
- Scope: Java - declaration
- Other options enabled:
    - Reformat according to style
    - Use static import if possible
    - Shorten FQ names

## @After and @AfterClass annotated methods

```java
@org.junit.After
public void after() {
    $code$
}
```

```java
@org.junit.AfterClass
public void afterClass() {
    $code$
}
```

### General configuration
- Abbreviation: *after*, *afterClass*, *teardown*
- Scope: Java - declaration
- Other options enabled:
    - Reformat according to style
    - Use static import if possible
    - Shorten FQ names

## Parameters method

```java
@org.junit.runners.Parameterized.Parameters
public static Iterable<Object[]> parameters() {
    return java.util.Arrays.asList(new Object[][]{
        {$parameter1$},
        {$parameter2$}
    });
}
```

### General configuration
- Abbreviation: *parameters*
- Scope: Java - declaration
- Other options enabled:
    - Reformat according to style
    - Shorten FQ names
0