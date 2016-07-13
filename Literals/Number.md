# Number

Numbers are a way to represent any ordinal limited by your computer's memory.

---

Cheddar's numbers support **decimals**, **separators**, **bases**, and **implicit promotion**.

## Basic Numbers

The most basic form of a number in Cheddar are integers and decimals. Cheddar wraps both of these in a "Number" type. You can write numbers as you would in most languages:

```c
1
123
123.456
.123
0.1
1.0
```

## Separators
 Often in programs you deal with large numbers. Numbers are often written with commas to distinguish the sections of the number. Cheddar provides a simple **syntax for number separators**, `_`.
 
 ```swift
 123_456 // Same as 123456
 1_2_3_4 // Same as 1234
 1__2345 // same as 12345
 ```
 
 As you can see, Cheddar does not enforce where you place your number separators.
 
 ## Bases
 
 You can type **binary**, **octal**, and **hexadecimal** literals in Cheddar:
 
 ```javascript
 0b1010   // *b*inary
 0xFF     // He*x*adecimal
 0o0222   // *o*ctal
 ```
 
 What's the zero at the beginning? That specified the amount of **zeros to append** to the integer section of the number. For example:
 
 ```java
 2b1 // equal to 0b100
 1xF // equal to 0xF0
 ```