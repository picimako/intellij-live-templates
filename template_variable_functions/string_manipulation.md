# String manipulation functions

## camelCase(String)

Converts a string into camelCase.

| Function call | Output |
|---|---|
| camelCase("my-text-file") | myTextFile |
| camelCase("my text file") | myTextFile |
| camelCase("my_text_file") | myTextFile |

**Related macro:** [ConvertToCamelCaseMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/ConvertToCamelCaseMacro.java)

## capitalize(String)
	
Capitalizes the first letter of the parameter.

| Function call | Output |
|---|---|
| capitalize("aJavaClass") | AJavaClass |
| capitalize("AJavaClass") | AJavaClass |
| capitalize("10 more coffees please") | 10 more coffees please |

**Related macro:** [CapitalizeMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CapitalizeMacro.java)

## capitalizeAndUnderscore(String)

Capitalizes all the letters of a CamelCase name passed as the parameter, and inserts an underscore between the parts.

| Function calls | Output |
|---|---|
| capitalizeAndUnderscore("my-text-file") | MY_TEXT_FILE |
| capitalizeAndUnderscore("my text file") | MY_TEXT_FILE |
| capitalizeAndUnderscore("my_text_file") | MY_TEXT_FILE |

**Related macro:** [CapitalizeAndUnderscoreMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CapitalizeAndUnderscoreMacro.java)

## concat(expressions...)

Returns a concatenation of all the strings passed to the function as parameters.

| Function call | Output |
|---|---|
| concat() | [empty string] |
| concat("unicorns ", "are real") | unicorns are real |
| concat("unicorns ", 3, "are real", 6.0, false) | unicorns are real |

This function ignores number and boolean values, and concatenates only String values.

**Related macro:** [ConcatMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/ConcatMacro.java)

## decapitalize(sName)

Replaces the first letter of the parameter with the corresponding lowercase letter.

| Function call | Output |
|---|---|
| decapitalize("Unicorns") | unicorns |
| decapitalize("unicorns") | unicorns |

**Related macro:** [DecapitalizeMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/DecapitalizeMacro.java)

## escapeString(sEscapeString)

Escapes the string specified as the parameter.

| Function call | Output |
|---|---|
| escapeString("\b \t \n \f \r \\ Ű 漢") | b \t \n \f r \\ Ű 漢 |
| escapeString("\\b \\t \\n \\f \\r \\\\") | \\b \\t \\n \\f \\r \\\\ |

**Related macro:** [EscapeStringMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/EscapeStringMacro.java)
**Escaping logic:** [StringUtil](https://github.com/JetBrains/intellij-community/blob/master/platform/util/src/com/intellij/openapi/util/text/StringUtil.java)

## firstWord(sFirstWord)

Returns the first word of the string passed as the parameter.

| Function call | Output |
|---|---|
| firstWord("Unicorns") | Unicorns |
| firstWord("Unicorns are real") | Unicorns |

**Related macro:** [FirstWordMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/FirstWordMacro.java)

## lowercaseAndDash(String)

Converts a camelCase string into lower case and inserts n-dashes as separators.

| Function call | Output |
|---|---|
| lowercaseAndDash("UnicornsAreReal") | unicorns-are-real |
| lowercaseAndDash("unicornsAreReal") | unicorns-are-real |
| lowercaseAndDash("unicorns are real") | unicorns-are-real |
| lowercaseAndDash("unicorns_are_real") | unicorns-are-real |

**Related macro:** [SplitWordsMacro.LowercaseAndDash](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/SplitWordsMacro.java)

## regularExpression(String, Pattern, Replacement)

Find all occurrences of Pattern in a String and replace it with Replacement. You can specify the pattern as a regular expression to find everything that matches it in the string.

Based on Cucumber step descriptions:

| Function call | Output |
|---|---|
| regularExpression("I have 4 apples", "\\d+", "{int}") | I have {int} apples |

**Related macro:** [RegExMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/RegExMacro.java)

## snakeCase(String)

Converts a string into snake_case.

| Function call | Output |
|---|---|
| snakeCase("FezesAreCool") | fezes_are_cool |
| snakeCase("fezesAreCool") | fezes_are_cool |
| snakeCase("fezes are cool") | fezes_are_cool |
| snakeCase("fezes-are-cool") | fezes_are_cool |

**Related macro:** [SplitWordsMacro.SnakeCaseMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/SplitWordsMacro.java)

## spaceSeparated(String)

Converts a string into lowercase and inserts spaces as separators.

**NOTE:** contrary to the official documentation it doesn't convert the input value to lowercase.

| Function call | Output |
|---|---|
| spaceSeparated("FezesAreCool") | Fezes Are Cool |
| spaceSeparated("fezesAreCool") | fezes Are Cool |
| spaceSeparated("FEZES_ARE_COOL") | FEZES ARE COOL |
| spaceSeparated("fezes-are-cool") | fezes are cool |

**Related macro:** [SnakeCaseMacro.SpaceSeparated](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/SplitWordsMacro.java)

## spacesToUnderscores(sParameterWithSpaces)

Replaces spaces with underscores in the string passed as the parameter.

| Function call | Output |
|---|---|
| spacesToUnderscores("Fezes Are Cool") | Fezes_Are_Cool |
| spacesToUnderscores("fezesAreCool") | fezesAreCool |
| spacesToUnderscores("FEZES_ARE_COOL") | FEZES_ARE_COOL |
| spacesToUnderscores("fezes-are-cool") | fezes-are-cool |

**Related macro:** [ReplaceSpacesWithUnderscoresMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/ReplaceSpacesWithUnderscoresMacro.java)

## substringBefore(String,Delimiter)

Removes the extension after the specified delimiter and returns only the filename.
This is helpful for test file names (for example, `substringBefore($FileName$,".")` returns *component-test* in *component-test.js*).

| Function call | Output |
|---|---|
| substringBefore("AJavaClass.java", ".") | AJavaClass |
| substringBefore("list, of, items", ", ") | list |

**Related macro:** [SubstringBeforeMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/SubstringBeforeMacro.java)

## underscoresToCamelCase(String)

Replaces underscores with camelCase letters in the string passed as the parameter.

| Function call | Output |
|---|---|
| underscoresToCamelCase("Fezes Are Cool") | fezes are cool |
| underscoresToCamelCase("fezesAreCool") | fezesarecool |
| underscoresToCamelCase("FEZES_ARE_COOL") | fezesAreCool |
| underscoresToCamelCase("fezes-are-cool") | fezes-are-cool |

**Related macro:** [ConvertToCamelCaseMacro.ReplaceUnderscoresToCamelCaseMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/ConvertToCamelCaseMacro.java)

## underscoresToSpaces(sParameterWithUnderscores)

Replaces underscores with spaces in the string passed as the parameter.

| Function call | Output |
|---|---|
| underscoresToSpaces("Fezes Are Cool") | Fezes Are Cool |
| underscoresToSpaces("fezesAreCool") | fezesAreCool |
| underscoresToSpaces("FEZES_ARE_COOL") | FEZES ARE COOL |
| underscoresToSpaces("fezes-are-cool") | fezes-are-cool |

**Related macro:** [ReplaceUnderscoresWithSpacesMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/ReplaceUnderscoresWithSpacesMacro.java)
