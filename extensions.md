#Extensions  

Extensions are the equivalent to categories in Objective-C and are used to add additional functionality to a class. However in Swift, extensions can also be used to extend structures, enums and protocols.  

Extensions are simply to declare:  
```
class Language {
  // Base class
  var name: String
  var languageFamily: String
}

extension Language {
}
```

They can be used to add protocol conformance:  
```
// Add protocol conformance
extension Language: TextToSpeechProtocol {

  // Add computed properties
  var description: String { return "\(self.name) from the language family \(self.languageFamily)"}

  // Add new methods
  func translate(string: String, from language: Language) -> String {
    ...
    return translatedString
  }
}
```


**Previous**: [Classes](classes.md)  
**Next**: [Protocols](protocols.md)  
Return to the [homepage](README.md).
