#Flow of Control  

Swift includes [control flow](https://en.wikipedia.org/wiki/Control_flow)   structures just like other languages to determine where the program's next line of execution should proceed.  

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
