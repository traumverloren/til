Regex. You understand it one day, and then the next day it's total magic again.

```
Look ahead of a word
(?=(word))
```

```
Look behind a word
(?<=(word))
```

```
Look behind a word and select all of the line following
(?<=(word)).*$
```
```
Look behind a word and select all of the line following, and the next line, and the next
(?<=(word)).*$(\n.*$)(\n.*$)
```
