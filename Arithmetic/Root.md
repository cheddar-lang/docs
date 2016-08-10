# Root

## Syntax
```swift
sqrt x
cbrt x
x root y
```

## Explanation

### `sqrt`/`cbrt`
`sqrt` and `cbrt`, find the square root and the cube root of the given operand respectively. They are aliases of `x root 2` and `x root 3`. There is minimal speed different, if any, and are simply exist for clearer code.

### `root`
`root` finds the $n^{th}$ root of `x` ($\sqrt[n]{x}$), where $n = y$. It is equivilent to `x ** y ** -1`

## Examples

```swift
sqrt 16    // 4
cbrt 8     // 2
16 root 4  // 2
```