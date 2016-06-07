## For

`for` loops are the most concise loop construct. On the `for`, **parenthesis are required**, this is described in the [Control Flow](#Control Flow) section. There syntax is highly resemblant of their C counterpart:

```go
for (var i := 0; i < 5; i++) {
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
i is: 2
i is: 3
i is: 4
i is: 5
```

This is because the variable `i` is initialized to `0` at the beginning. Then, because `i` is less then `5`, it will keep running the code block until `i` is not less than `5`. This happens because the `i++` increases `i` everytime, after, the code block (i.e. the `print`) is executed.