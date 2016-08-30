# Variables & Constants

A variable is a named representation of some section of memory. Variables are used to store values, one of the most fundamental part of any program. Some examples of declaring variables are:

```js
var my_variable = 123
var my_variable: Number = 123

let my_variable = 123
let my_variable: Number = 123

const my_constant = 123
const my_constant: Number = 123
```

`let` is simply an alias for `var`, they are exactly the same.

## Strong v Weak

Many, now considered, "low-level" programming languages such as C are **"strongly" typed**. This means, you cannot change the type of a variable once it has been declared. This type is passed with the variable's decleration. For example the following is invalid:

```c
int foo = 123; // Declares `foo` as an integer;
foo = "bar";   // Error: cannot make an int a string
```

Some other languages such as JavaScript and Python, are **"weakly" typed**, this means you can change the type of a variable after it has been declared:

```js
var foo = 123;
foo = "bar";   // just fine
```

---

**Cheddar uses both**. Different programmers have different preferences on which typing is the best. Strong typing can be used as beneficial to avoid hard to debug bugs when typed automatically change. Weak typing can be helpful when quickly scripting. Cheddar suits both:

```swift
// == Weak Typing ==
var weak_var = 123
weak_var = "bar"    // no error

// == Strong Typing ==
var strong_var : Number = 123
strong_bar = "bar"  // error
```

**Note:** If you're using a Cheddar version < 0.3 (`cheddar -V`) implicit variables use the legacy `var a := b` syntax.

## Constants

Often times you want a variable that doesn't change, to be a "constant". Cheddar supports this, simply instead of the `var` keyword, use `const`:

```js
const my_constant = 123
my_constant = "foo";     // Error
```

Constants can also be strongly & weakly typed, except that the only time the type checking will ever happen is at the deceleration. 
