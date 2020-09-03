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
    - [String Literals]](#ch1.6)


<a name="ch2TOC"></a>

2. [Source File Structure](#ch2)
    - [File Comments](#ch2.1)
    - [Import Statements](#ch2.2)
    - [Type, Variable, and Function Declarations](#ch2.3)
    - [Overloaded Declarations](#ch2.4)
    - [Extensions](#ch2.5)
    
    
<a name="ch2TOC"></a>

3.[ General Formatting](#ch3)
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

<a name="tablesWithAlignment"></a>


## [1. Source File Basics](#ch1TOC)
### [File Names](#ch1TOC)
### [File Encoding](#ch1TOC)
### [Whitespace Characters](#ch1TOC)
### [Special Escape Sequences](#ch1TOC)
### [Invisible Characters and Modifiers](#ch1TOC)
### [String Literals](#ch1TOC)

------------------------------------------------------------------------------------------------------------------------

## [2. Source File Structure](#ch2TOC)
### [File Comments](#ch2TOC)
### [Import Statements](#ch2TOC)
### [Type, Variable, and Function Declarations](#ch2TOC)
### [Overloaded Declarations](#ch2TOC)
### [Extensions](#ch2TOC)
    
------------------------------------------------------------------------------------------------------------------------

## [3. General Formatting](#ch3TOC)
### [Column Limit](#ch3TOC)
### [Braces](#ch3TOC)
### [Semicolons](#ch3TOC)
### [One Statement Per Line](#ch3TOC)
### [Line-Wrapping](#ch3TOC)
    ### [Function Declarations](#ch3TOC)
    ### [Type and Extension Declarations](#ch3TOC)
    ### [Function Calls](#ch3TOC)
    ### [Control Flow Statements](#ch3TOC)
    ### [Other Expressions](#ch3TOC)
### [Horizontal Whitespace](#ch3TOC)
### [Horizontal Alignment](#ch3TOC)
### [Vertical Whitespace](#ch3TOC)
### [Parentheses](#ch3TOC)
    
------------------------------------------------------------------------------------------------------------------------

## [4. Formatting Specific Constructs](#ch4TOC)
### [Non-Documentation Comments](#ch4TOC)
### [Properties](#ch4TOC)
### [Switch Statements](#ch4TOC)
### [Enum Cases](#ch4TOC)
### [Trailing Closures](#ch4TOC)
### [Trailing Commas](#ch4TOC)
### [Numeric Literals](#ch4TOC)
### [Attributes](#ch4TOC)
    
------------------------------------------------------------------------------------------------------------------------

## [5. Naming](#ch5TOC)
### [Apple’s API Style Guidelines](#ch5TOC)
### [Naming Conventions Are Not Access Control](#ch5TOC)
### [Identifiers](#ch5TOC)
### [Initializers](#ch5TOC)
### [Static and Class Properties](#ch5TOC)
### [Global Constants](#ch5TOC)
### [Delegate Methods](#ch5TOC)
  
------------------------------------------------------------------------------------------------------------------------

## [6. Programming Practices](#ch6TOC)
### [Compiler Warnings](#ch6TOC)
### [Initializers](#ch6TOC)
### [Properties](#ch6TOC)
### [Types with Shorthand Names](#ch6TOC)
### [Optional Types](#ch6TOC)
### [Error Types](#ch6TOC)
### [Force Unwrapping and Force Casts](#ch6TOC)
### [Implicitly Unwrapped Optionals](#ch6TOC)
### [Access Levels](#ch6TOC)
### [Nesting and Namespacing](#ch6TOC)
### [guards for Early Exits](#ch6TOC)
### [for-where Loops](#ch6TOC)
### [fallthrough in switch Statements](#ch6TOC)
### [Pattern Matching](#ch6TOC)
### [Tuple Patterns](#ch6TOC)
### [Numeric and String Literals](#ch6TOC)
### [Playground Literals](#ch6TOC)
### [Trapping vs. Overflowing Arithmetic](#ch6TOC)
### [Defining New Operators](#ch6TOC)
### [Overloading Existing Operators](#ch6TOC)

------------------------------------------------------------------------------------------------------------------------

## [7. Documentation Comments](#ch7TOC)
### [General Format](#ch7TOC)
### [Single-Sentence Summary](#ch7TOC)
### [Parameter, Returns, and Throws Tags](#ch7TOC)
### [Apple’s Markup Format](#ch7TOC)
### [Where to Document](#ch7TOC)

------------------------------------------------------------------------------------------------------------------------
