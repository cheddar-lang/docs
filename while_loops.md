# While Loops

`while` loops are the fastest, most basic loop. Due to the simplicity of this block, most programmers are very familiar with this construct. Parenthesis are optional on these.

```swift
var input := nil;
while !( (input = IO.prompt()) in "Yn" ) {
    print "Please enter either 'Y' or 'N'"
}
print "You inputted #{input}"
```