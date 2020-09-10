# Swift Style Guide
https://google.github.io/swift/

## Table of Contents:

<a name="ch1TOC"></a>

1. [Source File Basics](#ch1)
    - [File Names](#ch1.1)
    - [File Encoding](#ch1.2)
    - [Whitespace Characters](#ch1.3)
    - [Special Escape Sequences](#ch1.4)
    - [Invisible Characters and Modifiers](#ch1.5)
    - [String Literals](#ch1.6)


<a name="ch2TOC"></a>

2. [Source File Structure](#ch2)
    - [File Comments](#ch2.1)
    - [Import Statements](#ch2.2)
    - [Type, Variable, and Function Declarations](#ch2.3)
    - [Overloaded Declarations](#ch2.4)
    - [Extensions](#ch2.5)
    
    
<a name="ch2TOC"></a>

3. [ General Formatting](#ch3)
    - [Column Limit](#ch3.1)
    - [Braces](#ch3.2)
    - [Semicolons](#ch3.3)
    - [One Statement Per Line](#ch3.4)
    - [Line-Wrapping](#ch3.5)
        - [Function Declarations](#ch3.5.1)
        - [Type and Extension Declarations](#ch3.5.2)
        - [Function Calls](#ch3.5.3)
        - [Control Flow Statements](#ch3.5.4)
        - [Other Expressions](#ch3.5.5)
    - [Horizontal Whitespace](#ch3.6)
    - [Horizontal Alignment](#ch3.7)
    - [Vertical Whitespace](#ch3.8)
    - [Parentheses](#ch3.9)
    
    
<a name="ch3TOC"></a>

4. [Formatting Specific Constructs](#ch4)
    - [Non-Documentation Comments](#ch4.1)
    - [Properties](#ch4.2)
    - [Switch Statements](#ch4.3)
    - [Enum Cases](#ch4.4)
    - [Trailing Closures](#ch4.5)
    - [Trailing Commas](#ch4.6)
    - [Numeric Literals](#ch4.7)
    - [Attributes](#ch4.8)
    
    
<a name="ch4TOC"></a>

5. [Naming](#ch5)
    - [Apple’s API Style Guidelines](#ch5.1)
    - [Naming Conventions Are Not Access Control](#ch5.2)
    - [Identifiers](#ch5.3)
    - [Initializers](#ch5.4)
    - [Static and Class Properties](#ch5.5)
    - [Global Constants](#ch5.6)
    - [Delegate Methods](#ch5.7)
    
    
<a name="ch6TOC"></a>

6. [Programming Practices](#ch6)
    - [Compiler Warnings](#ch6.1)
    - [Initializers](#ch6.2)
    - [Properties](#ch6.3)
    - [Types with Shorthand Names](#ch6.4)
    - [Optional Types](#ch6.5)
    - [Error Types](#ch6.6)
    - [Force Unwrapping and Force Casts](#ch6.7)
    - [Implicitly Unwrapped Optionals](#ch6.8)
    - [Access Levels](#ch6.9)
    - [Nesting and Namespacing](#ch6.10)
    - [guards for Early Exits](#ch6.11)
    - [for-where Loops](#ch6.12)
    - [fallthrough in switch Statements](#ch6.13)
    - [Pattern Matching](#ch6.14)
    - [Tuple Patterns](#ch6.15)
    - [Numeric and String Literals](#ch6.16)
    - [Playground Literals](#ch6.17)
    - [Trapping vs. Overflowing Arithmetic](#ch6.18)
    - [Defining New Operators](#ch6.19)
    - [Overloading Existing Operators](#ch6.20)
    
    
<a name="ch7TOC"></a>

7. [Documentation Comments](#ch7)
    - [General Format](#ch7.1)
    - [Single-Sentence Summary](#ch7.2)
    - [Parameter, Returns, and Throws Tags](#ch7.3)
    - [Apple’s Markup Format](#ch7.4)
    - [Where to Document](#ch7.5)


------------------------------------------------------------------------------------------------------------------------



<a name="ch1"></a>
## [1. Source File Basics](#ch1TOC)

<a name="ch1.1"></a>
### [File Names](#ch1TOC)

<a name="ch1.2"></a>
### [File Encoding](#ch1TOC)

<a name="ch1.3"></a>
### [Whitespace Characters](#ch1TOC)

<a name="ch1.4"></a>
### [Special Escape Sequences](#ch1TOC)

<a name="ch1.5"></a>
### [Invisible Characters and Modifiers](#ch1TOC)

<a name="ch1.6"></a>
### [String Literals](#ch1TOC)

------------------------------------------------------------------------------------------------------------------------

<a name="ch2"></a>
## [2. Source File Structure](#ch2TOC)

<a name="ch2.1"></a>
### [File Comments](#ch2TOC)

<a name="ch2.2"></a>
### [Import Statements](#ch2TOC)

<a name="ch2.3"></a>
### [Type, Variable, and Function Declarations](#ch2TOC)

<a name="ch2.4"></a>
### [Overloaded Declarations](#ch2TOC)

<a name="ch2.5"></a>
### [Extensions](#ch2TOC)
    
------------------------------------------------------------------------------------------------------------------------

<a name="ch3"></a>
## [3. General Formatting](#ch3TOC)

<a name="ch3.1"></a>
### [Column Limit](#ch3TOC)

<a name="ch3.2"></a>
### [Braces](#ch3TOC)

<a name="ch3.3"></a>
### [Semicolons](#ch3TOC)

<a name="ch3.4"></a>
### [One Statement Per Line](#ch3TOC)

<a name="ch3.5"></a>
### [Line-Wrapping](#ch3TOC)

<a name="ch3.5.1"></a>
### [Function Declarations](#ch3TOC)

<a name="ch3.5.2"></a>
### [Type and Extension Declarations](#ch3TOC)

<a name="ch3.5.3"></a>
### [Function Calls](#ch3TOC)

<a name="ch3.5.4"></a>
### [Control Flow Statements](#ch3TOC)

<a name="ch3.5.5"></a>
### [Other Expressions](#ch3TOC)
    
<a name="ch3.6"></a>
### [Horizontal Whitespace](#ch3TOC)

<a name="ch3.7"></a>
### [Horizontal Alignment](#ch3TOC)

<a name="ch3.8"></a>
### [Vertical Whitespace](#ch3TOC)

<a name="ch3.9"></a>
### [Parentheses](#ch3TOC)
    
------------------------------------------------------------------------------------------------------------------------

<a name="ch4"></a>
## [4. Formatting Specific Constructs](#ch4TOC)

<a name="ch4.1"></a>
### [Non-Documentation Comments](#ch4TOC)

<a name="ch4.2"></a>
### [Properties](#ch4TOC)
- Variables are not created in single line
- Local variables that are closely related are stored as a tuple instead

Ex:
```swift
//⛔️⛔️⛔️
var quotient = 11, remainder = 1
```
```swift
//✅✅✅
var quotient = 11
var remainder = 1

//⭐️⭐️⭐️
let (quotient, remainder) = divide(100, 9)
```

<a name="ch4.3"></a>
### [Switch Statements](#ch4TOC)
- Case statements are indented at the same level as the switch statement to which they belong.
- Only code block inside the cases are indented with the exception of `break`

Ex:
```swift
//⛔️⛔️⛔️
switch order {
  case .ascending:
    print("Ascending")
  case .descending:
    print("Descending")
  case .same:
    print("Same")
  default:
    break
}
```

```swift
//✅✅✅
switch order {
case .ascending:
  print("Ascending")
case .descending:
  print("Descending")
case .same:
  print("Same")
default: break
}
```


<a name="ch4.4"></a>
### [Enum Cases](#ch4TOC)
- In general, there is only one case per line in an enum. Only separate cases with a comma when enum is simple and when none of the cases have asociated values or raw values

```swift
//✅✅✅
public enum Token { //enum without associated or raw values
  case comma, semicolon, identifier
}

public enum Token {
  case comma
  case semicolon
  case identifier(String) //associated value
```
```swift
//⛔️⛔️⛔️
public enum Token {
  case comma, semicolon, identifier(String)
}
```

- When all cases of an enum are `indirect`, the enum itself is declared `indirect` and the indirect keyword is removed from all the cases.

```swift
//✅✅✅
public indirect enum DependencyGraphNode {
  case userDefined(dependencies: [DependencyGraphNode])
  case synthesized(dependencies: [DependencyGraphNode])
}
```
```swift
//⛔️⛔️⛔️
public enum DependencyGraphNode {
  indirect case userDefined(dependencies: [DependencyGraphNode])
  indirect case synthesized(dependencies: [DependencyGraphNode])
}
```

- When an `enum` case does not have associated values, empty parentheses are never present

```swift
//⛔️⛔️⛔️
public enum BinaryTree<Element> {
  indirect case node(element: Element, left: BinaryTree, right: BinaryTree)
  case empty()  // AVOID.
}
```
```swift
//✅✅✅
public enum BinaryTree<Element> {
  indirect case node(element: Element, left: BinaryTree, right: BinaryTree)
  case empty  // GOOD.
}
```


- The cases of an enum must follow a logical ordering that the author could explain.

```swift
//⛔️⛔️⛔️
public enum HTTPStatus: Int {
  case badRequest = 400
  case forbidden = 403
  case internalServerError = 500
  case notAuthorized = 401
  case notFound = 404
  case ok = 200
  case paymentRequired = 402
}
```
```swift
//✅✅✅
//Cases are arranged in numerical order and blank lines are used to separate groups
public enum HTTPStatus: Int {
  case ok = 200

  case badRequest = 400
  case notAuthorized = 401
  case paymentRequired = 402
  case forbidden = 403
  case notFound = 404

  case internalServerError = 500
}
```

<a name="ch4.5"></a>
### [Trailing Closures](#ch4TOC)
- Functions should not be overloaded that they differ only by the name of their trailing closure argument.

```swift
//⛔️⛔️⛔️
//This prohibits using trailing closure syntax to call greet
func greet(enthusiastically nameProvider: () -> String) {
  print("Hello, \(nameProvider())! It's a pleasure to see you!")
}

func greet(apathetically nameProvider: () -> String) {
  print("Oh, look. It's \(nameProvider()).")
}

greet { "John" }  // error: ambiguous use of 'greet'
```
```swift
//✅✅✅
func greetEnthusiastically(_ nameProvider: () -> String) {
  print("Hello, \(nameProvider())! It's a pleasure to see you!")
}

func greetApathetically(_ nameProvider: () -> String) {
  print("Oh, look. It's \(nameProvider()).")
}

greetEnthusiastically { "John" }
greetApathetically { "not John" }
```

- If a function call has multiple closure arguments, then *none* are called using trailing closure syntax, instead *all* are labeled and nested inside the argument list’s parentheses.
```swift
//⛔️⛔️⛔️
UIView.animate(
  withDuration: 0.5,
  animations: {
    // ...
  }) { finished in
    // ...
  }
```
```swift
//✅✅✅
UIView.animate(
  withDuration: 0.5,
  animations: {
    // ...
  },
  completion: { finished in //labeled closure arguments
    // ...
  })
```

- When a function called with trailing closure syntax takes no other arguments, empty parentheses (()) after the function name are never present.

```swift
//✅✅✅
let squares = [1, 2, 3].map { $0 * $0 }
```

```swift
//⛔️⛔️⛔️
let squares = [1, 2, 3].map({ $0 * $0 })
let squares = [1, 2, 3].map() { $0 * $0 }
```


<a name="ch4.6"></a>
### [Trailing Commas](#ch4TOC)
- Trailing commas in **array** and **dictionary literals** are required when each element is placed on its own line.

```swift
//✅✅✅
let configurationKeys = [
  "bufferSize",
  "compression",
  "encoding",                                    // GOOD.
]
```
```swift
//⛔️⛔️⛔️
let configurationKeys = [
  "bufferSize",
  "compression",
  "encoding"                                     // AVOID.
]
```


<a name="ch4.7"></a>
### [Numeric Literals](#ch4TOC)
- For readability, It is recommended but not required that long numeric literals (decimal, hexadecimal, octal, and binary) use the underscore (_) separator to group digits
- 3 digits for decimals, 4 digits for hexadecimal, 4 or 8 digits for binary literals

```swift
//⛔️⛔️⛔️
var bigInt = 50020099000
var smallDouble = 0.2340911002
var bigHex = "7BFC6FEA9"
```
```swift
//✅✅✅
var bigInt = 50_020_099_000
var smallDouble = 0.234_091_100_2
var bigHex = "7_BFC6_FEA9"
```

<a name="ch4.8"></a>
### [Attributes](#ch4TOC)
- Parameterized attributes (such as @availability(...) or @objc(...)) are each written on their own line before the declaration to which they apply, are ordered, and are indented at the same level.
```swift
//⛔️⛔️⛔️
@available(iOS 9.0, *) public func coolNewFeature() {
  // ...
}
```
```swift
//✅✅✅
@available(iOS 9.0, *)
public func coolNewFeature() {
  // ...
}
```

- Attributes without parameters (for example, @objc without arguments, `@IBOutlet`, or `@NSManaged`) may be placed on the same line
```swift
//✅✅✅
public class MyViewController: UIViewController {
  @IBOutlet private var tableView: UITableView!
}
```

------------------------------------------------------------------------------------------------------------------------

<a name="ch5"></a>
## [5. Naming](#ch5TOC)

<a name="ch5.1"></a>
### [Apple’s API Style Guidelines](#ch5TOC)


<a name="ch5.2"></a>
### [Naming Conventions Are Not Access Control](#ch5TOC)
- Do not put access control (`open`, `internal`, `fileprivate`, `private`) on model or variable names
- Open access is the highest (least restrictive) access level and private access is the lowest (most restrictive) access level.
```swift
//⛔️⛔️⛔️
struct PrivateProfile {
    var secretId: String
    ...
}
```

```swift
//✅✅✅
private struct HiddenProfile {
    var secretId: String
    ...
}
```

<a name="ch5.3"></a>
### [Identifiers](#ch5TOC)
- Identifiers should only contain [7-bit ASCII characters](https://www.sciencebuddies.org/science-fair-projects/references/ascii-table). 
- Unicode identifiers are allowed if they have a clear and legitimate meaning 
    - e.g. Greek letters that represent mathematical concepts
```swift
//✅✅✅
let smile = "😊"
let deltaX = newX - previousX
let Δx = newX - previousX
```

```swift
//⛔️⛔️⛔️
let 😊 = "😊"
```

<a name="ch5.4"></a>
### [Initializers](#ch5TOC)
- Initializer arguments that correspond directly to a stored property have the same name as the property

```swift
//⛔️⛔️⛔️
public struct Person {
  public let name: String
  public let phoneNumber: String

  // AVOID.
  public init(name otherName: String, phoneNumber otherPhoneNumber: String) {
    name = otherName
    phoneNumber = otherPhoneNumber
  }
}
```
```swift
//✅✅✅
public struct Person {
  public let name: String
  public let phoneNumber: String

  // GOOD.
  public init(name: String, phoneNumber: String) {
    self.name = name
    self.phoneNumber = phoneNumber
  }
}
```

<a name="ch5.5"></a>
### [Static and Class Properties](#ch5TOC)
- Static and class properties that return instances of the declaring type are *not suffixed* with the name of the type.
```swift
//⛔️⛔️⛔️
public class UIColor {
  public class var redColor: UIColor {           // AVOID.
    // ...
  }
}

public class URLSession {
  public class var sharedSession: URLSession {   // AVOID.
    // ...
  }
}

```
```swift
//✅✅✅
public class UIColor {
  public class var red: UIColor {                // GOOD.
    // ...
  }
}

public class URLSession {
  public class var shared: URLSession {          // GOOD.
    // ...
  }
}
```

<a name="ch5.6"></a>
### [Global Constants](#ch5TOC)
- Like other variables, global constants are **lowerCamelCase**
```swift
//⛔️⛔️⛔️
let SecondsPerMinute = 60
let kSecondsPerMinute = 60
let gSecondsPerMinute = 60
let SECONDS_PER_MINUTE = 60
```

```swift
//✅✅✅
let secondsPerMinute = 60
```

<a name="ch5.7"></a>
### [Delegate Methods](#ch5TOC)
- All methods take the delegate’s source object as the first argument

##### For methods that take the delegate’s source object as their only argument:
- If method **returns Void**
    - base name is **delegate’s source type** followed by an **indicative verb phrase** describing the event
    - argument is **unlabeled**
    ```swift
    func scrollViewDidBeginScrolling(_ scrollView: UIScrollView) //✅✅✅
    ```
- If the method **returns Bool** (such as those that make an assertion about the delegate’s source object itself), then the method’s 
    - name is the **delegate’s source type** followed by an **indicative or conditional verb phrase** describing the assertion
    - argument is **unlabeled**.
    ```swift
    func scrollViewShouldScrollToTop(_ scrollView: UIScrollView) -> Bool //✅✅✅
    ```
- If the method returns some other value 
    - base name is a **noun phrase** describing the property being queried. 
    - argument is **labeled with a preposition or phrase with a trailing preposition** that combines the noun phrase and the delegate’s source object
    ```swift
    func numberOfSections(in scrollView: UIScrollView) -> Int //✅✅✅
    ```
##### For methods that take additional arguments after the delegate’s source object, the method’s base name is the delegate’s source type by itself and the **first argument is unlabeled**. Then:
- If the method **returns Void**, 
    - the second argument is **labeled with an indicative verb phrase** describing the event that has the argument as its **direct object or prepositional object**
    ```swift
    //✅✅✅
    func tableView(
    _ tableView: UITableView,
    willDisplayCell cell: UITableViewCell,
    forRowAt indexPath: IndexPath)
    ```
- If the method **returns Bool**, 
    - the second argument is **labeled with an indicative or conditional verb phrase** that describes the return value in terms of the argument

    ```swift
    //✅✅✅
    func tableView(
      _ tableView: UITableView,
      shouldSpringLoadRowAt indexPath: IndexPath,
      with context: UISpringLoadedInteractionContext
    ) -> Bool
    ```
- If the method **returns some other value**, 
    - the second argument is **labeled with a noun phrase and trailing preposition** that describes the return value in terms of the argument
    ```swift
    //✅✅✅
    func tableView(
      _ tableView: UITableView,
      heightForRowAt indexPath: IndexPath
    ) -> CGFloat
    ```

Apple’s documentation on [delegates and data sources](https://developer.apple.com/library/content/documentation/General/Conceptual/CocoaEncyclopedia/DelegatesandDataSources/DelegatesandDataSources.html) also contains some good general guidance about such names.



------------------------------------------------------------------------------------------------------------------------

<a name="ch6"></a>
## [6. Programming Practices](#ch6TOC)

<a name="ch6.1"></a>
### [Compiler Warnings](#ch6TOC)
  
```swift
//⛔️⛔️⛔️

```

```swift
//✅✅✅

```

<a name="ch6.2"></a>
### [Initializers](#ch6TOC)
  
```swift
//⛔️⛔️⛔️

```

```swift
//✅✅✅

```

<a name="ch6.3"></a>
### [Properties](#ch6TOC)

<a name="ch6.4"></a>
### [Types with Shorthand Names](#ch6TOC)

<a name="ch6.5"></a>
### [Optional Types](#ch6TOC)

<a name="ch6.6"></a>
### [Error Types](#ch6TOC)

<a name="ch6.7"></a>
### [Force Unwrapping and Force Casts](#ch6TOC)

<a name="ch6.8"></a>
### [Implicitly Unwrapped Optionals](#ch6TOC)

<a name="ch6.9"></a>
### [Access Levels](#ch6TOC)

<a name="ch6.10"></a>
### [Nesting and Namespacing](#ch6TOC)

<a name="ch6.11"></a>
### [guards for Early Exits](#ch6TOC)

<a name="ch6.12"></a>
### [for-where Loops](#ch6TOC)

<a name="ch6.13"></a>
### [fallthrough in switch Statements](#ch6TOC)

<a name="ch6.14"></a>
### [Pattern Matching](#ch6TOC)

<a name="ch6.15"></a>
### [Tuple Patterns](#ch6TOC)

<a name="ch6.16"></a>
### [Numeric and String Literals](#ch6TOC)

<a name="ch6.17"></a>
### [Playground Literals](#ch6TOC)

<a name="ch6.18"></a>
### [Trapping vs. Overflowing Arithmetic](#ch6TOC)

<a name="ch6.19"></a>
### [Defining New Operators](#ch6TOC)

<a name="ch6.20"></a>
### [Overloading Existing Operators](#ch6TOC)


------------------------------------------------------------------------------------------------------------------------

<a name="ch7"></a>
## [7. Documentation Comments](#ch7TOC)

<a name="ch7.1"></a>
### [General Format](#ch7TOC)

<a name="ch7.2"></a>
### [Single-Sentence Summary](#ch7TOC)

<a name="ch7.3"></a>
### [Parameter, Returns, and Throws Tags](#ch7TOC)

<a name="ch7.4"></a>
### [Apple’s Markup Format](#ch7TOC)

<a name="ch7.5"></a>
### [Where to Document](#ch7TOC)

------------------------------------------------------------------------------------------------------------------------
