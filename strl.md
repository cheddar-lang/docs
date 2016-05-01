# String

Strings are traditionally a sequence of characters, but you can think of them as "text". Cheddar's strings are like [Ruby](https://www.ruby-lang.org/en/)'s strings.

---

## Basic Syntax

Strings in Cheddar are delimited by **double quotes** or **single quotes**. Additionally, Cheddar supports **literal newlines** within Strings.

```c
"Hello, World!" // Both of these are
'Hello, World!' // exactly the same
```

Whichever quote you use is your choice and varies based on your personal preference. For the rest of this documentation, double quotes will be used.

## Using special characters
 Cheddar is, again, like the C language in respect to escaping. You can use a **backslash** before a character to insert it's literal form rather than it to have a special meaning.

```c
"This is a double quote: \"."
'This is a single quote: \'.'
"This is a blackslash: \\"
```

## Using formatting
 "String formatting" is a way to insert the **result of an expression** directly into a string. Using `#{ ... }` you can "format" a string.
 
 ```ruby
 "2+2=#{2+2}" // evaluates 2+2 and returns 4
 "2+2=4" // Has the same value as the above
 ```
 
 Backslashes also work to escape formatting:
 
 ```ruby
"2+2=\#{2+2}" // Does NOT evaluate 2+2 or the format
 ```