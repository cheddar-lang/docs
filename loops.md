# Loops

Loops are the most common way to repeat a task. Additionally sometimes recursion maybe better suited for your needs. Loops are more efficient to the fact their execution is allocated once, and is only re-executed. This is compared to recursion which requires the scope to be reconstructed.

## For

`for` loops are the most concise loop construct. There syntax is highly resemblant of their C counterpart:

```go
for (var i := 0; i < 10; i++) {
    print "i is: #{i}"
}
```

The syntax of the `for` loop is:

```go
for (<initalization>; <condition>; <afterthought>) {
    [code block]
}
```

Essentially the way this works is:

```go
execute initalization
while condition evaluates to true
    execute code block
    execute afterthought
```

The output of the first `for` example would be:

```
i is: 0
i is: 1
i is: 0i is: 2
