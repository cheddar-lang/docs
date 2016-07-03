## What is a Scope?
A scope is the most basic interpretation class. You can think of it as a glorified hashmap which can inherit. It's structure is:

```
             Scope
               |
  +------------+------------+
  |            |            |
scope     inheritance   interface
             chain          |
                        +---+---+
                        |   |   |
                       get set has
```

What is each part?:

 - `scope`: a hashmap. The **key** is the variable name, the **value** is the value of the variable (this is usually a `CheddarVariable`, described later).
 - `inheritance chain`: this is either **another Scope** class, or **`null`**. If this exists, its `scope` will also be navigated, acting as inheritance. This is so the class being inherited from is modified itself, rather than a copy of it.
 - `interface`: this provides a **very raw interface** for `get`ting a variable, `set`ting a variable, or checking if it `has` a variable. These can be overwritten, but these methods are **not to be confused with** getters and setters.

All together this class can implement scopes. Here's an (psuedo-code) example of what is called when (the path the program takes is highlighted with `+`):

```js
a = 1;     + interface/set(a, 1)
           - if inheritance chain/has(a)
           -    inheritance chain/set(a, 1)
           + else
           +    scope/set(a, 1)

{
    a = 1  + interface/set(a, 1)
           + if inheritance chain/has(a)
           +    inheritance chain/set(a, 1)
           - else
           -    scope/set(a, 1)
}

print a;   + interface/get(a)
           - if inheritance chain/has(a)
           -    inheritance chain/get(a)
           + else
           +    scope/get(a, 1)

```