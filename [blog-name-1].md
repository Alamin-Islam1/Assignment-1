
# Type vs Interface in TypeScript

## Introduction

TypeScript provides two powerful ways to define object structures: `type` aliases and `interface`. Both help developers define the shape of data and improve code readability. However, they have some important differences.

## Detailed Explanation

### 1. What is an Interface?

An interface is mainly used to describe the structure of objects. It defines which properties and types an object should contain. Interfaces also support declaration merging.

Example:

```typescript
interface User {
  name: string;
  age: number;
}

interface User {
  email: string;
}

const user: User = {
  name: "Al-Amin",
  age: 22,
  email: "alamin@example.com"
};
```

In this example, TypeScript combines both interface declarations into one structure.

### 2. What is a Type Alias?

A type alias allows developers to create custom names for different types. It supports objects, unions, intersections, primitive types, and tuples.

Example:

```typescript
type User = {
  name: string;
  age: number;
};

type Status = "active" | "inactive";

type UserWithStatus = User & {
  status: Status;
};
```

Here, the type alias combines object properties and a union type.

### 3. Core Differences

- Interface supports declaration merging, but type aliases do not.
- Interface is commonly used for object structures.
- Type aliases support union and intersection types.
- Both support inheritance-like extension through `extends` or intersections.
- Both provide type safety and improve code maintainability.

### 4. When Should You Choose One?

Use interfaces when defining object structures, class contracts, and public APIs. Use type aliases when creating union types, tuples, intersections, and more complex type definitions.

## Conclusion

Both `type` and `interface` are useful TypeScript features. Choosing the right one depends on project requirements. Understanding their differences helps developers write cleaner, reusable, and maintainable code.
