# Head (`.head()`)


| type | returns |
| ---- | ------- |
| method | `string` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| size | int | the amount of characters to grab |

## Explanation
Returns a substring of the given size, starting at the string's first index. Roughly equivilent to `#slice(0, size)`

## Examples

```swift
"Hello, World".head(5) == "Hello"
"Hi".head(3) == "Hi"
```
