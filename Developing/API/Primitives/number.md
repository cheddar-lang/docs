# number

The number class for Cheddar

#### Arguments
| name | type | description |
| ---- | ---- | ----------- |
| base | number | base to translate the given to |
| shift | number | number of zeros to append to the value before base change |
| value | number or string | The literal value of the number |

#### Usage:
`0b101`, with api:
```js
cheddar.init(
    cheddar.number,
    2, 0, 101
)
```

---

`0xFF`, with api:
```js
cheddar.init(
    cheddar.number,
    16, 0, 'FF'
)
```

---

`123`, with api:
```js
cheddar.init(
    cheddar.number,
    10, 0, 123
)
```
