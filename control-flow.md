#Flow of Control  

Swift includes [control flow](https://en.wikipedia.org/wiki/Control_flow)   structures just like other languages to determine where the program's next line of execution should proceed.  

###If Statements  

If-statements are probably the most frequently used control-flow statements in any programming language and are easy to understand by even non-programmers. Swift does away with the parentheses that were required in Objective-C.  
```
if condition {
    // Continue here if condition is true
}
```

Else and else-if statements work the same way and are not required by **do** require attachment to an if-statement:  
```
if condition {
    // Continue here if condition is true
} else if anotherCondition {
    // ...otherwise if anotherCondition is true continue here
} else {
    // ...if both conditions are false, then continue here
}
```

###Traditional For-Loops  
Using Swift's syntax, the traditional for-loop should be very familiar yet seldom used in Swift because of the more powerful for-loops offered.
```
for var index = 0; index < 3; index++ {
    print("\(index)")
}
```

###For-In Loops
Swift also supports **ranges** in for-loop control-flow statements for quicker syntax than the traditional for-loops.  
```
for index in 0...3 {
    print("\(index)")
}
```

For-loops can be used to iterate over items in a collection without an index:  
```
for person in organization {
    print("\(person.name)")
}
```

The index can also be simultaneously retrieved in the for-in loop using a tuple:  
```
for (index, person) in organization {
    print("\(person.name) is employe number \(index)")
}
```

###Repeat and Repeat-While  

Roughly equivalent to traditional do and do-while loops, Swift's repeat and repeat-while offers looping based on a single condition.  

```
// Drink only if thirsty (0 or more times)
while person.thirsty {
    person.drink()
}

// Eat at least once, even if not hungry (1 or more times)
repeat {
    person.eat()
} while person.hungry
```

