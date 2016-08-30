# Functional Composition (`+`)

## Syntax
```swift
f + g
```

## Explanation
Performs functional composition on the two operands. Returns a function which passes its arguments to `g` and then too `f`. 

The following are equivilent:
```swift
(f + g)(a,b) == f(g(a,b))
```

## Examples
An example to change a zero-indexed function to a one-indexed function utilizing composition is:
```swift
let fibonacci = n f -> n < 2 ? 1 : f(n - 1) + f(n - 2);
let increment = (+) & 1;

( fibonacci + increment )( 5 ) == 13
```
