# Chunk (`.chunk()`)

| type | returns |
| ---- | ------- |
| Method | `array<string>` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| size | int  | Size of each chunk in resulting array

## Explanation
Splits the given string into substrings of the given size. 

## Examples

```swift
"1234".chunk(2) == ["12", "34"]
"Hello".chunk(3) == ["Hel", "lo"]
```
