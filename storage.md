# Primitive Objects

In order to understand _how_ to create classes and namespaces. You'll need to understand _what_ namespaces and classes actually are internally. These are the five things you'll need to understand:

 - What a Scope is
 - What a Class is
 - What a Variable is
 - What a Namespace is

### What is a Scope?
A scope is the most basic interpretation class. You can think of it as a glorified hashmap which can inherit. It's structure is:

```
             Scope
               |
  +------------+------------+
  |            |            |
scope     inheritance   interface
             chain          |
                        +---+---+
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

### What is a Class?
You may know what a class is, a "blueprint" for which an object is to be constructed from, but internally they are very simple (the source code contains detailed information of their implementation, [the class implementation](https://github.com/cheddar-lang/Cheddar/blob/master/src/interpreter/core/env/class.es6#L1) may provide additional details). A class has 3 main parts:

```
         Class
           |
  +--------+--------+
  |        |        |
scope    init()  instance
```

**A class _is_ a scope**. An instance of a class is really just a scope. This may sound confusing but, think about what a scope _is_, it is a hashmap of variables which can inherit and provides interfacing for accessing it's variables. That sounds just like what a class is.

So what else? A class has an initializer, this is the main part seperating a class from a scope. Here are the steps taken during a class initalization:

 1. **Create** an empty scope (this is called the "instance")
 2. **Copy** the class's scope to the instance (and the inheriting class's is applicable).
 3. **Run** the initializer (`init`) and pass the instance as "self".
 4. **Return** the instance.

As you can see, the returned _instance_, is **just a regular scope**, but pre-populated. When executed, methods are passed the scope as a whole. Here's an example:

```js
class MyClass() {
  whatIsSelf -> self
}

var A = MyClass{};
A.whatIsSelf();   // < Instance of "MyClass" >
```

as you can see, `whatIsSelf` is passed its scope (`A`) by the evaluator, but the scope is not directly attached to `whatIsSelf`.

### What is a Variable?

### What is a Namespace?