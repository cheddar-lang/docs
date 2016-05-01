# Array
 An array is a **data structure** that is an ordered sequence of values. Arrays in Cheddar are dynamic and can have the values of any class. Due to the fact arrays are dynamic, their length is not fixed. This means an element can be inserted at any arbitrary point within the array. Empty elements are automatically filled with `nil`.
 
 ---
 
 Arrays are delimited with square brackets (`[` and `]`). Elements are expressions and are separated by commas.
 
 ```c
 [1, 2, 3, 4]
 [1,, 3] // [1, nil, 3]
 [1, "2", "3", 4, "5", 6]
 ```