---
name: programming-languages
description: Master multiple programming languages including Python, JavaScript, Java, Go, Rust, and more. Learn language-specific paradigms, syntax patterns, and problem-solving approaches. Use when learning new programming languages or comparing language features.
---

# Programming Languages Skill

## Quick Start

Learn to compare and master programming languages:

### JavaScript - Modern Web Language
```javascript
// Modern ES6+ JavaScript
const greet = (name) => {
    return `Hello, ${name}!`;
};

// Promise-based async
const fetchData = async () => {
    try {
        const response = await fetch('/api/data');
        const data = await response.json();
        return data;
    } catch (error) {
        console.error('Error:', error);
    }
};

// Destructuring & spread
const { name, age } = user;
const newUser = { ...user, age: 30 };
```

### Python - Versatile & Readable
```python
# Python simplicity
def greet(name):
    return f"Hello, {name}!"

# List comprehension
squares = [x**2 for x in range(10)]

# Async/await
async def fetch_data():
    async with httpx.AsyncClient() as client:
        response = await client.get('/api/data')
        return response.json()

# Decorators
@cache
def expensive_function():
    return compute()
```

### Java - Enterprise Solid
```java
// Java's type-safe approach
public class User {
    private String name;
    private int age;

    public User(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Streams API
    List<String> names = users.stream()
        .filter(u -> u.getAge() > 18)
        .map(User::getName)
        .collect(Collectors.toList());
}
```

### Rust - Systems Safety
```rust
// Rust's ownership system
fn main() {
    let name = String::from("World");
    greet(&name);  // Borrowing
    println!("{}", name);  // Still valid
}

// Pattern matching
match result {
    Ok(value) => println!("{}", value),
    Err(e) => println!("Error: {}", e),
}
```

## Language Comparison Guide

### Choose Your Language

| Language | Best For | Learning Curve | Job Market |
|----------|----------|----------------|-----------|
| JavaScript | Web & Full Stack | Easy | Very High |
| Python | Data Science, Backend | Easy | Very High |
| TypeScript | Type-safe JavaScript | Medium | High |
| Java | Enterprise Apps | Medium | High |
| Go | Backend Services | Easy-Medium | Growing |
| Rust | Systems Programming | Hard | Growing |
| C++ | High Performance | Hard | High |

## Core Programming Concepts

### Variables & Types
- Primitive types (int, float, string, boolean)
- Type systems (static vs dynamic)
- Type inference
- Type conversion

### Control Flow
- Conditionals (if/else, switch)
- Loops (for, while, do-while)
- Functions/Methods
- Pattern matching

### Object-Oriented Programming
- Classes & Objects
- Inheritance & Composition
- Polymorphism
- Encapsulation & Access Control

### Functional Programming
- First-class functions
- Higher-order functions
- Closures
- Immutability & Pure functions
- Functional data structures

### Data Structures
- Arrays & Lists
- Dictionaries/Hash Maps
- Sets
- Stacks & Queues
- Trees & Graphs

## Programming Paradigms

### Imperative (How to do it)
- JavaScript, Python, Java, C++

### Functional (What to do)
- Lisp, Scheme, Haskell, Erlang
- Multi-paradigm: JavaScript, Python, Java, Rust

### Object-Oriented (Objects & Classes)
- Java, C++, Python, C#

### Declarative (What should be)
- SQL, HTML, CSS
- Part of most languages

## Design Patterns

### Creational
- Singleton, Factory, Builder

### Structural
- Adapter, Decorator, Facade, Proxy

### Behavioral
- Observer, Strategy, Command, State

## Best Practices Across Languages

### Code Quality
- Clear, descriptive names
- DRY (Don't Repeat Yourself)
- SOLID principles
- Comments for WHY not WHAT
- Consistent style

### Error Handling
- Try/catch/finally
- Custom exceptions
- Error logging
- Graceful degradation

### Testing
- Unit tests
- Integration tests
- Test-driven development (TDD)
- Mocking & fixtures

## Practice Strategy

1. **Choose Primary Language** - Start with one
2. **Master Fundamentals** - Syntax, data structures, control flow
3. **Practice Daily** - Small coding challenges
4. **Build Projects** - Real-world applications
5. **Read Code** - Learn from others
6. **Learn Secondary Languages** - Easier after first
7. **Understand Paradigms** - Functional, OOP, etc.

## Advanced Topics

### Concurrency & Parallelism
- Threads & processes
- Async/await
- Promises/futures
- Channels & message passing
- Actor model (Erlang, Akka)

### Memory Management
- Stack vs Heap
- Garbage collection
- Memory leaks
- Reference counting
- Ownership (Rust)

### Performance Optimization
- Profiling
- Algorithm optimization
- Big O complexity
- Caching strategies

## When to Use This Skill

### Common Scenarios
- Learning a new language
- Comparing language features
- Understanding paradigms
- Solving language-specific problems
- Interview preparation
- Cross-language development

## Resources

- **Language-Specific Docs** - Official documentation
- **LeetCode/HackerRank** - Algorithm practice
- **Project Euler** - Mathematical problems
- **GitHub** - Learning from real code
- **Exercism** - Language learning exercises
