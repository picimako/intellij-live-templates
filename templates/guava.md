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
