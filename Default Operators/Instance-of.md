# Instance-of Operator (`is`)

## Syntax
```swift
obj is Foo
```

## Explanation
Returns if the left operand is an instance of the right operand. If an object is an instanceof a class's superclass, this operator will return true for the superclass.

## Examples

```swift
// Where: Dog IS-A Animal
let o := Dog { ... }
o is Animal
```
