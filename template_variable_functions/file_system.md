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
