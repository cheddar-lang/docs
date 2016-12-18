# Tail (`.tail()`)


| type | returns |
| ---- | ------- |
| method | `string` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| size | int | the amount of characters to grab |

## Explanation
Returns a substring of the given size, starting at the string's last character. Roughly equivilent to `#slice(-size)`
## Examples

```swift
"Hello!".tail(1) == "!"
// Goat emoji is a surrogate of two bytes
"🐑🐐".tail(2) == "🐐"
```
