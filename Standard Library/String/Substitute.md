# Substitute (`.sub()`)

| type | returns |
| ---- | ------- |
| Method | `string` |

## Arguments
| name | type | description |
| ---- | ---- | ----------- |
| value | regex \| string | The regex to perform replacements on |
| replacement | string \| `(...matches) -> string` | Replacement for each matches location |


## Explanation
Matches all occurences of `value`, with `replacement`.

### `value`
 - If value is a string. It is matched as appears in the string gloablly, it is not converted to a regular expression.
 - A regular expression's capture groups are passed to the replacement if applicable.

### String replacements
If the replacement is a string, the following charcater sequences have special behavior:

 | name | explanation | example |
 | ---- | ----------- | ------- |
 | `$\$` | Inserts a literal `$` | `"$\$59.99"` |
 | `$&` | Refers to the entire matches string | `"( $& )"` |
 | `$n` | Where `n` is a number, refers to the `n`th capture group | `$2, $1` |
 | `` $` `` | Refers to the match the precedes the given match | `` encountered: $` `` |
 | `$'` | Refers to the match that follows the given match | `upcoming: $'` |

### Function replacements
If the replacement is a function, the capture groups are passed in the format `( c1, c2, ..., cn )`. The function should return string, otherwise an error will be thrown

## Examples

```swift
"1 + 1 = 2".sub(/\d+ ([+*/-]) \d/g, "$1") == "+ = 2"
"1 + 1 - 2".sub(/(\d+ )?([+-]) \d+/g, "$'") == " - 2 "
"Hi".sub("i", "ello") == "Hello"
```
