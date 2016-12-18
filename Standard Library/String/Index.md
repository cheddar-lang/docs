# index (`.index()`)


| type | returns |
| ---- | ------- |
| method | `number` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| needle | string | The substring to search for |

## Explanation
Returns the index of the start of the `substring` in the given string. Returns `-1` if not found.

## Examples

```swift
"Hello! Hi!".index("Hi") == 7
"Goats :D".index("Hi") == -1
```
