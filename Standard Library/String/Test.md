# Test (`.test()`)

| type | returns |
| ---- | ------- |
| Method | `boolean` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| regex | regex | Regex to verify if matches

## Explanation
Determines if given `regex` matches the string.

## Examples

```swift
"Goat".test(/oat/) == true
"HeLlO".test(/hello/i) == true
```
