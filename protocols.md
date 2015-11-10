#Protocols  

Swift Protocols are similar to Protocols in Objective-C. As the Swift book says, a Protocol "defines a blueprint of methods, properties, and other requirements that suit a particular task or piece of functionality".  

```
protocol MyProtocol {
}
```

If a class conforms to a Protocol, then the class must implement the required characteristics defined by the Protocol (i.e. methods and properties).  

To declare that a type conforms to a protocol, add the protocol after the class name separated by a comma. Protocols should be placed after the SuperClass name.  

```
class MyClass: SuperClass, MyProtocol {
}
```

Protocols are in important part of the delegate pattern used throughout iOS.
