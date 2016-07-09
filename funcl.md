# Lambda
**Lambdas are anonymous functions** (functions without a name). "Without a name" just means they are declared without a name, you can still give them a name.

You can use lambdas for all sorts of things, usually they are used for quick, throw-away functions. This includes things such as arguments to `#map` and `#each` functions. Lambdas also play in important role in functional paradigm.

Lambdas in Cheddar have **implicit return**. The last statement's result will be implicitly returned. _Always_. 

> #### **Note** Best Practice
>
> In lambdas, what is being implicitly returned is easy to tell most of the time. 
> However this is not the case for many statements such as loops and ifs.
>
> Take for example this for loop:
>
> ```js
> input -> {
>     for letter of input {
>         if letter.ord() < letter.lower.ord() {
>             letter.lower.ord()
>         } else {
>             letter.ord()
>         }
>     }
> }
> ```
> It's difficult to tell what this is returning but it is either `letter.lower.ord()` or `letter.ord()`.
>
> To avoid this, store the desired return value in a variable:
> ```js
> input -> {
>     var result
>     for letter of input {
>         if letter.ord() < letter.lower.ord() {
>             result = letter.lower.ord()
>         } else {
>             result = letter.ord()
>         }
>     }
>     
>     result // return value
> }
> ```

If you want nothing to be returned, it is best to have the function return `nil`.

## Syntax
Syntax for lambdas shoud be familiar to lambdas in other C-based languages. Cheddar's lambdas however have some more features:

```js
-> Number::IO.prompt('Number? ')
arg1 -> arg1 * 2
(arg1, arg2) -> arg1 + arg2
arg1 -> {
    var a = arg1 / 2
    [a * 3, a * 4]
}
```

### Formal Syntax

The above roughly covers lambda usage. The formal syntax is along the lines of:

```c
[ arguments ] "->" ( "{" code "}" | expression )
```

The syntax can be derived as:

$$
\begin{matrix}
\begin{aligned}
F &\rightarrow \alpha \lambda \beta \\
\alpha &\rightarrow \text{(}V\text{)} \\
\alpha &\rightarrow v \\
\alpha &\rightarrow \epsilon \\
\beta &\rightarrow \left\{ \Delta \right\} \\
\beta &\rightarrow \delta \\
V &\rightarrow V\text{,} v \\
V &\rightarrow v \\
V &\rightarrow \epsilon
\end{aligned}
\\~\\
\Lambda = \left(\left\{F,\alpha\right\}, \left\{\lambda,v,\delta,\Delta\right\}, P, F\right)
\end{matrix}
$$

Where $$\delta$$ represents an expression, $$\Delta$$ represents a code block, $$\lambda$$ represents `->`, and $$v$$ represents a specific argument (descriped later)

### Explanation
The lambda syntax is in the form: `<arguments> -> <code>`.

**`<arguments>`** is the arguments to recieve from the lambda. This is either a single argument (described later), an array of arguments delimited by `(` and `)`, or nothing.

**`<code>`** is either an expression, or a code block.

## Argument Syntax
Lambda arguments are powerful and define what variables are passed to it, and how it is enforced. 

**An argument is a variable** which is passed to the lambda from it's call. An argument can be any variable name. Which is described in the "Variables" chapter.

**Type annotations** on a variable enforce what type that variable must be. You can simply prepend: `<type>:` to the argument to add a type annotation. Without one, any type is accepted. Free whitespace is allowed around the `:`. An example is `String: arg`.

**Optional arguments** allow variables to not be passed. Usually if a value is not passed for a function's argument, an error is thrown. Appending a `?` to the variable makes it **optional**. If a value is not supplied for the argument, it will be set to `nil`.

A **default value** is what a variable will be set to if no value is supplied. Default values _cannot_ be used with optional arguments. To specify a default argument, append `= <expression>` where `<expression>` is an expression which evaluates to what the default value should be.

### Argument Examples
Some examples of arguments:

```elixir
arg                  Normal argument
arg?                 Optional argument
Bool: arg            Argument that must be a boolean
Bool: arg?           Optional argument that must be boolean if supplied
Bool: arg = false    Argument that must be a boolean that defaults to false
```

## Lambda Examples

```js
-> Number::IO.prompt("Number? ")    // Anonymous function prompting from user
```