# Chars (`.chars`)

| type | returns |
| ---- | ------- |
| Getter | `array<string>` |

## Explanation
Returns an array of the bytes in a given string, handles unicode surrogates properly.

## Examples

```swift
"Hello" == ["H", "e", "l", "l", "o"]
"🐐 > 🐑" == ["🐐", " ", ">", " ", "🐑"]
```
