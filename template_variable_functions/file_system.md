# File system

## currentPackage()

Returns the current package name.

**Related macro:** [CurrentPackageMacro](https://github.com/JetBrains/intellij-community/blob/master/java/java-impl/src/com/intellij/codeInsight/template/macro/CurrentPackageMacro.java)

## fileName()

Returns the name of the current file with its extension.

**Related macro:** [FilePathMacroBase.FileNameMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/FilePathMacroBase.java)

## fileNameWithoutExtension()

Returns the name of the current file without its extension.

**Related macro:** [FilePathMacroBase.FileNameWithoutExtensionMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/FilePathMacroBase.java)

## filePath()
	
Returns the absolute path to the current file.

**Related macro:** [FilePathMacroBase.FilePathMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/FilePathMacroBase.java)

## fileRelativePath()

Returns the current file path relative to the current project. To check what the relative path is for a given file, right-click it and select Copy Reference, or pressCtrl+Shift+Alt+C.

**Related macro:** [FilePathMacroBase.FileRelativePathMacro](https://github.com/JetBrains/intellij-community/blob/master/platform/lang-impl/src/com/intellij/codeInsight/template/macro/FilePathMacroBase.java)
