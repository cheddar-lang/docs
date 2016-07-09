# Lambda
**Lambdas are anonymous functions** (functions without a name). "Without a name" just means they are declared without a name, you can still give them a name.

You can use lambdas for all sorts of things, usually they are used for quick, throw-away functions. This includes things such as arguments to `#map` and `#each` functions. Lambdas also play in important role in functional paradigm.

Lambdas in Cheddar have **implicit return**. The last statement's result will be implicitly returned. _Always_. 

> #### Note::Best Practice
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

---