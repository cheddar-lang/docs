# Functional Bonding (`&`)

## Syntax
```swift
f & a
a & f
```

## Explanation
Depending on the side of the operand to bond, it will be binded to side it is on to the function.

```swift
f & a == *args -> f(*(args + [a]))
a & f == *args -> f(*([a] + args))
```

## Examples
The following are examples utilizing functional operators:
```swift
let mod10 = (%) & 10;
mod(15) == 5
```

```swift
let reciprocal = 1 & (/);
reciprocal(1 / 3) == 3
```
