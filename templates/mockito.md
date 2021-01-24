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
