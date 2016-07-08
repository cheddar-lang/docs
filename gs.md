# Getting Started

The API is very simple to use and get started with. Depending on what you'd like to make, you're going to need to do different things. The Cheddar source code is located in the `src/` directory.

### Creating a namespace/class

If you wish to create a global namespace or class, make sure you've followed the instructions specified in the [Structure](./structure.md) article. `<name>` represents the name of your library.

 1. Locate `stdlib.es6` in the `stdlib/` directory.
 2. Locate the text `/** Global Libraries **/`. Directly underneath this, create a line in the following format:
```js
STDLIB.Item("<name>");
```
 3. Now in `ns/<name>.es6`. Set the contents to the template:
```js
export default function(cheddar) {
        return <implementation>;
}
```
`<implementation>` is to be replaced with your implementation. The `cheddar` variable, introduced by the function, is the API. `<implementation>` should not be wrapped as a variable. The API and it's details are described in the following sections. 

#### Adding items to your Namespace
If you're creating a namespace. Set `ns/<name>.es6` to:
```js
export default function(cheddar) {
     return cheddar.namespace(<data>);
}
```
where `<data>` is a 2D array representing the namespace's items. The most common format of a namespace looks like:

```js
export default function(cheddar) {
     return cheddar.namespace([
         ["<item>", cheddar.from(require("./<name>/<item>"))
     ]);
}
```

#### Creating a Class
To create a class. You can use the following format:

```js
export default function(cheddar) {
     return class <name> extends cheddar.class {
     }
}
```

More information on classes will be available once more documentation is written.