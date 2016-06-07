# While Loops

`while` loops are the fastest, most basic loop. Due to the simplicity of this block, most programmers are very familiar with this construct. Parenthesis are optional on these.

The usage is:

```swift
while <condition> {
    <code block>
}
```

As long as the condition is true, the code block will execute. Once, or if, the condition is false, the loop will stop executing and the program will continue.

An example of the use is:
```swift
var input := nil;
while !( (input = IO.prompt("[Y/n]> ")) in "Yn" ) {
    print "Please enter either 'Y' or 'N'"
}
print "You inputted #{input}"
```