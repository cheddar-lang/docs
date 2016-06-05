# Conditional

The conditional (a.k.a. `if`) is one of the most fundamental items in programming logic. Parenthesis on the if **are optional**. Due to this, braces are required around the code block. The rationale for this was that omitting braces can result in difficult to debug, critical bugs, as Apple has shown us<sup>[citation-needed]</sup>.

---

### Definition

The general syntax is the following:

```
if <condition> {
    [statement_1]
} [else if <condition> {
    [statement_2]
} ...][else {
    [statement_3]
}]
```

### Examples

```swift
if 1 == 1 {
    print "1 is in fact 1"
} else {
    print "Your universe is borked"
}
```

---

Additionally, an arbitrary amount of `else if` blocks can be supplied:

```swift
var num := Math.rand(3);

if num == 1 {
    print "Random number was 1"
} else if num == 2 {
    print "Random number was 2"
} else if num == 3 {
    print "Random number was 3"
} else {
    print "Random number was #{num}"
}
```

### Scoping

Ifs, like all other code-blocks in Cheddar are **block scoped**. The condition of the if is evaluated in the parent's context, meaning the new scope will only be created, once the condition has been validated and the code-block is ready to execute. 