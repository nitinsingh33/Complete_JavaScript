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

## Function Expressions

A function expression defines a function and assigns it to a variable. Unlike function declarations, function expressions are not hoisted, meaning you cannot call them before they are defined.

### Syntax:
```javascript
const add = function(a, b) {
    return a + b;
};

console.log(add(2, 3)); // Output: 5
```

### Key Points:
- Function expressions can be named or anonymous.
- Useful for assigning functions to variables or passing them as arguments.

---

## Arrow Functions

Arrow functions provide a more concise syntax for writing functions. They are especially useful for callbacks and when working with array methods. However, arrow functions do not have their own `this` context, which makes them behave differently from regular functions in some cases.

### Syntax:
```javascript
const multiply = (a, b) => a * b;

console.log(multiply(2, 3)); // Output: 6
```

### Examples:
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

### Summary Table
| Feature               | Syntax Example                             | Key Points                                       |
|-----------------------|-------------------------------------------|-------------------------------------------------|
| Function Expression   | `const add = function(a, b) { ... };`     | Anonymous or named, not hoisted.               |
| Arrow Function        | `const add = (a, b) => a + b;`            | Concise syntax, no `this` binding.             |
| Higher-Order Function | `array.map(x => x * 2);`                  | Takes/returns functions, enables abstractions. |

---

By mastering these function types, you can write more flexible, modular, and expressive JavaScript code.

