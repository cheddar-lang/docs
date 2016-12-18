# Length (`.len`)

| type | returns |
| ---- | ------- |
| Getter | `number` |

## Explanation
Returns the size of the string accounting for surrogate characters.

## Examples

```swift
"".len == 0
"🐐".len == 1
"1\n2".len == 3
"Hello".len == 5
"1 2 3".len == 5
```
