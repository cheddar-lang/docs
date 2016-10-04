## What is a Variable?
A variable is a simple wrapper for a value to be placed in a scope. The variable class specified a couple properties, including:

 - Whether the variable is read-only
 - Whether the variable is static-typed.
 - Whether a getter/setter should be used, rather than the value
 - Whether the variable is public or private (only applicable within specific senarios)

In Cheddar, all scope values are `CheddarVariable`s but this rule is not enforced. If a variable is not wrapped as a CheddarVariable, an uncaught error may occur.
