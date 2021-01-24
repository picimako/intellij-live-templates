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

# Google Guava

## Stopwatch elapsed - TimeUnit

```java
com.google.common.base.Stopwatch stopwatch = Stopwatch.createStarted();

long elapsedTime = stopwatch.elapsed($timeunit$);
```

| Config | Config value |
|---|---|
| General | Abbreviation: *stopelapsedunit*<br>Options enabled: Reformat according to style, Shorten FQ names |
| <pre>$timeunit$</pre> | Expression: `completeSmart()`.<br>Default value: `"TimeUnit.SECONDS"` |

## Stopwatch elapsed - Duration

```java
com.google.common.base.Stopwatch stopwatch = Stopwatch.createStarted();

java.time.Duration elapsedTime = stopwatch.elapsed();
```

| Config | Config value |
|---|---|
| General | Abbreviation: *stopelapsed*<br>Options enabled: Reformat according to style, Shorten FQ names |
