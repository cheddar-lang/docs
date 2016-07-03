# Primitive Objects

In order to understand _how_ to create classes and namespaces. You'll need to understand _what_ namespaces and classes actually are internally. These are the five things you'll need to understand:

 - What a Scope is
 - What a Class is
 - What a Variable is
 - What a Namespace is

These will be covered in this section

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
  whatIsSelf => self
}

var A = MyClass{};
A.whatIsSelf();   // < Instance of "MyClass" >
```

as you can see, `whatIsSelf` is passed its scope (`A`) by the evaluator, but the scope is not directly attached to `whatIsSelf`.

### What is a Variable?
A variable is a simple wrapper for a value to be placed in a scope. The variable class specified a couple properties, including:

 - Whether the variable is read-only
 - Whether the variable is static-typed.
 - Whether a getter/setter should be used, rather than the value

In Cheddar, all scope values are `CheddarVariable`s but this rule is not enforced. If a variable is not wrapped as a CheddarVariable, an uncaught error be occur.

### What is a Namespace?

