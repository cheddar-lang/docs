# Structure

The file structure of STDLIB (the standard library) is simple. It's located in the `src/stdlib/` directory. In this root directory, you'll see two files: `api.es6` and `stdlib.es6`. Each of these have their own uses:

 - `stdlib.es6`: This constructs the global scope (i.e. the standard library). 
 - `api.es6`: This is the API itself, it defines useful functions and provides the Cheddar primitives (`CheddarString`, `CheddarNumber`, etc.) to you. This also helps avoid cyclic dependency errors.

Here's a diagram of the further folder structure

```
stdlib/
 |
 |-- ns/             Namespaces
 |    |- <name>/       The implementations
 |    |- <name>.es6    Compiles the namespace's properties/methods
 |
 |-- primitive/      Primitive Libraries
      |- <name>/       A specific primitive
          |- lib/        The implementations
          |- lib.es6      Compiles the methods/properties
          |- static.es6   The static properties
```

