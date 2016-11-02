# Lines (`.lines`)

| type | returns |
| ---- | ------- |
| Getter | `array<string>` |

## Explanation
Returns an array of the given string's lines. This is a cross-platform solution which supports non-standard line breaks.

## Examples

```swift
"foo".lines == "foo"

"Hello
World" == ["Hello", "World"]

"Hello\r\nWorld" == ["Hello", "World"]
```
