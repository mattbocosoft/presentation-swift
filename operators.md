#Operators  

As with all programming languages, Swift contains a set of operators that act on its variables. Most of these operators are just like other languages or are intuitive and cross-discipline (like the arithmetic operators). Operators are either *unary* (1 target), *binary* (2 targets), or *ternary* (3 targets).  

The **assignment** operator assigns a value to a variable:  
```
(variable = value)
```

The **arithmetic** operators work just as taught in basic mathematics classes:  
```
(a + b) // addition
(a - b) // subtraction
(a * b) // multiplication (×)
(a / b) // division (÷)
```

The *remainder* operator divides the first target by the second target, and then returns the remainder, also known as the modulus. It can be used on both whole and floating point (non-whole) numbers.  
```
(22 % 3)   // remainder, returns 1
(22.5 % 3) // remainder, returns 1.5
```

There are arithmetic shortcuts that are useful for simplifying code by taking the result and storing it immediately in the variable:  
```
(a++)    // Adds 1 to the variable 'a' and store the final value in 'a'
(a--)    // Subtracts 1 from the variable 'a' and stores it in 'a'
(a += 2) // Adds 1 to the variable 'a' and store the final value in 'a'
(a -= 2) // Adds 1 to the variable 'a' and store the final value in 'a'
```
The last two forms can also also be used for other arithmetic operators besides addition and subtraction:  
```
(a *= 2) // Multiplies 'a' by 2 and stores the final value in 'a'
(a /= 2) // Divides 'a' by 2 and stores the final value in 'a'
```

Values can flip signs by applying '-':  
```
(-a) // Toggles the sign of 'a' (positive goes to negative, and vice-versa)
```

All the operators above apply an operation to a value and return a result. The *comparison* operators compare two values and return either true or false:  
```
(a == b) // Returns true if a and b are equal, otherwise returns false
(a != b) // Returns true if a and b are unequal, otherwise returns false
(a > b)  // Returns true if a is greater than b, otherwise returns false
(a < b)  // Returns true if a is greater than b, otherwise returns false
(a >= b) // Returns true is a is greater than or equal to b
(a <= b) // Returns true is a is less than or equal to b
```

**Range** operators are especially useful in the context of loops:  
```
for index in 5...10 {
   variable++
}
```

The range `(a...b)` is inclusive of both a and b, whereas `(a..<b)` does not include b.  

There are two useful `?` operators in Swift which are very useful. The first is the only ternary operator used in Swift and is also common in other programming languages.  
```
(a ? b : c) // If a is true, return b. Otherwise return c
```

The second is useful when checking for nil variables:  
```
a ?? b      // Return a if it is non-nil, otherwise return b
```

*Logical* operators and parentheses are important for combining multiple comparison operators in a single statement:  
```
(a || b) // Returns true if either a or b are true
(a && b) // Returns true if both a and b are true
(!a)     // Returns true if a is false
(a || (b && c)) // Returns true if either a is true or if both b and c are true
```

This page has covered the basic Swift operators. To read more about advanced operators, check out the [Advanced Operators](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-ID28) section in the Swift Programming Language book.
