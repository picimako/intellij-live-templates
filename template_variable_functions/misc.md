# Misc

## clipboard()

Just like what you'd expect, quoting the official documentation it *"Returns the contents of the system clipboard."*

**Related macro:** [ClipboardMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/ClipboardMacro.java)

## complete()

Invokes code completion at the position of the variable.

**Related macro:** [CompleteMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CompleteMacro.java)

## completeSmart()

Invokes smart type completion at the position of the variable.

**Related macro:** [CompleteSmartMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CompleteSmartMacro.java)

## date(sDate)

Returns the current system date in the specified format.

**Related macro:** [CurrentDateMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CurrentDateMacro.java)

## groovyScript("groovy code", arg1)

Returns a Groovy script with the specified code.

**Related macro:** [GroovyScriptMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/GroovyScriptMacro.java)

## lineNumber()

Returns the line number at which the associated template parameter is positioned after invoking the live template.

Considering that the live template is invoked in the 11th line, the results would be the following:

| Template | Result  |
|---|---|
| <pre>lineNumber$</pre> | 11 |
| <pre>$start$<br><br><br>$lineNumber$</pre> | 14 |

**Related macro:** [LineNumberMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/LineNumberMacro.java)

## showParameterInfo

NOTE: This is not included in the official documentation at the moment.

**Related macro:** [ShowParameterInfoMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/ShowParameterInfoMacro.java)

## suggestFirstVariableName(sFirstVariableName)

Doesn't suggest true, false, this, super.

**Related macro:** [SuggestFirstVariableNameMacro](https://github.com/JetBrains/intellij-community/blob/master/java/java-impl/src/com/intellij/codeInsight/template/macro/SuggestFirstVariableNameMacro.java)

## suggestIndexName()

Suggests the name of an index variable from most commonly used ones: i, j, k, and so on (first one that is not used in the current scope).

**Related macro:** [SuggestIndexNameMacro](https://github.com/JetBrains/intellij-community/blob/master/java/java-impl/src/com/intellij/codeInsight/template/macro/SuggestIndexNameMacro.java)

## suggestVariableName()

Suggests the name for a variable based on the variable type and its initializer expression...

**Related macro:** [SuggestVariableNameMacro](https://github.com/JetBrains/intellij-community/blob/master/java/java-impl/src/com/intellij/codeInsight/template/macro/SuggestVariableNameMacro.java)

## time(sSystemTime)

Returns the current system time in the specified format.

TODO: Check without parameter as well.

**Related macro:** [CurrentTimeMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CurrentTimeMacro.java)

## user()

Returns the name of the current user.

**Related macro:** [CurrentUserMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CurrentUserMacro.java)