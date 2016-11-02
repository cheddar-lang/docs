# Count (`.count()`)


| type | returns |
| ---- | ------- |
| method | `number` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| needle | string | The substring to search for |

## Explanation
Returns the amount of times the given substring (`needle`) appears within the string.

## Examples

```swift
"Hello".count('l') == 2
"".count("I'm not in the string") == 0
```
