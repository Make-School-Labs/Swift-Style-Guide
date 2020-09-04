# Swift Style Guide
https://google.github.io/swift/

<!-- Author Notes:
To color code: https://stackoverflow.com/questions/11509830/how-to-add-color-to-githubs-readme-md-file
    ```diff
    - text in red
    + text in green
    ! text in orange
    # text in gray
    @@ text in purple (and bold)@@
    ```
-->

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
```diff
- //⛔️⛔️⛔️
- var quotient = 11, remainder = 1
```
```swift
+ //✅✅✅
+ var quotient = 11
+ var remainder = 1

+ //⭐️⭐️⭐️
+ let (quotient, remainder) = divide(100, 9)
```

<a name="ch4.3"></a>
### [Switch Statements](#ch4TOC)

<a name="ch4.4"></a>
### [Enum Cases](#ch4TOC)

<a name="ch4.5"></a>
### [Trailing Closures](#ch4TOC)

<a name="ch4.6"></a>
### [Trailing Commas](#ch4TOC)

<a name="ch4.7"></a>
### [Numeric Literals](#ch4TOC)

<a name="ch4.8"></a>
### [Attributes](#ch4TOC)
    
------------------------------------------------------------------------------------------------------------------------

<a name="ch5"></a>
## [5. Naming](#ch5TOC)

<a name="ch5.1"></a>
### [Apple’s API Style Guidelines](#ch5TOC)

<a name="ch5.2"></a>
### [Naming Conventions Are Not Access Control](#ch5TOC)

<a name="ch5.3"></a>
### [Identifiers](#ch5TOC)

<a name="ch5.4"></a>
### [Initializers](#ch5TOC)

<a name="ch5.5"></a>
### [Static and Class Properties](#ch5TOC)

<a name="ch5.6"></a>
### [Global Constants](#ch5TOC)

<a name="ch5.7"></a>
### [Delegate Methods](#ch5TOC)
  
------------------------------------------------------------------------------------------------------------------------

<a name="ch6"></a>
## [6. Programming Practices](#ch6TOC)

<a name="ch6.1"></a>
### [Compiler Warnings](#ch6TOC)

<a name="ch6.2"></a>
### [Initializers](#ch6TOC)

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
