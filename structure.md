# Structure

The Cheddar source code is located in the `src/` directory. 

### Tokenizer

The tokenizer has no specific folder structure. Terminal parsers, are generally kept in the `literals/` directory, expression non-terminals in the `parsers/`, and statements in the `states/` directory.

### Standard Library

The file structure of STDLIB (the standard library) is simple. It's located in the `src/stdlib/` directory. In this root directory, you'll see two files: `api.es6` and `stdlib.es6`. Each of these have their own uses:

 - `stdlib.es6`: This constructs the global scope (i.e. the standard library). 
 - `api.es6`: This is the API itself, it defines useful functions and provides the Cheddar primitives (`CheddarString`, `CheddarNumber`, etc.) to you. This also helps avoid cyclic dependency errors.

Here's a diagram of the further folder structure

```
stdlib/
 |
 |-- stdlib.es6      Standard Library List
 |-- api.es6         The STDLIB API
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

`<name>` would be replaced with the name of that specific item. 

---

If you which to create a new namespace, or a global class. Create a `<name>.es6` file in `ns/` and a folder in the same directory. `<name>.es6` will be where your class/namespace is defined. Individual method implementations can go in the folder you created. For example, if I was creating a package named "Geometry" my files/folders would look like:

```
stdlib/ns/
 |-- geometry.es6
 |-- geometry/
```