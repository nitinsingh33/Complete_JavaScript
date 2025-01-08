# JS Functions

a function is a block of reusable code that performs a specific task or set of tasks. Functions are used to organize code into modular and manageable pieces, promote code reuse, and make programs more readable.

```javascript
function functionName(parameters) {
    // code to be executed
    return result;  // optional return statement
}
```
---
### Syntax-Function Declaration

```javascript
function greet() {
    console.log("Hello Nitin!");
}
```
### Syntax-Function Invocation

```javascript
function greet() {
    console.log("Hello Nitin!");
}

greet()
```
### Syntax-Function Parameter

```javascript
function greet(parameter1, parameter2, ...) {
    console.log("Hello Nitin!");
}

greet()
```
### Syntax-Function Argument

```javascript
function greet(parameter1, parameter2, ...) {
    console.log("Hello Nitin!");
}

greet(argument1, argument2, ...)
```


## Function expressions

A function expression is a way to define a function as part of an expression. It can be either named or anonymous. If it's named, it becomes a named function expression.

### Syntax:
```javascript
var result = function sum(a, b) {
     console.log(a + b);
 };

 result(10, 15);
 ```


### Key Points:
- Function expressions can be named or anonymous.
- Useful for assigning functions to variables or passing them as arguments.

---

## Arrow Functions

An arrow function is a concise way to write function expressions. They were introduced in ES6 (ECMAScript 2015) and have become very popular due to their shorter syntax and lexical scoping of the this keyword. 

### Syntax:
```javascript
const functionName = (parameters) => {
    // function body
};
```
### Examples:
```javascript
const multiply = (a, b) => a * b;

console.log(multiply(2, 3));   //Output: 6
```


1. Single parameter:
```javascript
const square = x => x * x;
console.log(square(4)); // Output: 16
```

2. No parameters:
```javascript
const greet = () => 'Hello, World!';
console.log(greet()); // Output: Hello, World!
```

3. Multiline function body:
```javascript
const subtract = (a, b) => {
    const result = a - b;
    return result;
};

console.log(subtract(5, 2)); // Output: 3
```

### Key Points:
- Compact syntax for functions.
- No `arguments` object and no binding of `this`.

---

## Higher-Order Functions

A higher-order function is a function that operates on other functions, either by taking them as arguments or by returning them.

### Examples:
1. **Functions as arguments:**
```javascript
const applyOperation = (a, b, operation) => operation(a, b);

const add = (x, y) => x + y;
const multiply = (x, y) => x * y;

console.log(applyOperation(3, 4, add)); // Output: 7
console.log(applyOperation(3, 4, multiply)); // Output: 12
```

2. **Functions returning functions:**
```javascript
const createMultiplier = factor => number => number * factor;

const double = createMultiplier(2);
const triple = createMultiplier(3);

console.log(double(5)); // Output: 10
console.log(triple(5)); // Output: 15
```

3. **Array methods (built-in higher-order functions):**
```javascript
const numbers = [1, 2, 3, 4];

const squares = numbers.map(x => x * x);
console.log(squares); // Output: [1, 4, 9, 16]

const evens = numbers.filter(x => x % 2 === 0);
console.log(evens); // Output: [2, 4]

const sum = numbers.reduce((acc, x) => acc + x, 0);
console.log(sum); // Output: 10
```

### Key Points:
- Enables functional programming patterns.
- Commonly used for array manipulation, callbacks, and event handling.

---


