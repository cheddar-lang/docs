# Match (`.match()`)

| type | returns |
| ---- | ------- |
| Method | `array<string>` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| regex | regex | Regex to match string

## Explanation
Returns an array of matched strings. When and if the `g` flag is provided, `.match()` returns all the matches in the string. Regardless of flags, `.match()` will always return a string array.

## Examples

```swift
"Hello! Hi!".match(/H.+?!/) == ["Hello!"]
"Hello! Hi!".match(/H.+?!/g) == ["Hello!", "Hi!"]
```
