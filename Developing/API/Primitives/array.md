# array

The array class for Cheddar

#### Arguments

| name | type | description |
| ---- | ---- | ----------- |
| `item` | any | the array item |
| ...  | 〃 | 〃 |

#### Usage:
`[]`, with api:
```js
cheddar.init(
    cheddar.array
)
```
---
`[1,2,3]`, with api:
```js
cheddar.init(
    cheddar.array,
    cheddar.init(cheddar.number, 10, 0, 1),
    cheddar.init(cheddar.number, 10, 0, 2),
    cheddar.init(cheddar.number, 10, 0, 3)
)
```
