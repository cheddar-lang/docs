# Split (`.split()`)

| type | returns |
| ---- | ------- |
| Method | `array<string>` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| seperator | string | regex, default: `/\s+/` | The seperator the split upon

## Explanation
Returns the string split upon the given seperator as a string array. If the argument is a regex, the string will be split where the regex matches.

## Examples

```swift
"hello world".split(" ") == ["hello", "world"]
"hello    world".split() == ["hello", "world"]
"Hello, World".split(/[^A-Za-z]/) == ["Hello", "World"]
```
