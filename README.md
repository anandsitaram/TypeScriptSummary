# TypeScript Overview

This document provides a comprehensive overview of TypeScript features, including data types, interfaces, classes, enums, and functions. TypeScript is a typed superset of JavaScript that adds optional static typing and other features to enhance the development experience.

## Characteristics of TypeScript

- **Synchronous & Single-threaded:** Executes code sequentially and processes one command at a time.
- **Weakly Typed:** Data types can change dynamically.
- **Object-oriented:** Supports object-oriented programming principles.
- **Versatile:** Runs in browsers, on computers, and servers.

## Data Types

TypeScript supports various data types, including:

- **String:** Textual data.
- **Number:** Numeric values.
- **BigInt:** Large integers.
- **Boolean:** True or false values.
- **Undefined:** A variable that has been declared but not assigned a value.
- **Null:** A variable that intentionally has no value.
- **Symbol:** A unique and immutable value used as an identifier.
- **Object:** A complex data structure.

### Example of Data Types

```typescript
type DataType = string | number | bigint | boolean | undefined | null | symbol | object;

const dataTypes: DataType[] = [
    "String",
    42,
    BigInt(9007199254740991),
    true,
    undefined,
    null,
    Symbol('symbol'),
    {}
];
Enums
Enums allow you to define a set of named constants, which can be used to represent a collection of related values.

Example of Enum
enum UserRole {
    Admin,
    User,
    Guest
}

const role: UserRole = UserRole.Admin;
console.log(role); // Output: 0 (index of Admin)
Interfaces
Interfaces define the structure of an object, specifying the types of its properties and methods.

Example of Interface
interface Person {
    name: string;
    age: number;
    isEligible: boolean;
    greet(): void;
}

Sure! Here’s the complete content in a single README.md file format, including all the sections and examples:

markdown
Copy code
# TypeScript Overview

This document provides a comprehensive overview of TypeScript features, including data types, interfaces, classes, enums, and functions. TypeScript is a typed superset of JavaScript that adds optional static typing and other features to enhance the development experience.

## Characteristics of TypeScript

- **Synchronous & Single-threaded:** Executes code sequentially and processes one command at a time.
- **Weakly Typed:** Data types can change dynamically.
- **Object-oriented:** Supports object-oriented programming principles.
- **Versatile:** Runs in browsers, on computers, and servers.

## Data Types

TypeScript supports various data types, including:

- **String:** Textual data.
- **Number:** Numeric values.
- **BigInt:** Large integers.
- **Boolean:** True or false values.
- **Undefined:** A variable that has been declared but not assigned a value.
- **Null:** A variable that intentionally has no value.
- **Symbol:** A unique and immutable value used as an identifier.
- **Object:** A complex data structure.

### Example of Data Types

```typescript
type DataType = string | number | bigint | boolean | undefined | null | symbol | object;

const dataTypes: DataType[] = [
    "String",
    42,
    BigInt(9007199254740991),
    true,
    undefined,
    null,
    Symbol('symbol'),
    {}
];
Enums
Enums allow you to define a set of named constants, which can be used to represent a collection of related values.

Example of Enum
typescript
Copy code
enum UserRole {
    Admin,
    User,
    Guest
}

const role: UserRole = UserRole.Admin;
console.log(role); // Output: 0 (index of Admin)
Interfaces
Interfaces define the structure of an object, specifying the types of its properties and methods.

Example of Interface
typescript
Copy code
interface Person {
    name: string;
    age: number;
    isEligible: boolean;
    greet(): void;
}
Classes
Classes are blueprints for creating objects, encapsulating data and behavior.

Example of Class
typescript
Copy code
class User implements Person {
    constructor(public name: string, public age: number, public isEligible: boolean) {}

    greet(): void {
        console.log(`Hi, this is ${this.name} and age is ${this.age}`);
    }
}

// Create an instance of User
const user = new User("QA", 32, true);
user.greet(); // Output: Hi, this is QA and age is 32
Variables
TypeScript allows variable declarations using var, let, and const:

var: Function-scoped or globally scoped. Value can be reassigned.
let: Block-scoped. Value can be reassigned.
const: Block-scoped. Value cannot be reassigned.
Example of Variable Declaration
typescript
Copy code
let variable: number = 5; // let variable declaration
const constant: string = "I cannot be reassigned"; // const declaration
var globalVar: boolean = true; // var declaration
Functions
Functions in TypeScript can be defined in several ways, including declarative functions, function expressions, and arrow functions.

Example of Functions
typescript
Copy code
// Declarative Function
function printHello(): void {
    console.log("This is a Declarative function");
}
printHello(); // Output: This is a Declarative function

// Function Expression
const b = function(): void {
    console.log('Function expression');
};
b(); // Output: Function expression

// Arrow Function
const test = (): void => console.log("This is an Arrow Function");
test(); // Output: This is an Arrow Function
Objects
Objects are key-value pairs that can hold multiple values and functions.

Example of Object
typescript
Copy code
const person: Person = {
    name: "QA",
    age: 32,
    isEligible: true,
    greet() {
        console.log(`Hi, this is ${this.name} and age is ${this.age}`);
    }
};

person.greet(); // Output: Hi, this is QA and age is 32
Arrays
Arrays are used to store multiple values in a single variable.

Example of Arrays
typescript
Copy code
const arrExample: (string | boolean | number)[] = ["Mandya", false, "Mysore", 67, "Testing"];

console.log(arrExample[2]); // Output: Mysore

const cities: string[] = ["Mandya", "Bengaluru", "Mysore", "Mangalore"];
console.log(cities.length); // Output: 4

cities.push('Udupi'); // Add new city
console.log(cities); // Output: ["Mandya", "Bengaluru", "Mysore", "Mangalore", "Udupi"]
Spread and Rest Operators
Spread and rest operators allow for easier manipulation of arrays and function parameters.

Example of Spread Operator
typescript
Copy code
const copyArray: string[] = [...cities]; // Create a copy of the array
console.log(copyArray);
Example of Rest Operator
typescript
Copy code
function returnValues(...args: number[]): number[] {
    return args;
}
console.log(returnValues(3, 4, 5, 8)); // Output: [3, 4, 5, 8]
Destructuring
Destructuring allows you to unpack values from arrays or properties from objects into distinct variables.

Example of Object Destructuring
typescript
Copy code
const account: Account = {
    accountName: "Savings",
    accountNo: 677343431212,
    isActive: true,
    customer: "John Hammer",
    greet() {
        console.log(`Hi, this is ${this.customer} and accountNo is ${this.accountNo}`);
    }
};

const { accountName, accountNo } = account;
console.log(accountName); // Output: Savings
Example of Array Destructuring
typescript
Copy code
const capitals: string[] = ["Delhi", "Chennai", "Hyderabad", "Mumbai", "Lucknow"];
const [cap1, cap2] = capitals;
console.log(cap1); // Output: Delhi
console.log(cap2); // Output: Chennai
Higher-Order Functions and Callbacks
Higher-order functions are functions that take other functions as arguments or return functions as their results.

Example of Higher-Order Functions
typescript
Copy code
const hello = (name: string): void => {
    console.log("Hello " + name);
};

const greet = (func: (name: string) => void): void => {
    const name = "Testing";
    func(name);
};

greet(hello); // Output: Hello Testing
