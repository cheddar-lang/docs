# Defining Functions

Cheddar has various types of functions, these include:
 - Methods
 - Named Functions
 - Lambdas

Methods are declared as part of a class which are covered within a later chapter but named functions and lambdas are specified here.

## What is a Lambda?

While a named function's name may be obvious at what it does, this is not the case for lambda. Lambda is the greek letter $$ \lambda $$, what a lambda _is_ in programming is an **anonymous function**. Now this brings up the question:

> _What is as an "anonymous function" and why are they important?_

If you come from a C background, you may be customized to functions which are declared and must have a "name" (i.e. assigned to a variable). As you come to functional programming, this is not the case for a majority of functions. Functions tend to not have named and are often dynamically created.

So lets answer the first question. **An anonymous function is** a function without a name, or one not assigned to a variable. It can be used as a literal within expressions just like any other object or value, such as a number, or a string. **This is useful** because this allows you to quickly create a function to pass to another function as an argument.

This idea of using functions together is what functional programming branches off of. While this simplification of functional programming may of described the basis of it sufficiently, enough jargon may be used in this chapter to make the concepts confusing. For this reason, a glossary is provided which can be referenced inline.
