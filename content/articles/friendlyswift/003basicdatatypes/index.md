---
title: "De Principiante a Desarrollador iOS | Tipos de datos en Swift"
description: "Introduction to Swift's type system fundamentals. Learn type inference, explicit type annotations, and the foundation of Swift's type safety approach."
date: 2025-09-07T12:00:00-06:00
lastmod: 2025-09-07T12:00:00-06:00
draft: false
author: "FriendlySwift Team"
categories: 
  - "Programming"
  - "iOS Development"
  - "Swift"
  - "Computer Science"
tags:
  - "Swift"
  - "Data Types"
  - "Type System"
  - "Type Safety"
  - "Programming Fundamentals"
  - "iOS Development"
---

{{< youtubeLite id="jQK8gNntcYo" label="De Principiante a Desarrollador iOS | Swift DataTypes and TypeSafety" >}}

Type systems form the backbone of modern programming languages, providing structure, safety, and performance optimization. Swift's type system combines the flexibility needed for rapid development with the safety guarantees required for production applications. This introduction covers the fundamental concepts that underpin all data types in Swift.


## Learning Objectives

By the end of this tutorial, you will understand:

- What type safety means in Swift programming
- How Swift's type inference system works
- When and why to use explicit type annotations
- The foundation concepts for all Swift data types
- How type safety prevents common programming errors

## Understanding Type Safety

Swift is a statically typed language, meaning that every variable and constant must have a specific type that is determined at compile time. This approach prevents many common runtime errors and enables powerful compiler optimizations.

### The Benefits of Type Safety

Type safety provides several critical advantages:

- **Error Prevention**: Catches type-related errors before your app runs
- **Performance Optimization**: Enables compiler optimizations for better performance
- **Code Clarity**: Makes code intentions explicit and easier to understand
- **Tool Support**: Enables better autocomplete and refactoring in development environments

```swift
// Type safety prevents this kind of error:
let age = 25
let name = "John"
// let result = age + name  // Compiler error - cannot add Int and String
```

## Type Inference System

Swift can automatically determine the type of a variable or constant based on the value you assign to it. This feature, called type inference, reduces code verbosity while maintaining type safety.

### How Type Inference Works

When you declare a variable or constant without specifying a type, Swift examines the initial value and infers the appropriate type:

```swift
let message = "Hello, Swift"        // Swift infers: String
let count = 42                      // Swift infers: Int
let price = 29.99                   // Swift infers: Double
let isAvailable = true              // Swift infers: Bool
```

### Type Inference Rules

Swift follows specific rules when inferring types:

```swift
// Integer literals default to Int
let wholeNumber = 100               // Type: Int

// Decimal literals default to Double
let decimalNumber = 3.14            // Type: Double

// String literals are always String
let text = "Programming"            // Type: String

// Boolean literals are always Bool
let flag = false                    // Type: Bool
```

## Explicit Type Annotations

While type inference is convenient, there are situations where explicitly declaring types is beneficial or necessary.

### When to Use Explicit Type Annotations

```swift
// When you want a specific type different from the default
let preciseValue: Float = 3.14      // Float instead of Double
let smallNumber: Int8 = 42          // Int8 instead of Int

// When declaring without immediate initialization
var userInput: String              // Will be assigned later
var itemCount: Int                 // Will be calculated later

// For clarity in complex code
let conversionRate: Double = 1.2345 // Makes intent clear
```

### Syntax for Explicit Type Annotations

The syntax for explicit type annotation follows this pattern:

```swift
let identifier: TypeName = value
var identifier: TypeName = value
```

Examples in practice:

```swift
let userName: String = "developer"
let userAge: Int = 28
let accountBalance: Double = 1500.75
let isPremiumMember: Bool = true
```

## Swift's Fundamental Data Types

Swift provides several built-in types that serve as the foundation for all data representation:

### The Core Types

```swift
// String - for text and characters
let applicationName: String = "MyApp"

// Int - for whole numbers
let maxUsers: Int = 1000

// Double - for decimal numbers (default for decimals)
let version: Double = 2.1

// Bool - for true/false values
let isActive: Bool = true
```

### Type Consistency

Once a type is established (either through inference or annotation), it cannot be changed:

```swift
var counter = 0                     // Type: Int
counter = 10                        // Valid - same type
// counter = "ten"                  // Error - cannot change type
```

## Best Practices

### When to Use Type Inference

Use type inference when:
- The type is obvious from the context
- You're using standard default types
- Code remains clear and readable

```swift
// Good use of type inference
let username = "john_doe"           // Obviously a String
let itemCount = 42                  // Obviously an Int
let isLoggedIn = false              // Obviously a Bool
```

### When to Use Explicit Types

Use explicit type annotations when:
- You need a specific type variant
- The variable is declared without initialization
- Clarity is important for complex code

```swift
// Good use of explicit types
let precision: Float = 3.14         // Want Float, not Double
var result: String                  // Will assign later
let timeout: Double = 30            // Clarity for configuration
```

## Error Prevention Through Type Safety

Type safety helps prevent common programming errors:

```swift
// These would cause compile-time errors:
let age = 25
let name = "Alice"

// Error: Cannot convert value of type 'String' to expected argument type 'Int'
// let result = age + name

// Error: Cannot assign value of type 'String' to type 'Int'
// age = "twenty-five"

// Correct approach requires explicit intention:
let ageString = String(age)         // Convert Int to String
let message = "Age: " + ageString   // Now we can concatenate
```


## Key Takeaways

1. **Type safety prevents runtime errors** by catching mistakes at compile time
2. **Type inference reduces verbosity** while maintaining safety
3. **Explicit type annotations provide control** when specific types are needed
4. **Consistency is enforced** - types cannot change after declaration
5. **Swift's type system balances safety and convenience** for productive development

These concepts form the foundation for all data manipulation in Swift, enabling you to write safer, more reliable iOS applications.

---

**[Previous: Variables and Constants](../variables-constants/)** | **[Next: String Deep Dive](../strings/)**

## Additional Resources

- [Swift Language Guide - The Basics](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html)
- [Apple Developer Documentation - Swift Types](https://developer.apple.com/documentation/swift)

*This tutorial is part of a comprehensive Swift programming series designed for developers seeking to master iOS development fundamentals.*