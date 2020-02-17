# Comments

## blockCommentStart() / blockCommentEnd()

Considering Java as the current language context the following template

```java
$start$
$end$
```

will produce the following block comment:

```java
/*
*/
```

If there are empty lines between these two template variables

```java
$start$


$end$
```

then it will result in the following block comment:

```java
/*


*/
```

**Related macro:**
- ?

**Example built-in templates:**
- ?
