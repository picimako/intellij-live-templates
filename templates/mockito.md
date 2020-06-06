# Mockito

## @Mock and @Spy fields

```java
@org.mockito.Mock
private $TargetType$ $fieldName$;
```

```java
@org.mockito.Spy
private $TargetType$ $fieldName$;
```

| Config | Config value |
|---|---|
| General - mock | Abbreviation: *mock*<br>Options enabled: Reformat according to style, Shorten FQ names |
| General - spy| Abbreviation: *spy*<br>Options enabled: Reformat according to style, Shorten FQ names |

## @Captor field

```java
@org.mockito.Captor
private org.mockito.ArgumentCaptor<$CaptorType$> $fieldName$;
```

| Config | Config value |
|---|---|
| General | Abbreviation: *Captor*<br>Options enabled: Reformat according to style, Shorten FQ names |
