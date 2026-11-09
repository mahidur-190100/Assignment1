Overview

This assignment shows my understanding of core TypeScript concepts from Modules 1, 2, and 3 — including basic types, optional/default/rest parameters, readonly tuples, interfaces, type narrowing, generics, Promises, and Object-Oriented Programming.

All coding solutions are in a single file: `solutions.ts`. I also wrote two blog posts on TypeScript topics.


What I Solved

- **multiplyValue** — A function that multiplies a number by an optional multiplier, defaulting to 2. Handled 0 correctly using a default parameter instead of || 2.
- **processInput** — Accepts string | number |  and returns a formatted result using typeof type narrowing.
- **formatCoordinate** — Takes a readonly [number, number, string] tuple and returns a formatted location string without mutation.
- **concatenateArrays** — A generic function using rest parameters (...arrays: T[][]) to combine multiple arrays of the same type.
- **Course + getPopularCourses** — An interface and a function that filters published courses by minimum students without mutating the original array.
- **pluckValues** — A type-safe generic function using <T, K extends keyof T> to extract values of a specific key from an array of objects.
- **Employee & Manager** — Two classes showing inheritance, protected/private access modifiers, and super().
- **validateAgeAsync** — An async function returning Promise<string> that resolves after 1 second or rejects with an Error.



Blog Posts

Difference between any, unknown, and never, and why unknown is safer 
How public, privat`, protected, and readonly work in TypeScript OOP 

Each blog follows the required structure: Title, Introduction, Body with Code Examples, and Conclusion. Both stay within the 150–300 word range.

