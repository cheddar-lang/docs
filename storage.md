# Storage and Scoping

In order to understand _how_ to create classes and namespaces. You'll need to understand _what_ namespaces and classes actually are internally. They are three things you'll need to understand:

 - What a Scope is
 - What a Class is
 - What a Variable is
 - What a Namespace is

### What is a Scope?
A scope is the most basic interpretation class. You can think of it as a glorified hashmap which can inherit. It's structure is:

```

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

### What is a Variable?

### What is a Namespace?