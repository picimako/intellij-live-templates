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

# Comments

## blockCommentStart() / blockCommentEnd()

| Language | Template | Result |
|---|---|---|
| Java | <pre>$start$<br>$end$</pre> | <pre>/\*<br>*/</pre> |
| Java | <pre>$start$<br><br><br>$end$</pre> | <pre>/\*<br><br><br>*/</pre> |
| XML | <pre>$start$<br>$end$</pre> | <pre>\<!--<br>--></pre> |

**Related macros:** [CommentMacro.BlockCommentStart / CommentMacro.BlockCommentEnd](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CommentMacro.java)

## commentStart() / commentEnd()

| Language | Template | Result |
|---|---|---|
| Java | <pre>$start$<br>$end$</pre> | <pre>//<br></pre> |
| XML | <pre>$start$<br>$end$</pre> | <pre>\<!--<br>--></pre> |

Since there is no line comment end indicator in Java, the `commendEnd()` function returns an empty string.

**Related macros:** [CommentMacro.AnyCommentStart / CommentMacro.AnyCommentEnd](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CommentMacro.java)

## lineCommentStart()

| Language | Template | Result |
|---|---|---|
| Java | <pre>$start$</pre> | <pre>//<br></pre> |
| XML | <pre>$start$</pre> | <pre></pre> |

In case of XML the function returns an empty string since there are no line comments in XML.

**Related macros:** [CommentMacro.LineCommentStart](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/CommentMacro.java)
