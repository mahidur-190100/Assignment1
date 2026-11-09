Introduction

Access modifiers are like door locks in your code. They decide who can see or change data. TypeScript has four: public, private, protected, and readonly. They keep your code safe and clean.

Body
public — open to everyone
By default, all properties and methods are public. They can be accessed from anywhere.

typescript
class User {
  public name: string; // 'public' is optional here
  constructor(name: string) {
    this.name = name;
  }
}

private — only inside the class
private members are accessible only within the class itself not from outside or subclasses.

typescript
class BankAccount {
  private balance: number = 0;
  deposit(amount: number) {
    this.balance += amount; // works inside
  }
}
// account.balance = 9999; // Error

protected — class and subclasses
protected members are accessible within the class and its subclasses, but not from outside.

typescript
class Animal {
  protected sound = "sound";
}
class Dog extends Animal {
  speak() {
    return `I make a ${this.sound}`; //accessible in subclass
  }
}

readonly — set once, never changed
readonly means a property can be assigned once but cannot be modified afterward.

typescript
class Config {
  readonly apiKey: string;
  constructor(key: string) {
    this.apiKey = key; // set once
  }
}
// config.apiKey = "new"; //  Error
Note that readonly can be combined with private or public—it controls mutation, not visibility.

Conclusion

In short: public = everyone, private = own class only, protected = class and subclasses, readonly = set once and locked. These modifiers enforce encapsulation and reduce accidental data changes—essential for good OOP design.

