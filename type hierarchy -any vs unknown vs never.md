Introduction
TypeScript has three special types any, unknown, and never. They look similar but work very differently. Many developers use any to stop type errors but this hides bugs. This post explains the difference in simple words.

Body

any — Don't check me
any means TypeScript stops checking the value. Even wrong code compiles.

example- 
let data: any = 5;
data.toUpperCase(); // no error but crashes run time


unknown — the safe alternative
unknown also accepts any value, but you must check its type before using it.

typescript
let data: unknown = "hello";
 data.toUpperCase(); // Error: Object is of type unknown

if (typeof data === "string") {
  data.toUpperCase(); // it works now 
}
For data from APIs or JSON, unknown is the right choice—it forces you to validate before acting.

never — "This can never happen"
never means a value that can never exist. A function that always throws returns never.

typescript
function fail(msg: string): never {
  throw new Error(msg);
}
never is also useful for exhaustive checks—ensuring every case in a union is handled.

Conclusion
Remember it simply: any = don't check which might be dangerous, unknown = check before use which is safe, never = nothing (impossible). In real projects, avoid any and prefer unknown to keep your code safe and bug-free.