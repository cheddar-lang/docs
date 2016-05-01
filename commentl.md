# Comment

Comments are sections of code which are ignored by the interpreter. You may use them to write notes **describing** your code or to aid people reading your code in **understanding** it.

Cheddar has **C-style** comments, you can delimit a comment either with `//`, `#`, or `/* .. */`:

Comments can go wherever **whitespace can go**. This means comments do not work within strings.

---

A single-line comment `//` or `#`, starts at any point in the line and continues until either a new line or the EOF (end of file).

```php
// Hello, World! This is my comment
# This is also a comment!
```

---

Multiline comments are a little more special. They support _nested_ comments which will elaborated more on. They will span until a matching `*/` has been found or the EOF.

```c
/*
Hello, this is my multi-line comment.
I can use this to quickly mark out blocks of code
or to just write longer messages.
*/
```

```c
/*
This comment does not have an ending,
 but it will work.
This is because comments will continue to
 the EOF if it can't find a `/*`
```

```c
/*
This is an example of nested comments.

If there is  another multiline comment
 within this one. It won't close this comment
 
  /*
   This is another coment
  */
  
This comment is still going as the previous `*​/`
did not close this comment.
 Note: the `*​/` before has a zero-width space
   between the * and /.
   This is why the comment didn't end
 
*/
```