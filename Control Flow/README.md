# Control Flow

In order to perform any sort of logic, control flow statements must exist to  form a decision model. Cheddar is abundant with control flow statements, inheriting syntax and statements, from the C language.

---

> **Note** Best Practice
> 
> In Cheddar, parenthesis are optional around most statements. This is to suit a wider variety of programmings styles.
> For this reason, when using more complex statements, it is generally regarded as better practice to put parenthesis around your condition
> 
> For example the following is readable:
> ```swift
> if input is String {
>     print "Input is a string!"
> }
> ```
> While the following isn't:
> 
> ```go
> if len input = argv[0].split(",", true).map(-> (i) i - 1) > 3 {
>     print "Too many arguments"
> }
> ```
> Without syntax highlighting, this can be quite unreadable at a glance