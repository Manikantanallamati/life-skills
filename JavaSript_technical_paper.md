# JavaScript Technical Paper

## 1. Different Datatypes in JavaScript

JavaScript has 8 data types:

* **Primitive**: string, number, bigint, boolean, undefined, symbol, null
* **Non-Primitive**: object (including arrays, functions)

## 2. let, var, const

* `var`: function-scoped, hoisted, can be re-declared and updated
* `let`: block-scoped, not hoisted like var, can be updated, not re-declared
* `const`: block-scoped, not hoisted like var, cannot be re-assigned

## 3. Why We Must Not Use var

* Function scope can cause unintended bugs
* Can be re-declared, leading to confusion
* Hoisting can cause undefined behavior

## 4. Why Using Global Variables is Bad

* Pollutes global namespace
* Makes code less modular
* Increases chances of naming conflicts

## 5. Truthy and Falsy Values

* **Falsy**: false, 0, '', null, undefined, NaN
* All other values are **truthy**

## 6. Function Hoisting

* Printing a variable before declaring that variable

## 7. What Happens When a Function Does Not Have a Return Statement

* Returns `undefined` by default

## 8. Different Ways of Declaring a Function

* Function Declaration
* Function Expression
* Arrow Function

## 9. Pass by Reference and Pass by Value

* **Primitive types**: passed by value
* **Objects and arrays**: passed by reference

## 10. Different Types of For Loops

* `for (let i = 0; i < n; i++)` — basic numeric iteration
* `for...in` — iterates over object keys
* `for...of` — iterates over iterable values
* `forEach()` — executes callback on array items

## 11. Searching MDN (Mozilla Developer Network)

* Use MDN for official, updated documentation and examples

## 12. Popular Array Utility Methods

* `map`, `filter`, `reduce`, `forEach`, `find`, `includes`, `sort`

## 13. Popular String Utility Methods

* `toUpperCase`, `toLowerCase`, `trim`, `includes`, `split`, `replace`, `slice`, `substring`

## 14. Popular Object Utility Methods

* `Object.keys`, `Object.values`, `Object.entries`

## 15. When to Use forEach vs. map, filter, reduce

* `forEach`:modifies in the given array only
* `map`: create a new array with new values
* `filter`: extract matching elements
* `reduce`: accumulate into single value

## 16. Immutable and Mutable Methods

* **Immutable**: map, filter, reduce, concat
* **Mutable**: push, pop, splice, sort

## 17. Error Handling (try-catch)

* Use `try {}` and `catch (error) {}` to handle exceptions

## 18. Throwing Errors

* `throw new Error("message")`: standard error object
* `throw "message"`: throws a string, not recommended

## 19. Reading Error Messages and Stack Trace

* Understand the message and trace the file, line number, and function name to debug

## 20. Importance of Catch Block

* Prevents crashing, enables recovery, and debugging

## 21. Spread Operator

* Spreads elements of iterable (e.g., `[...arr]`, `{...obj}`)

## 22. Template Literals

* Syntax: `` `Hello, ${name}` ``
* Supports multi-line strings and interpolation

## 23. Default Parameters

* `function greet(name = "Guest") {}`

## 24. Destructuring

* Extract values from arrays or objects into variables

  ```js
  const [a, b] = [1, 2];
  const {name, age} = user;
  ```

## 25. Closures

* Functions that retain access to their lexical scope even when called outside of it

## 26. Arrow Functions vs Regular Functions

* Arrow functions: no `this`, `arguments`, not suitable for constructors

## 27. === vs ==

* `===`: strict comparison (type + value)
* `==`: loose comparison (value i.e. '5' == 5 : true)

## 28. Why value === undefined is Better Than !value

* `!value` is false for `0`, `''`, `false`, `null`, `undefined`, `NaN`
* `value === undefined` is explicit

## 29. Array Utility Methods Chaining

* Combine methods like: `arr.filter(...).map(...).reduce(...)`

## 30. null vs undefined

* `null`: intentional absence of value
* `undefined`: variable declared but not assigned

## 31. Importing and Exporting Modules

* `require()` and `module.exports` in CommonJS
* `import` and `export` in ES Modules

## 32. Console Methods

* `console.log()`, `console.error()`, `console.warn()`

## 33. Best Practices (From LMS)

* Consistent indentation
* Meaningful variable and function names
* Avoid global scope pollution
* Use constants for values that don’t change

## 34. Passing Functions to Other Functions

* Higher-order functions accept functions as arguments

## 35. Named Functions vs Anonymous Functions

* **Named**: better stack traces and debugging
* **Anonymous**: often used in expressions and callbacks

## 36. Variable Number of Arguments

* Use `arguments` object or rest parameter `(...args)`


