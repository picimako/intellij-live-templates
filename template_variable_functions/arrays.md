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

# Arrays

## arrayVariable()

Suggests all array variables applicable in the current scope.

There are examples for this in the iterations group of the Live Templates. The example below is for the template called `itar` whose purpose is to **Iterate elements of array**:

```java
for(int $INDEX$ = 0; $INDEX$ < $ARRAY$.length; $INDEX$++) {
  $ELEMENT_TYPE$ $VAR$ = $ARRAY$[$INDEX$];
  $END$
}
```

Its `$ARRAY$` variable is configured to use this (`arrayVariable()`) macro.

Given that there is at least one array in the current scope, e.g.:

```java
public void thisIsAMethod(int[] intArray, String[] stringArray) {
}
```

using the keyword `itar` will work the following, suggesting all array variables at the first occurrence of the appropriate template variable:

![arrayVariable_itar](images/arrayVariable.gif)

By default it inserts the code snippet using the first array in the scope but along the way it can be changed easily from the suggestions list.

In case there is no array variable in the current scope, then the `$ARRAY$` variable is populated with the default name `array` and one has to create it manually.

![arrayVariable_itar](images/arrayVariable_no_array_in_scope.gif)

**Related macro:** [ArrayVariableMacro](https://github.com/JetBrains/intellij-community/blob/master/java/java-impl/src/com/intellij/codeInsight/template/macro/ArrayVariableMacro.java)

## componentTypeOf(<array>)

Returns component type of an array.

The example below is for the template called `itar` whose purpose is to **Iterate elements of array**:

```java
for(int $INDEX$ = 0; $INDEX$ < $ARRAY$.length; $INDEX$++) {
  $ELEMENT_TYPE$ $VAR$ = $ARRAY$[$INDEX$];
  $END$
}
```

Its `$ELEMENT_TYPE$` variable is configured to use this (`componentTypeOf()`) macro: `componentTypeOf(ARRAY)` which also shows how one can reference a template variable in a live template function.
This one references the $ARRAY$ variable.

Given that there is at least one array in the current scope, e.g.:

```java
public void thisIsAMethod(int[] intArray, String[] stringArray) {
}
```

using the keyword `itar` will work the following, automatically populating the `$ELEMENT_TYPE$` variable with the type that the selected array can store:

Although the inserted snippet uses the first available array and array type, upon selecting another array for the `$ARRAY$` variable, `$ELEMENT_TYPE$` also changes automatically. 

![component_type_of_itar](images/componentTypeOf.gif)

**Related macro:** [ComponentTypeOfMacro](https://github.com/JetBrains/intellij-community/blob/master/java/java-impl/src/com/intellij/codeInsight/template/macro/ComponentTypeOfMacro.java)

## iterableComponentType(<ArrayOrIterable>)

Returns the type of an iterable component, such as an array or a collection.

The example below is for the template called `iter` whose purpose is to **Iterate Iterable | Array**:

```java
for ($ELEMENT_TYPE$ $VAR$ : $ITERABLE_TYPE$) {
  $END$
}
```

Its `$ELEMENT_TYPE$` variable is configured to use this (`iterableComponentType()`) macro: `iterableComponentType(ITERABLE_TYPE)`.

Given that there is at least one iterable in the current scope, e.g.:

```java
public void thisIsAMethod(List<String> strings, int[] integers) {
}
```

using the keyword `iter` will work the following, automatically populating the `$ELEMENT_TYPE$` variable with the type that the selected iterable can store:

![iterable_component_type_iter](images/iterableComponentType.gif)

**Related macro:** [IterableComponentTypeMacro](https://github.com/JetBrains/intellij-community/blob/master/java/java-impl/src/com/intellij/codeInsight/template/macro/IterableComponentTypeMacro.java)

## iterableVariable()
	
Returns the name of a variable that can be iterated.

The example below is for the template called `iter` whose purpose is to **Iterate Iterable | Array**:

```java
for ($ELEMENT_TYPE$ $VAR$ : $ITERABLE_TYPE$) {
  $END$
}
```

Its `$ITERABLE_TYPE$` variable is configured to use this (`iterableVariable()`).

Given that there is at least one iterable in the current scope, e.g.:

```java
public void thisIsAMethod(List<String> strings, int[] integers) {
}
```

using the keyword `iter` will work the following, suggesting all iterable variables:

![iterable_variable_iter](images/iterableVariable.gif)

In case there is no iterable variable in the current scope, then the `$ITERABLE_TYPE$` variable is not populated by default, one has to do it manually.

![iterable_variable_no_iterable_iter](images/iterableVariable_no_iterable_in_scope.gif)

**Related macro:** [IterableVariableMacro](https://github.com/JetBrains/intellij-community/blob/master/java/java-impl/src/com/intellij/codeInsight/template/macro/IterableVariableMacro.java)
