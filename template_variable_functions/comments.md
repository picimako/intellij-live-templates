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
