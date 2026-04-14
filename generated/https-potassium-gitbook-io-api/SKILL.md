---
name: potassium
description: Use this skill when working with Potassium. Triggers when user mentions Potassium or imports from it.
---

# Potassium

## What this is
Potassium is a library that provides a simple and efficient way to work with data. It allows users to easily manipulate and analyze data using a variety of tools and methods. With Potassium, users can perform tasks such as data cleaning, filtering, and transformation.

## Installation
```bash
npm install @potassium/core
```

## Key concepts
The most important APIs and patterns in Potassium include:
* **Atoms**: The basic building blocks of data in Potassium, which can be used to store and manipulate individual values.
* **Molecules**: Collections of atoms that can be used to represent more complex data structures.
* **Reactions**: Functions that take in atoms or molecules and produce new values.

Example:
```javascript
import { atom } from '@potassium/core';

const counter = atom(0);

console.log(counter.get()); // Output: 0
```

## Correct usage patterns
Here are some examples of correct usage patterns in Potassium:
* Creating and updating atoms:
```javascript
import { atom } from '@potassium/core';

const counter = atom(0);

counter.set(1);
console.log(counter.get()); // Output: 1
```
* Using reactions to transform data:
```javascript
import { molecule, reaction } from '@potassium/core';

const data = molecule({ name: 'John', age: 30 });

const greeting = reaction(data, (data) => `Hello, ${data.name}!`);

console.log(greeting.get()); // Output: Hello, John!
```

## Common mistakes to avoid
Some common mistakes to avoid when using Potassium include:
* Not properly updating atoms and molecules, leading to stale data.
* Not handling errors and exceptions properly, leading to unexpected behavior.

## File and folder conventions
Potassium projects typically follow standard JavaScript naming conventions and folder structures. Configuration files, such as `package.json`, should be placed in the root of the project.