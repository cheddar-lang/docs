# Slice (`.slice()`)

| type | returns |
| ---- | ------- |
| Method | `string`` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| A    | number | The starting position to slice from |
| B    | number, optional | The position to end the slice. If omitted this slices to the end. If negative, it will refer to the position from the end |
## Explanation
The `.slice` function returns a substring from two given indexes of the original string.

## Examples

```swift
"foo".slice(1, 2) == "o"
"0123".slice(0, -1) == "012"
```
