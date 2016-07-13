# func

The function class for Cheddar

#### Arguments:
| name | type | description |
| ---- | ---- | ----------- |
| `arguments` | 2D array | (described below) this matrix described the arguments for the function. In the form of `[ ["arg_name", { <options> }] ]`
| `body` | function | (described below) the function body

###### arguments matrix:

| name | type | default | description |
| ---- | ---- | ------- | ----------- |
| `Type` | `cheddar.class` | n/a | If provided, the argument is required to be of the given type
| `Default` | `cheddar.class{}` | n/a | If provided and the argument is not provided, it will be set to this rather than throwing an error.
| `Splat` | bool | `false` | If provided, this and the following arguments will be combined into a `cheddar.array` object.
| `Optional` | bool | `false` | If true, the argument will be `nil` if not provided |

###### Function Body

| argument | description |
| -------- | ----------- |
| first    | This is the **function's scope** as a `cheddar.scope`.
| second   | This is a function which returns a variable's value, given a variable name. |

#### Usage:
`-> (a, b = 0) a + b`, with api:
```js
new cheddar.func(
  [
    ["a", {}],
    ["b", {
        Default: cheddar.init(
          cheddar.number,
          10, 0, 0
        )
    }]
  ],
  function(scope, input) {
    return cheddar.init(
      cheddar.number,
      10, 0,
      input("a").value + input("b").value
    );
  }
)
```