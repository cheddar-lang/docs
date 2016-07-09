# Lambda
**Lambdas are anonymous functions** (functions without a name). "Without a name" just means they are declared without a name, you can still give them a name.

You can use lambdas for all sorts of things, usually they are used for quick, throw-away functions. This includes things such as arguments to `#map` and `#each` functions. Lambdas also play in important role in functional paradigm.

Lambdas in Cheddar have **implicit return**. The last statement's result will be implicitly returned. _Always_. 

> #### Note::Best Practice
> 