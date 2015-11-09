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

###Switch Cases  
An important difference between Swift's switch statements and traditional switch statments is that 'break's are not required to prevent fall-through from one case to the next. Instead multiple cases can be matched simulataneously:  
```
switch person.position {
case Job.BusinessAnalyst:
    print("What's needed?")
case Job.Designer:
    print("Make pretty things")
case Job.Developer:
    print("Let's code!")
case Job.ProductManager, Job.ProjectManager, Job.ScrumMaster:
    print("Is the code done yet?")
default:
    print("I need a job...")
}
```

Swift's switch case control flow statement is exhaustive, meaning that every case needs to be considered either explictly or via the 'default' catch-all.  

###Control Transfers  

Control transfer statements include **break**, **continue**, and **return** work just like they do in most programming languages. **Break** leaves the current control-flow statement, **continue** return to the first line of the control-flow statement instead of leaving it entirely, and **return** returns from the current function with an optional value.


For more information about control flow in Swift, including special handling of Tuples in switch statements and labeled statments check out the chapter on [Control Flow](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html) in Apple's Swift Book.  
