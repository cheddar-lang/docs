# number

The number class for Cheddar

#### Arguments:
 - Base
 - Zero shift (zeros to append _before_ base change)

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
