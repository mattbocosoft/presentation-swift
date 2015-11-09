**CSCI 5828: Foundations of Software Engineering**  
*Fall 2015, Professor Kenneth Anderson*

Student: **Matthew Thomas**  
Presentation 4  

![swift-logo](images/swift-logo.png)  
# Swift Programming Language  

Swift is a relatively new programming language designed by [Chris Lattner](https://en.wikipedia.org/wiki/Chris_Lattner) and other developers at Apple. The language began to be developed in 2010 and was announced to the public in June 2014. Since then, the language has undergone many changes to harden its syntax and semantics through a series of public betas. Swift is the *eventual* replacement for Objective-C, the programming language that [NeXT](https://en.wikipedia.org/wiki/NeXT) began using it in the 1980s and Apple later began using when Apple acquired NeXT, however the two programming languages currently work hand in hand.    

Swift is multi-[paradigm](https://en.wikipedia.org/wiki/Programming_paradigm) (e.g. Imperative, Functional, Object-Oriented, etc.) programming languages that has taken many of the best aspects of Objective-C and added safe programming patterns and modern features.  

###Operators  

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

All the operators above apply an operation to a value and return a result. Another kind of operator compares two values and returns either true or false:  
```
(a == b) // Returns true if a and b are equal, otherwise returns false
(a != b) // Returns true if a and b are unequal, otherwise returns false
(a > b)  // Returns true if a is greater than b, otherwise returns false
(a < b)  // Returns true if a is greater than b, otherwise returns false
(a >= b) // Returns true is a is greater than or equal to b
(a <= b) // Returns true is a is less than or equal to b
```

To read more about advanced operators, check out the [Advanced Operators](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-ID28) section in the Swift Programming Language book.

###Collections  

###Optionals and Optional Chaining  

###[Flow of Control](https://en.wikipedia.org/wiki/Control_flow)  

###Classes  

####Initializers  

Initializers do not return a value.
All stored non-optional properties must be initialized.

###Extensions  

###Protocols  

###Functions and Methods  

###Subclassing  

###Error Handling  

4 ways to handle errors
1. Propagating Errors Using Throwing Functions  
2. Handling Errors Using Do-Catch  
3. Converting Errors to Optional Values  
4. Disabling Error Propagation  

###Interoperating with Objective-C  

##Resources  
Apple released two books on Swift available for free on the iBooks Store:  
[The Swift Programming Language](https://itunes.apple.com/us/book/the-swift-programming-language/id881256329?mt=11) [(*or View Online*)](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-ID203)  
[Using Swift with Cocoa and Objective-C](https://itunes.apple.com/us/book/using-swift-cocoa-objective/id888894773?mt=11)  
