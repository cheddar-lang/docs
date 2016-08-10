# Exponentiation (`**`)

## Syntax
```js
x ** y
```

## Explanation
The exponentiation operator raises the first operand to the power of the second. It is right associative meaning:

```js
x ** y ** z == x ** (y ** z)
```

## Examples

```swift
2 ** 4   // 16
2 ** -3  // 0.125
-2 ** 3  // -8
16 ** .5 // 4
```