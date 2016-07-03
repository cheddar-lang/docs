# func

The function class for Cheddar

#### Arguments:
 - argument matrix.  
   a 2d array in the form of:
   ```
   [
       ["arg_name", { <options> }],
       ...
   ]
   ```
   Where `<options>` is an object specifing any of
   - **`Type` (default: any)** the argument should be this type
   - **`Default`(default: false)** if non-falsy and the associated argument was not passed, the argument will be set to this
   - **`Splat` (default: false)** if true, this, and the following arguments will be combined and returned as a Cheddar array
   - **`Optional` (default: false)** if true, the argument is optional and will _not_ throw an error if not provided.
 - a function, the implementation

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