# Function

The syntax for functions is current under design and is not finalized. The current proposal is:

```swift
func MyFunction(String: str2, arg) {
    return Number::str2 + arg
}
```

This defined a function `MyFunction` which takes to arguments `str2` and `arg`. `str2` has had it's type explicitly set to `String` and will throw an error if not. It will return the string, cast to a number, added to `arg2`.

---

The proposed lambda syntax is:

```js
-> (arg1, arg2) arg1 + arg2;
-> (arg1, arg2) {
    arg1 + arg2
}
add -> (arg1, arg2) arg1 + arg2;
```

All lambdas have implicit output. The last case assigns the lambda to variable `add`.