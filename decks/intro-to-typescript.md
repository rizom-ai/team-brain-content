---
title: TypeScript Introduction
description: Learn TypeScript basics and best practices
author: Recall Team
---

# Welcome to TypeScript

A comprehensive introduction to TypeScript fundamentals

---

## What is TypeScript?

- **Superset of JavaScript** - All valid JavaScript is valid TypeScript
- **Static Type Checking** - Catch errors before runtime
- **Enhanced IDE Support** - Better autocomplete and refactoring
- **Compiles to JavaScript** - Works anywhere JavaScript runs

---

## Why TypeScript?

### Benefits

- 🛡️ **Type Safety** - Prevent common bugs
- 📚 **Better Documentation** - Types serve as inline docs
- 🔧 **Improved Tooling** - Enhanced IDE features
- 🚀 **Scalability** - Easier to maintain large codebases

---

## Getting Started

### Installation

```bash
npm install -g typescript
```

### Your First TypeScript File

```typescript
function greet(name: string): string {
  return `Hello, ${name}!`;
}

console.log(greet("World"));
```

---

## Basic Types

```typescript
// Primitives
let isDone: boolean = false;
let count: number = 42;
let message: string = "Hello";

// Arrays
let numbers: number[] = [1, 2, 3];
let names: Array<string> = ["Alice", "Bob"];

// Objects
interface Person {
  name: string;
  age: number;
}
```

---

## Functions

```typescript
// Function with typed parameters and return type
function add(a: number, b: number): number {
  return a + b;
}

// Optional parameters
function greet(name: string, greeting?: string): string {
  return `${greeting || "Hello"}, ${name}!`;
}

// Arrow functions
const multiply = (a: number, b: number): number => a * b;
```

---

## Interfaces

```typescript
interface User {
  id: number;
  name: string;
  email: string;
  isAdmin?: boolean;  // Optional property
}

function createUser(user: User): void {
  console.log(`Creating user: ${user.name}`);
}
```

---

## Type Aliases

```typescript
// Union types
type Status = "pending" | "active" | "inactive";

// Intersection types
type Admin = User & {
  permissions: string[];
};

// Generic types
type Result<T> = {
  success: boolean;
  data?: T;
  error?: string;
};
```

---

## Classes

```typescript
class Animal {
  constructor(public name: string) {}

  speak(): void {
    console.log(`${this.name} makes a sound`);
  }
}

class Dog extends Animal {
  speak(): void {
    console.log(`${this.name} barks`);
  }
}
```

---

## Generics

```typescript
// Generic function
function identity<T>(arg: T): T {
  return arg;
}

// Generic interface
interface Container<T> {
  value: T;
  getValue(): T;
}

// Usage
const numberContainer: Container<number> = {
  value: 42,
  getValue() { return this.value; }
};
```

---

## Best Practices

1. **Enable strict mode** in tsconfig.json
2. **Avoid `any`** - Use unknown or proper types
3. **Use interfaces** for object shapes
4. **Leverage type inference** - Don't over-annotate
5. **Write tests** - TypeScript doesn't replace testing

---

## Resources

- 📖 [Official TypeScript Handbook](https://www.typescriptlang.org/docs/)
- 🎓 [TypeScript Deep Dive](https://basarat.gitbook.io/typescript/)
- 💻 [TypeScript Playground](https://www.typescriptlang.org/play)
- 📺 [TypeScript YouTube Channel](https://www.youtube.com/c/typescript)

---

## Thank You!

**Questions?**

Happy coding with TypeScript! 🎉
