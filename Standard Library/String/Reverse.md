# Reverse (`.rev`)

| type | returns |
| ---- | ------- |
| Getter | `string` |

## Explanation
Returns the reverse of a string. Handles unicode surrogates.

## Examples

```swift
"🐐🐑".rev == "🐑🐐"
"Hello! Hi!" == "!iH !olleH"
"Hi".rev == "iH"
"".rev == ""
```
