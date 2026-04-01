Here are **clear, neat, and detailed answers with examples** for your **JavaScript Basics interview questions** 👇

---

# 🚀 JavaScript Interview Answers (Basics)

---

## 1. What is JavaScript?

JavaScript is a **high-level, interpreted programming language** used to make web pages **interactive and dynamic**.

* Runs in the browser (client-side) and also on server (Node.js)
* Used for:

  * Form validation
  * DOM manipulation
  * API calls
  * Building full-stack apps

✅ Example:

```javascript
console.log("Hello, Ashish!");
```

---

## 2. What are the data types in JavaScript?

JavaScript has **2 types of data types**:

### 🔹 Primitive Data Types

* String → `"Hello"`
* Number → `10`
* Boolean → `true/false`
* Undefined → `undefined`
* Null → `null`
* BigInt → `123456789n`
* Symbol → `Symbol("id")`

### 🔹 Non-Primitive (Reference Types)

* Object
* Array
* Function

✅ Example:

```javascript
let name = "Ashish"; // String
let age = 22; // Number
let isDev = true; // Boolean

let arr = [1, 2, 3]; // Array
let obj = { name: "Ashish" }; // Object
```

---

## 3. Difference between var, let, and const

| Feature   | var             | let       | const     |
| --------- | --------------- | --------- | --------- |
| Scope     | Function        | Block     | Block     |
| Reassign  | ✅ Yes           | ✅ Yes     | ❌ No      |
| Redeclare | ✅ Yes           | ❌ No      | ❌ No      |
| Hoisting  | Yes (undefined) | Yes (TDZ) | Yes (TDZ) |

✅ Example:

```javascript
var a = 10;
let b = 20;
const c = 30;

b = 25; // allowed
// c = 35; ❌ error
```

---

## 4. What is Hoisting?

Hoisting is JavaScript’s behavior of **moving variable and function declarations to the top of their scope** before execution.

✅ Example:

```javascript
console.log(a); // undefined
var a = 10;
```

👉 Internally becomes:

```javascript
var a;
console.log(a);
a = 10;
```

---

## 5. What is Temporal Dead Zone (TDZ)?

TDZ is the **time between variable declaration and initialization** where you **cannot access let and const variables**.

✅ Example:

```javascript
console.log(a); // ❌ ReferenceError
let a = 10;
```

👉 The variable exists but is **not accessible yet**

---

## 6. What is Scope in JavaScript?

Scope defines **where variables can be accessed** in your code.

Types:

* Global Scope
* Function Scope
* Block Scope

---

## 7. What is Block Scope?

Variables declared with `let` and `const` inside `{}` are only accessible within that block.

✅ Example:

```javascript
{
  let x = 10;
  console.log(x); // 10
}

console.log(x); // ❌ error
```

---

## 8. What is Global Scope?

Variables declared outside any function/block are accessible **anywhere in the program**.

✅ Example:

```javascript
let name = "Ashish";

function greet() {
  console.log(name);
}
greet(); // Ashish
```

---

## 9. What is Function Scope?

Variables declared with `var` inside a function are accessible **only within that function**.

✅ Example:

```javascript
function test() {
  var x = 10;
  console.log(x);
}

test(); // 10
console.log(x); // ❌ error
```

---

## 10. What is Strict Mode?

Strict mode is a way to **enable stricter parsing and error handling** in JavaScript.

👉 Helps catch common mistakes and unsafe actions.

✅ Example:

```javascript
"use strict";

x = 10; // ❌ Error (must declare variable)
```

---

# 🔥 Pro Interview Tip

If interviewer asks follow-up:

* Prefer **let & const over var**
* Explain **scope + hoisting + TDZ together**
* Give **real examples (like bugs caused by var)**

---
Here are **detailed, interview-ready explanations with examples** for your next JavaScript section 👇

---

# 🚀 JavaScript Interview Answers

## 📌 2. Data Types & Operators (Detailed)

---

## 11. What are Primitive Data Types?

Primitive data types are **immutable (cannot be changed)** and stored **by value**.

### ✅ Types:

1. String
2. Number
3. Boolean
4. Undefined
5. Null
6. BigInt
7. Symbol

### 🔥 Key Points:

* Stored in **stack memory**
* Copy creates a **new independent value**

### ✅ Example:

```javascript
let a = 10;
let b = a;

b = 20;

console.log(a); // 10 (unchanged)
console.log(b); // 20
```

👉 Changing `b` does NOT affect `a`

---

## 12. What are Reference Data Types?

Reference types are **objects stored by reference (memory address)**.

### ✅ Types:

* Object
* Array
* Function

### 🔥 Key Points:

* Stored in **heap memory**
* Variables store **reference (address), not actual value**

### ✅ Example:

```javascript
let obj1 = { name: "Ashish" };
let obj2 = obj1;

obj2.name = "Rahul";

console.log(obj1.name); // Rahul
```

👉 Both point to same memory → change affects both

---

## 13. Difference between null and undefined

| Feature     | null                    | undefined                          |
| ----------- | ----------------------- | ---------------------------------- |
| Meaning     | Intentional empty value | Variable declared but not assigned |
| Type        | object (JS bug)         | undefined                          |
| Assigned by | Developer               | JS engine                          |

### ✅ Examples:

```javascript
let a;
console.log(a); // undefined

let b = null;
console.log(b); // null
```

### 🔥 Interview Tip:

* `undefined` → “value not assigned yet”
* `null` → “intentionally empty”

---

## 14. What is NaN?

NaN = **Not a Number**

It represents an **invalid numeric operation**

### ✅ Examples:

```javascript
console.log("abc" / 2); // NaN
console.log(0 / 0);     // NaN
```

### 🔥 Important:

```javascript
console.log(NaN === NaN); // false ❗
```

👉 Use:

```javascript
isNaN(value)
Number.isNaN(value)
```

---

## 15. What is Type Coercion?

Type coercion is **automatic or manual conversion of one data type to another**.

### 🔹 Types:

1. Implicit (automatic)
2. Explicit (manual)

---

### ✅ Implicit Coercion:

```javascript
console.log("5" + 2); // "52" (number → string)
console.log("5" - 2); // 3 (string → number)
```

---

### ✅ Explicit Coercion:

```javascript
Number("10"); // 10
String(123);  // "123"
Boolean(0);   // false
```

---

## 16. Difference between == and ===

| Operator | Meaning         | Type Conversion |
| -------- | --------------- | --------------- |
| ==       | Loose equality  | ✅ Yes           |
| ===      | Strict equality | ❌ No            |

---

### ✅ Example:

```javascript
console.log(5 == "5");  // true
console.log(5 === "5"); // false
```

### 🔥 Interview Tip:

👉 Always prefer `===` (safer & predictable)

---

## 17. What is typeof operator?

`typeof` is used to **check the data type of a variable**

---

### ✅ Examples:

```javascript
typeof "Hello";   // string
typeof 10;        // number
typeof true;      // boolean
typeof undefined; // undefined
typeof null;      // object ❗ (bug in JS)
```

---

### 🔥 Special Cases:

```javascript
typeof NaN; // number
typeof [];  // object
typeof {}   // object
```

---

## 18. What is instanceof?

`instanceof` checks whether an object is an **instance of a constructor (class)**

---

### ✅ Example:

```javascript
let arr = [1, 2, 3];

console.log(arr instanceof Array);  // true
console.log(arr instanceof Object); // true
```

---

### 🔥 Use Case:

* To differentiate objects like Array vs Object

---

## 19. What are Truthy and Falsy values?

### 🔹 Falsy Values (only 7):

* false
* 0
* -0
* "" (empty string)
* null
* undefined
* NaN

---

### 🔹 Everything else → Truthy

---

### ✅ Example:

```javascript
if ("hello") {
  console.log("Truthy");
}

if (0) {
  console.log("Won't run");
}
```

---

### 🔥 Interview Trick:

```javascript
Boolean([]);  // true
Boolean({});  // true
```

👉 Empty array/object are **truthy**

---

## 20. What is Optional Chaining (?.)?

Optional chaining (`?.`) is used to **safely access nested object properties** without causing errors.

---

### ❌ Without Optional Chaining:

```javascript
console.log(user.address.city); // ❌ Error if address undefined
```

---

### ✅ With Optional Chaining:

```javascript
console.log(user?.address?.city);
```

👉 Returns `undefined` instead of crashing

---

### 🔥 Real Example:

```javascript
let user = {};

console.log(user?.profile?.name); // undefined (safe)
```

---

# 🚀 Final Interview Tips

* Always explain with:

  * **Definition**
  * **Key behavior**
  * **Example**
* Mention:

  * Stack vs Heap (VERY IMPORTANT)
  * `===` over `==`
  * Optional chaining for real-world apps

---

Here are **detailed, interview-ready explanations with examples** for your next section 👇

---

# 🚀 JavaScript Interview Answers

## 📌 3. Functions (Detailed)

---

## 21. What is a Function Declaration?

A function declaration is a **named function defined using the `function` keyword**.

### 🔥 Key Points:

* Hoisted (can be called before definition)
* Has a name

### ✅ Example:

```javascript
greet(); // ✅ works (hoisting)

function greet() {
  console.log("Hello!");
}
```

---

## 22. What is a Function Expression?

A function expression is when a function is **assigned to a variable**.

### 🔥 Key Points:

* Not hoisted like declarations
* Can be anonymous

### ✅ Example:

```javascript
const greet = function () {
  console.log("Hello!");
};

greet();
```

### ❌ Hoisting Issue:

```javascript
greet(); // ❌ Error

const greet = function () {};
```

---

## 23. What is an Arrow Function?

Arrow functions are a **shorter syntax** for writing functions using `=>`.

### 🔥 Key Points:

* More concise
* No `this` binding (inherits from parent)

### ✅ Examples:

```javascript
const add = (a, b) => a + b;

const greet = () => {
  console.log("Hello!");
};
```

---

## 24. Difference between Normal Function and Arrow Function

| Feature     | Normal Function   | Arrow Function  |
| ----------- | ----------------- | --------------- |
| Syntax      | function() {}     | () => {}        |
| this        | Own `this`        | Inherits `this` |
| arguments   | Available         | Not available   |
| Hoisting    | Yes (declaration) | No              |
| Constructor | Yes               | No              |

---

### 🔥 Example (`this` difference):

```javascript
const obj = {
  name: "Ashish",
  normal: function () {
    console.log(this.name);
  },
  arrow: () => {
    console.log(this.name);
  }
};

obj.normal(); // Ashish
obj.arrow();  // undefined ❗
```

---

## 25. What is a Callback Function?

A callback is a **function passed as an argument to another function** and executed later.

---

### ✅ Example:

```javascript
function greet(name, callback) {
  console.log("Hello " + name);
  callback();
}

function sayBye() {
  console.log("Bye!");
}

greet("Ashish", sayBye);
```

---

### 🔥 Real Use:

* API calls
* Event listeners
* setTimeout

---

## 26. What is a Higher-Order Function?

A higher-order function is a function that:

* Takes another function as argument OR
* Returns a function

---

### ✅ Example:

```javascript
function calculate(a, b, operation) {
  return operation(a, b);
}

const add = (x, y) => x + y;

console.log(calculate(5, 3, add)); // 8
```

---

### 🔥 Built-in Examples:

* `map()`
* `filter()`
* `reduce()`

---

## 27. What is a Pure Function?

A pure function:

1. Always returns same output for same input
2. Has no side effects (does not modify external data)

---

### ✅ Example:

```javascript
function add(a, b) {
  return a + b;
}
```

---

### ❌ Not Pure:

```javascript
let total = 0;

function addToTotal(x) {
  total += x; // side effect
}
```

---

## 28. What is IIFE?

IIFE = **Immediately Invoked Function Expression**

It runs **immediately after being defined**

---

### ✅ Example:

```javascript
(function () {
  console.log("I run immediately!");
})();
```

---

### 🔥 Use Cases:

* Avoid global scope pollution
* Initialization code

---

## 29. What is Default Parameter?

Default parameters allow you to **assign default values to function parameters**

---

### ✅ Example:

```javascript
function greet(name = "Guest") {
  console.log("Hello " + name);
}

greet();        // Hello Guest
greet("Ashish"); // Hello Ashish
```

---

## 30. What is Rest Parameter?

Rest parameter (`...`) collects multiple arguments into an array

---

### ✅ Example:

```javascript
function sum(...numbers) {
  return numbers.reduce((acc, curr) => acc + curr, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
```

---

### 🔥 Difference:

* Rest → function parameters
* Spread → used while calling or copying

---

# 🚀 Final Interview Tips (IMPORTANT 🔥)

If interviewer goes deeper, mention:

* Arrow functions don’t have `this`, `arguments`, `prototype`
* Callbacks → can lead to **callback hell**
* Pure functions → used in **React & functional programming**
* HOF → very important for **array methods**

---
Here are **detailed, interview-ready answers with clear explanations + examples** for this section 👇

---

# 🚀 JavaScript Interview Answers

## 📌 4. Objects & Arrays (Detailed)

---

## 31. How to create an object?

Objects are collections of **key-value pairs**.

### ✅ Ways to create:

### 🔹 1. Object Literal (most common)

```javascript
const user = {
  name: "Ashish",
  age: 22
};
```

### 🔹 2. Using Constructor

```javascript
const user = new Object();
user.name = "Ashish";
```

### 🔹 3. Using Class

```javascript
class User {
  constructor(name) {
    this.name = name;
  }
}
const u1 = new User("Ashish");
```

---

## 32. How to access object properties?

### 🔹 2 Ways:

### ✅ Dot Notation:

```javascript
console.log(user.name);
```

### ✅ Bracket Notation:

```javascript
console.log(user["name"]);
```

### 🔥 When to use bracket:

```javascript
const key = "name";
console.log(user[key]);
```

---

## 33. What is Destructuring?

Destructuring allows you to **extract values from objects or arrays into variables**

---

### ✅ Object Destructuring:

```javascript
const user = { name: "Ashish", age: 22 };

const { name, age } = user;
```

---

### ✅ Array Destructuring:

```javascript
const arr = [10, 20];

const [a, b] = arr;
```

---

### 🔥 Advanced:

```javascript
const { name: username } = user;
```

---

## 34. What is Spread Operator?

Spread operator (`...`) is used to **expand or copy elements**

---

### ✅ Array Example:

```javascript
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];
```

---

### ✅ Object Example:

```javascript
const user = { name: "Ashish" };
const updated = { ...user, age: 22 };
```

---

### 🔥 Use Cases:

* Copy arrays/objects
* Merge data
* Avoid mutation

---

## 35. What are map, filter, reduce?

These are **important array methods (VERY IMPORTANT IN INTERVIEWS)**

---

### 🔹 map() → Transform each element

```javascript
const nums = [1, 2, 3];

const result = nums.map(n => n * 2);
// [2, 4, 6]
```

---

### 🔹 filter() → Select elements

```javascript
const nums = [1, 2, 3, 4];

const even = nums.filter(n => n % 2 === 0);
// [2, 4]
```

---

### 🔹 reduce() → Accumulate value

```javascript
const nums = [1, 2, 3];

const sum = nums.reduce((acc, curr) => acc + curr, 0);
// 6
```

---

## 36. What is forEach?

`forEach()` is used to **iterate over an array**

---

### ✅ Example:

```javascript
const nums = [1, 2, 3];

nums.forEach(n => console.log(n));
```

---

### 🔥 Important:

* Does NOT return a new array
* Used for side effects (logging, API calls)

---

## 37. Difference between map and forEach

| Feature      | map()          | forEach() |
| ------------ | -------------- | --------- |
| Return value | New array      | undefined |
| Purpose      | Transform data | Iterate   |
| Chainable    | ✅ Yes          | ❌ No      |

---

### ✅ Example:

```javascript
const nums = [1, 2, 3];

const a = nums.map(n => n * 2); // [2,4,6]
const b = nums.forEach(n => n * 2); // undefined
```

---

## 38. What is find()?

`find()` returns the **first element that matches condition**

---

### ✅ Example:

```javascript
const nums = [1, 2, 3, 4];

const result = nums.find(n => n > 2);
// 3
```

---

### 🔥 Difference:

* `find()` → single value
* `filter()` → array

---

## 39. What is some() and every()?

### 🔹 some() → checks if ANY element passes

```javascript
const nums = [1, 2, 3];

nums.some(n => n > 2); // true
```

---

### 🔹 every() → checks if ALL elements pass

```javascript
nums.every(n => n > 0); // true
```

---

### 🔥 Quick Difference:

* `some()` → OR condition
* `every()` → AND condition

---

## 40. What is shallow copy vs deep copy?

---

### 🔹 Shallow Copy:

Copies only **first level**, nested objects still reference same memory

```javascript
const obj1 = { a: 1, b: { c: 2 } };
const obj2 = { ...obj1 };

obj2.b.c = 99;

console.log(obj1.b.c); // 99 ❗
```

---

### 🔹 Deep Copy:

Copies **all levels (fully independent)**

---

### ✅ Methods:

```javascript
// Modern way
const deep = structuredClone(obj1);

// Old way
const deep2 = JSON.parse(JSON.stringify(obj1));
```

---

### 🔥 Key Difference:

| Feature        | Shallow Copy | Deep Copy    |
| -------------- | ------------ | ------------ |
| Nested objects | Shared       | Independent  |
| Performance    | Faster       | Slower       |
| Use case       | Simple data  | Complex data |

---

# 🚀 Final Interview Tips (IMPORTANT 🔥)

If interviewer goes deeper, mention:

* `map/filter/reduce` → **functional programming**
* Always prefer **immutable operations (spread, map)**
* Avoid direct mutation → important in **React**
* Know difference:

  * `find` vs `filter`
  * `map` vs `forEach`

---
Here are **deep, interview-level explanations (VERY IMPORTANT TOPIC 🔥)** for Closures & Scope 👇

---

# 🚀 JavaScript Interview Answers

## 📌 5. Closures & Scope (Detailed)

---

## 41. What is Closure?

A closure is created when a **function remembers variables from its outer (parent) scope even after the outer function has finished execution**.

### 🔥 Key Idea:

👉 Function + its lexical environment = **Closure**

---

### ✅ Example:

```javascript id="h1p2a9"
function outer() {
  let count = 0;

  function inner() {
    count++;
    console.log(count);
  }

  return inner;
}

const fn = outer();
fn(); // 1
fn(); // 2
```

👉 `inner()` still remembers `count` even after `outer()` is done

---

## 42. Give a real example of Closure

### 🔹 Real-world use: Counter / Private variable

```javascript id="gg2v18"
function createCounter() {
  let count = 0;

  return {
    increment: () => ++count,
    decrement: () => --count,
    get: () => count
  };
}

const counter = createCounter();

console.log(counter.increment()); // 1
console.log(counter.increment()); // 2
console.log(counter.get());       // 2
```

### 🔥 Why important:

* Data privacy
* State management (React uses closures internally)

---

## 43. What is Lexical Scope?

Lexical scope means **scope is determined by where variables are written in code (not how functions are called)**.

---

### ✅ Example:

```javascript id="jy5x6t"
function outer() {
  let name = "Ashish";

  function inner() {
    console.log(name);
  }

  inner();
}

outer(); // Ashish
```

👉 `inner()` can access `name` because it is defined inside `outer()`

---

## 44. What is Execution Context?

Execution context is the **environment in which JavaScript code is executed**.

---

### 🔹 Types:

1. Global Execution Context (GEC)
2. Function Execution Context (FEC)

---

### 🔥 It contains:

* Variable Object (variables, functions)
* Scope Chain
* `this` keyword

---

### ✅ Example:

```javascript id="u8k8p3"
let a = 10;

function test() {
  let b = 20;
}
```

👉 JS creates execution contexts to run this code

---

## 45. What is Call Stack?

Call stack is a **data structure that keeps track of function calls (LIFO)**

---

### 🔥 LIFO → Last In, First Out

---

### ✅ Example:

```javascript id="bbrh64"
function one() {
  two();
}

function two() {
  console.log("Hello");
}

one();
```

### 🧠 Stack Flow:

```
one() → pushed
two() → pushed
console.log → executed
two() → popped
one() → popped
```

---

## 46. What is `this` keyword?

`this` refers to the **object that is calling the function**

---

### ✅ Example:

```javascript id="j3b9h9"
const user = {
  name: "Ashish",
  greet() {
    console.log(this.name);
  }
};

user.greet(); // Ashish
```

---

### 🔥 Depends on:

* How function is called (not where defined)

---

## 47. How does `this` work in Arrow Functions?

Arrow functions **do NOT have their own `this`**
They inherit `this` from their **parent scope**

---

### ❗ Example:

```javascript id="gpt4q2"
const user = {
  name: "Ashish",
  greet: () => {
    console.log(this.name);
  }
};

user.greet(); // undefined ❗
```

---

### ✅ Correct Way:

```javascript id="v0wz2s"
const user = {
  name: "Ashish",
  greet() {
    const arrow = () => {
      console.log(this.name);
    };
    arrow();
  }
};

user.greet(); // Ashish
```

---

## 48. What is bind()?

`bind()` creates a **new function with fixed `this` value**

---

### ✅ Example:

```javascript id="1o4n1b"
const user = {
  name: "Ashish"
};

function greet() {
  console.log(this.name);
}

const boundFn = greet.bind(user);
boundFn(); // Ashish
```

---

### 🔥 Use Case:

* Fix `this` in callbacks

---

## 49. What is call()?

`call()` invokes a function **immediately** and sets `this`

---

### ✅ Example:

```javascript id="lz9qkh"
function greet(city) {
  console.log(this.name + " from " + city);
}

const user = { name: "Ashish" };

greet.call(user, "Mumbai");
```

---

## 50. What is apply()?

`apply()` is same as `call()` but arguments are passed as an **array**

---

### ✅ Example:

```javascript id="8rkn5x"
greet.apply(user, ["Mumbai"]);
```

---

## 🔥 call vs apply vs bind

| Feature   | call()     | apply()   | bind()           |
| --------- | ---------- | --------- | ---------------- |
| Execution | Immediate  | Immediate | Returns function |
| Arguments | Individual | Array     | Individual       |

---

# 🚀 Final Interview Tips (VERY IMPORTANT 🔥)

If interviewer goes deep, say:

* Closure = **function + lexical scope**
* Used in:

  * Data hiding
  * React hooks
* `this` depends on **call-site**
* Arrow function → no `this`, no `arguments`
* bind/call/apply → control `this`

---
Here are **deep, interview-level explanations (MOST IMPORTANT TOPIC 🔥)** for **Asynchronous JavaScript** 👇

---

# 🚀 JavaScript Interview Answers

## 📌 6. Asynchronous JavaScript (Detailed)

---

## 51. What is Synchronous vs Asynchronous?

### 🔹 Synchronous (Blocking)

* Code runs **line by line**
* Next line waits until current finishes

```javascript
console.log("Start");
console.log("End");
```

👉 Output:

```
Start
End
```

---

### 🔹 Asynchronous (Non-blocking)

* Code does NOT wait
* Executes later (via callbacks, promises)

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Async Task");
}, 1000);

console.log("End");
```

👉 Output:

```
Start
End
Async Task
```

---

## 52. What is Callback Hell?

Callback hell is when **multiple nested callbacks make code hard to read and maintain**

---

### ❌ Example:

```javascript
id="4wxqf4"
setTimeout(() => {
  console.log("Step 1");
  setTimeout(() => {
    console.log("Step 2");
    setTimeout(() => {
      console.log("Step 3");
    }, 1000);
  }, 1000);
}, 1000);
```

---

### 🔥 Problem:

* Hard to debug
* Pyramid structure

👉 Solution:

* Promises
* Async/Await

---

## 53. What is Promise?

A Promise is an object that represents **eventual completion (or failure) of an async operation**

---

### 🔥 Syntax:

```javascript
id="j39fkl"
const promise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Done!");
  } else {
    reject("Error!");
  }
});
```

---

### ✅ Using Promise:

```javascript
id="78f2ti"
promise
  .then(res => console.log(res))
  .catch(err => console.log(err));
```

---

## 54. Promise States

A Promise has **3 states**:

1. **Pending** → Initial state
2. **Fulfilled** → Success (`resolve`)
3. **Rejected** → Failure (`reject`)

---

### 🔥 Flow:

```
Pending → Fulfilled
        → Rejected
```

---

## 55. What is async/await?

`async/await` is a **cleaner way to handle Promises**

---

### 🔹 async:

* Makes function return a Promise

### 🔹 await:

* Waits for Promise to resolve

---

### ✅ Example:

```javascript
id="6sx1dl"
async function fetchData() {
  try {
    let res = await fetch("https://api.com");
    let data = await res.json();
    console.log(data);
  } catch (err) {
    console.log(err);
  }
}
```

---

### 🔥 Benefits:

* Cleaner code
* Avoid callback hell

---

## 56. What is Event Loop?

Event loop is a mechanism that **handles asynchronous operations in JavaScript**

---

### 🧠 How it works:

1. Call Stack executes code
2. Async tasks go to Web APIs
3. Results go to Queue
4. Event Loop pushes them back to stack

---

### 🔥 Example:

```javascript
id="2z3c9k"
console.log("Start");

setTimeout(() => console.log("Timeout"), 0);

console.log("End");
```

👉 Output:

```
Start
End
Timeout
```

---

## 57. What is Microtask Queue?

Microtask queue has **higher priority than callback queue**

---

### 🔹 Contains:

* Promises (`.then`)
* MutationObserver

---

### ✅ Example:

```javascript
id="l7tr6v"
console.log("Start");

Promise.resolve().then(() => console.log("Promise"));

console.log("End");
```

👉 Output:

```
Start
End
Promise
```

---

## 58. What is setTimeout?

`setTimeout()` executes a function **after a delay**

---

### ✅ Example:

```javascript
id="7q6w3v"
setTimeout(() => {
  console.log("Hello after 2 sec");
}, 2000);
```

---

### 🔥 Note:

* Delay is **minimum time**, not exact

---

## 59. What is setInterval?

`setInterval()` runs a function **repeatedly at fixed interval**

---

### ✅ Example:

```javascript
id="2h8s9l"
setInterval(() => {
  console.log("Running every 1 sec");
}, 1000);
```

---

### 🔥 Stop it:

```javascript
id="s7f6l9"
const id = setInterval(() => {}, 1000);
clearInterval(id);
```

---

## 60. What is Fetch API?

Fetch API is used to **make HTTP requests (GET, POST, etc.)**

---

### ✅ Example:

```javascript
id="1w8k9z"
fetch("https://api.example.com/data")
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.log(err));
```

---

### 🔥 With async/await:

```javascript
id="3k9x1a"
async function getData() {
  const res = await fetch("https://api.example.com");
  const data = await res.json();
  console.log(data);
}
```

---

# 🚀 Final Interview Tips (VERY IMPORTANT 🔥)

If interviewer goes deep, mention:

* JS is **single-threaded but async via event loop**
* Microtasks > Macrotasks priority
* Prefer:

  * `async/await` over `.then`
* Avoid:

  * Callback hell

---

# 🔥 MOST ASKED INTERVIEW QUESTION

👉 Output-based question:

```javascript
console.log("Start");

setTimeout(() => console.log("Timeout"), 0);

Promise.resolve().then(() => console.log("Promise"));

console.log("End");
```

✅ Output:

```
Start
End
Promise
Timeout
```

---
Here are **detailed, interview-ready answers with clear explanations + examples** for DOM & Browser 👇

---

# 🚀 JavaScript Interview Answers

## 📌 7. DOM & Browser (Detailed)

---

## 61. What is DOM?

DOM = **Document Object Model**

It is a **tree-like structure of HTML elements** created by the browser so JavaScript can **read, modify, and interact with the webpage**.

---

### 🔥 Example HTML:

```html
<body>
  <h1>Hello</h1>
</body>
```

👉 DOM Tree:

```text
Document
 └── html
      └── body
           └── h1
```

---

### ✅ Example (JS interaction):

```javascript id="yrw31o"
document.querySelector("h1").textContent = "Hello Ashish";
```

---

## 62. How to select elements in DOM?

### 🔹 Common Methods:

```javascript id="s94mbk"
document.getElementById("id");
document.getElementsByClassName("class");
document.getElementsByTagName("tag");

document.querySelector(".class");
document.querySelectorAll(".class");
```

---

### 🔥 Example:

```javascript id="q9c3z6"
const el = document.querySelector("#title");
```

---

## 63. Difference between querySelector and getElementById

| Feature     | querySelector   | getElementById |
| ----------- | --------------- | -------------- |
| Selector    | CSS selector    | Only ID        |
| Return      | First match     | Exact element  |
| Performance | Slightly slower | Faster         |

---

### ✅ Example:

```javascript id="zz9dwc"
document.querySelector("#id");
document.getElementById("id");
```

---

### 🔥 Tip:

👉 Use `querySelector` for flexibility

---

## 64. What is Event Delegation?

Event delegation is a technique where you **attach one event listener to a parent instead of multiple child elements**

---

### 🔥 Why?

* Better performance
* Works for dynamically added elements

---

### ✅ Example:

```javascript id="sqsbjf"
document.getElementById("parent").addEventListener("click", (e) => {
  if (e.target.tagName === "BUTTON") {
    console.log("Button clicked");
  }
});
```

---

## 65. What is addEventListener?

It is used to **attach an event handler to an element**

---

### ✅ Syntax:

```javascript id="98c7st"
element.addEventListener("event", callback);
```

---

### ✅ Example:

```javascript id="6m5n9q"
button.addEventListener("click", () => {
  console.log("Clicked!");
});
```

---

## 66. What is preventDefault?

It prevents the **default browser behavior**

---

### 🔥 Example:

```javascript id="l6n5fd"
form.addEventListener("submit", (e) => {
  e.preventDefault();
  console.log("Form prevented from submitting");
});
```

---

### 🔹 Use Cases:

* Stop form reload
* Stop link navigation

---

## 67. What is stopPropagation?

It stops the **event from bubbling up to parent elements**

---

### 🔥 Example:

```javascript id="m5z41u"
child.addEventListener("click", (e) => {
  e.stopPropagation();
});
```

---

### 🧠 Event Flow:

```text
Capture → Target → Bubble
```

---

## 68. What is localStorage?

`localStorage` is used to **store data in the browser permanently**

---

### 🔥 Key Points:

* No expiry
* Stores data as string

---

### ✅ Example:

```javascript id="ot08ei"
localStorage.setItem("name", "Ashish");
console.log(localStorage.getItem("name"));
```

---

## 69. What is sessionStorage?

`sessionStorage` stores data **only for the session (tab)**

---

### 🔥 Key Points:

* Cleared when tab is closed

---

### ✅ Example:

```javascript id="nljrhh"
sessionStorage.setItem("user", "Ashish");
```

---

## 70. Difference between localStorage and sessionStorage

| Feature | localStorage | sessionStorage   |
| ------- | ------------ | ---------------- |
| Expiry  | No expiry    | Until tab closes |
| Scope   | All tabs     | Single tab       |
| Storage | Persistent   | Temporary        |

---

# 🚀 Final Interview Tips (IMPORTANT 🔥)

If interviewer goes deeper, mention:

* DOM = **bridge between HTML & JS**
* Event delegation → improves performance
* `addEventListener` supports multiple handlers
* Storage:

  * localStorage → persistent data
  * sessionStorage → temporary session data

---

# 🔥 Real Interview Scenario Question

👉 Q: How to handle click events on dynamically added elements?

✅ Answer:
👉 Use **event delegation**

---
Here are **detailed, interview-ready explanations (VERY IMPORTANT for modern JS 🔥)** for **ES6+ Features** 👇

---

# 🚀 JavaScript Interview Answers

## 📌 8. ES6+ Features (Detailed)

---

## 71. What are ES6 features?

ES6 (ECMAScript 2015) introduced **modern JavaScript features** to make code **cleaner, shorter, and more powerful**.

### 🔥 Major ES6 Features:

* `let` and `const`
* Arrow functions
* Template literals
* Destructuring
* Spread & Rest operator
* Classes
* Modules (import/export)
* Promises
* Default parameters

---

## 72. What are Template Literals?

Template literals use **backticks (` `)** and allow:

* String interpolation
* Multi-line strings

---

### ✅ Example:

```javascript id="3bbxzz"
const name = "Ashish";

console.log(`Hello ${name}`);
```

---

### 🔥 Multi-line:

```javascript id="wjg5aj"
const msg = `Hello
Welcome!`;
```

---

## 73. What are Modules?

Modules allow you to **split code into multiple files** and reuse them.

---

### 🔥 Benefits:

* Better organization
* Reusability
* Maintainability

---

### ✅ Example:

```javascript id="t6vps6"
// file1.js
export const name = "Ashish";
```

```javascript id="4fowdd"
// file2.js
import { name } from "./file1.js";
```

---

## 74. What is export and import?

Used to **share code between files**

---

### 🔹 Named Export:

```javascript id="qqsdix"
export const add = (a, b) => a + b;
```

```javascript id="24kebd"
import { add } from "./file.js";
```

---

## 75. What is Default Export?

Default export allows exporting **one main value per file**

---

### ✅ Example:

```javascript id="9bp1nx"
// file.js
export default function greet() {
  console.log("Hello");
}
```

```javascript id="n5bl9l"
import greet from "./file.js";
```

---

### 🔥 Difference:

* Named → `{}` required
* Default → no `{}`

---

## 76. What is Destructuring Assignment?

Destructuring lets you **extract values from arrays/objects easily**

---

### ✅ Object:

```javascript id="dpfnw5"
const user = { name: "Ashish", age: 22 };

const { name, age } = user;
```

---

### ✅ Array:

```javascript id="q88sd2"
const arr = [1, 2];

const [a, b] = arr;
```

---

### 🔥 Advanced:

```javascript id="6e8tnv"
const { name: username } = user;
```

---

## 77. What is Spread Operator?

Spread (`...`) expands elements

---

### ✅ Example:

```javascript id="klg4q4"
const arr = [1, 2];
const newArr = [...arr, 3];
```

---

### 🔥 Object:

```javascript id="c2b9z9"
const obj = { a: 1 };
const newObj = { ...obj, b: 2 };
```

---

### 🔥 Use:

* Copy
* Merge
* Avoid mutation

---

## 78. What is Rest Operator?

Rest (`...`) collects multiple values into an array

---

### ✅ Example:

```javascript id="5hl6p2"
function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
```

---

### 🔥 Difference:

| Spread  | Rest     |
| ------- | -------- |
| Expands | Collects |

---

## 79. What is Class in JavaScript?

A class is a **blueprint to create objects** (syntactic sugar over prototypes)

---

### ✅ Example:

```javascript id="5plhzt"
class User {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log("Hello " + this.name);
  }
}

const u1 = new User("Ashish");
u1.greet();
```

---

### 🔥 Features:

* Constructor
* Methods
* Inheritance

---

## 80. What is Constructor?

A constructor is a **special method inside a class** used to initialize objects

---

### 🔥 Key Points:

* Runs automatically when object is created
* Uses `this`

---

### ✅ Example:

```javascript id="vb8m7j"
class User {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

const u1 = new User("Ashish", 22);
```

---

# 🚀 Final Interview Tips (IMPORTANT 🔥)

If interviewer goes deeper, mention:

* ES6 = **modern JS standard**
* Use:

  * `const` by default
  * Arrow functions for short code
* Modules → important for **React/Node projects**
* Spread/Rest → VERY frequently used
* Classes → just syntactic sugar over prototypes

---

# 🔥 Most Asked Follow-Up

👉 Difference between:

* Spread vs Rest
* Named vs Default export

---
Here are **deep, interview-level explanations (VERY IMPORTANT 🔥)** for **OOP in JavaScript** 👇

---

# 🚀 JavaScript Interview Answers

## 📌 9. OOP in JavaScript (Detailed)

---

## 81. What is Prototype?

In JavaScript, every object has a hidden property called **`[[Prototype]]`** (accessible via `__proto__`) that links to another object.

👉 This allows objects to **share properties and methods**

---

### ✅ Example:

```javascript
const obj = {
  greet() {
    console.log("Hello");
  }
};

const user = {};
user.__proto__ = obj;

user.greet(); // Hello
```

---

### 🔥 Key Idea:

👉 JS uses **prototype-based inheritance**, not classical OOP like Java/C++

---

## 82. What is Prototypal Inheritance?

Prototypal inheritance means an object can **inherit properties/methods from another object via prototype chain**

---

### ✅ Example:

```javascript
const parent = {
  sayHi() {
    console.log("Hi");
  }
};

const child = Object.create(parent);

child.sayHi(); // Hi
```

---

### 🔥 Prototype Chain:

```text
child → parent → Object.prototype → null
```

---

## 83. What is Class Inheritance?

Class inheritance allows a class to **inherit properties and methods from another class**

---

### ✅ Example:

```javascript
class Animal {
  speak() {
    console.log("Animal sound");
  }
}

class Dog extends Animal {
  bark() {
    console.log("Bark");
  }
}

const d = new Dog();
d.speak(); // inherited
d.bark();
```

---

### 🔥 Keywords:

* `extends` → inherit
* `super()` → call parent constructor

---

## 84. What is Encapsulation?

Encapsulation means **binding data and methods together** and restricting direct access.

---

### ✅ Example:

```javascript
class Bank {
  #balance = 0; // private

  deposit(amount) {
    this.#balance += amount;
  }

  getBalance() {
    return this.#balance;
  }
}

const b = new Bank();
b.deposit(100);
console.log(b.getBalance()); // 100
```

---

### 🔥 Benefit:

* Data protection
* Controlled access

---

## 85. What is Polymorphism?

Polymorphism means **same method behaves differently based on context**

---

### ✅ Example:

```javascript
class Animal {
  speak() {
    console.log("Some sound");
  }
}

class Dog extends Animal {
  speak() {
    console.log("Bark");
  }
}

new Dog().speak(); // Bark
```

---

### 🔥 Types:

* Method overriding
* Method overloading (not native in JS)

---

## 86. What is Abstraction?

Abstraction means **hiding complex implementation and showing only necessary features**

---

### ✅ Example:

```javascript
function startCar() {
  igniteEngine();
  injectFuel();
  console.log("Car started");
}
```

👉 User doesn’t need to know internal steps

---

### 🔥 In JS:

* Achieved using classes & functions

---

## 87. What is Getter and Setter?

Getters and setters allow **controlled access to object properties**

---

### ✅ Example:

```javascript
class User {
  constructor(name) {
    this._name = name;
  }

  get name() {
    return this._name;
  }

  set name(value) {
    this._name = value;
  }
}

const u = new User("Ashish");
console.log(u.name);

u.name = "Rahul";
```

---

### 🔥 Benefit:

* Validation
* Encapsulation

---

## 88. What is Static Method?

Static methods belong to the **class, not instance**

---

### ✅ Example:

```javascript
class MathUtil {
  static add(a, b) {
    return a + b;
  }
}

console.log(MathUtil.add(2, 3)); // 5
```

---

### 🔥 Key Point:

👉 Cannot access with object instance

---

## 89. What is Object.create()?

`Object.create()` creates a **new object with specified prototype**

---

### ✅ Example:

```javascript
const parent = {
  greet() {
    console.log("Hello");
  }
};

const child = Object.create(parent);

child.greet();
```

---

### 🔥 Use:

* Create inheritance manually

---

## 90. What is new keyword?

`new` is used to **create an instance of a constructor or class**

---

### 🔥 What it does internally:

1. Creates empty object
2. Links to prototype
3. Sets `this`
4. Returns object

---

### ✅ Example:

```javascript
function User(name) {
  this.name = name;
}

const u1 = new User("Ashish");
```

---

# 🚀 Final Interview Tips (VERY IMPORTANT 🔥)

If interviewer goes deep, say:

* JS uses **prototype-based OOP**
* Classes are **syntactic sugar over prototypes**
* Important concepts:

  * Prototype chain
  * Inheritance
  * Encapsulation (private fields `#`)
* `new` keyword → very commonly asked internally

---

# 🔥 Most Asked Combo Question

👉 Difference between:

* Prototype vs Class
* Inheritance vs Prototypal inheritance

---
Here are **advanced, interview-level explanations (VERY IMPORTANT 🔥)** for **JavaScript Advanced Concepts** 👇

---

# 🚀 JavaScript Interview Answers

## 📌 10. Advanced Concepts (Detailed)

---

## 91. What is Debouncing?

Debouncing ensures a function is **called only after a delay when user stops triggering events**

---

### 🔥 Use Case:

* Search input
* Resize events

---

### ✅ Example:

```javascript id="9d1t0q"
function debounce(fn, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => {
      fn.apply(this, args);
    }, delay);
  };
}

const search = debounce(() => {
  console.log("API Call");
}, 500);
```

👉 Called only after user stops typing

---

## 92. What is Throttling?

Throttling ensures a function is called **at most once in a given time interval**

---

### 🔥 Use Case:

* Scroll events
* Button clicks

---

### ✅ Example:

```javascript id="l5q2rx"
function throttle(fn, limit) {
  let flag = true;

  return function (...args) {
    if (!flag) return;

    fn.apply(this, args);
    flag = false;

    setTimeout(() => {
      flag = true;
    }, limit);
  };
}
```

---

### 🔥 Difference:

* Debounce → waits for inactivity
* Throttle → limits frequency

---

## 93. What is Memoization?

Memoization is an optimization technique where **results are cached to avoid repeated calculations**

---

### ✅ Example:

```javascript id="23bw68"
function memoize(fn) {
  let cache = {};

  return function (x) {
    if (cache[x]) return cache[x];

    let result = fn(x);
    cache[x] = result;
    return result;
  };
}

const square = memoize(n => n * n);

console.log(square(5)); // calculated
console.log(square(5)); // from cache
```

---

### 🔥 Use Case:

* Expensive calculations
* Dynamic programming

---

## 94. What is Currying?

Currying converts a function with multiple arguments into **nested functions with single argument**

---

### ✅ Example:

```javascript id="8z9ybd"
function add(a) {
  return function (b) {
    return function (c) {
      return a + b + c;
    };
  };
}

console.log(add(1)(2)(3)); // 6
```

---

### 🔥 Arrow Version:

```javascript id="m52ny8"
const add = a => b => c => a + b + c;
```

---

## 95. What is Event Bubbling?

Event bubbling means event **propagates from child → parent**

---

### ✅ Example:

```javascript id="03gvyv"
child.addEventListener("click", () => console.log("Child"));
parent.addEventListener("click", () => console.log("Parent"));
```

👉 Clicking child:

```text id="62br7f"
Child
Parent
```

---

## 96. What is Event Capturing?

Event capturing is **reverse of bubbling (parent → child)**

---

### ✅ Example:

```javascript id="3nn4ws"
parent.addEventListener("click", () => console.log("Parent"), true);
child.addEventListener("click", () => console.log("Child"), true);
```

👉 Output:

```text id="gkgh8y"
Parent
Child
```

---

### 🔥 Flow:

```text id="m6q4mv"
Capturing → Target → Bubbling
```

---

## 97. What is Garbage Collection?

Garbage collection is an automatic process where JavaScript **frees memory of unused variables**

---

### 🔥 Example:

```javascript id="o6vyb8"
let obj = { name: "Ashish" };

obj = null; // eligible for garbage collection
```

---

### 🧠 Key Idea:

👉 JS uses **Mark-and-Sweep algorithm**

---

## 98. What is WeakMap?

WeakMap is a collection of **key-value pairs where keys must be objects** and are weakly referenced

---

### 🔥 Key Features:

* Keys are objects only
* Not iterable
* Helps avoid memory leaks

---

### ✅ Example:

```javascript id="a4hp1q"
let wm = new WeakMap();

let obj = {};
wm.set(obj, "data");

obj = null; // garbage collected
```

---

## 99. What is WeakSet?

WeakSet is a collection of **unique objects (only objects allowed)**

---

### 🔥 Key Features:

* Only objects
* Not iterable
* Weak reference

---

### ✅ Example:

```javascript id="f4nfls"
let ws = new WeakSet();

let obj = {};
ws.add(obj);

obj = null; // GC removes it
```

---

## 100. What is Symbol?

Symbol is a **unique and immutable primitive data type**

---

### 🔥 Key Points:

* Always unique
* Used as object keys
* Avoid property conflicts

---

### ✅ Example:

```javascript id="d2kqqx"
const id1 = Symbol("id");
const id2 = Symbol("id");

console.log(id1 === id2); // false
```

---

### 🔥 Object Example:

```javascript id="nrf9f1"
const obj = {
  [Symbol("id")]: 123
};
```

---

# 🚀 Final Interview Tips (VERY IMPORTANT 🔥)

If interviewer goes deep, mention:

* Debounce vs Throttle → **VERY commonly asked**
* Memoization → performance optimization
* Currying → functional programming
* Event flow → Capturing → Target → Bubbling
* WeakMap/WeakSet → memory optimization
* Symbol → unique keys (used in libraries)

---

# 🔥 Most Asked Combo Questions

👉 Difference between:

* Debounce vs Throttle
* WeakMap vs Map
* Bubbling vs Capturing

---
Here are **clear, detailed, interview-ready answers** for **Error Handling in JavaScript** 👇

---

# 🚀 JavaScript Interview Answers

## 📌 11. Error Handling (Detailed)

---

## 101. What is try-catch?

`try...catch` is used to **handle runtime errors (exceptions)** so that your program doesn’t crash.

---

### 🔥 Structure:

```javascript
try {
  // risky code
} catch (error) {
  // handle error
}
```

---

### ✅ Example:

```javascript
try {
  let result = x + 10; // x is not defined
} catch (error) {
  console.log("Error occurred:", error.message);
}
```

---

### 🔥 Key Points:

* `try` → contains code that may throw error
* `catch` → handles the error
* Prevents app from crashing

---

## 102. What is finally?

`finally` block always executes **whether error occurs or not**

---

### 🔥 Syntax:

```javascript
try {
  // code
} catch (err) {
  // handle error
} finally {
  // always runs
}
```

---

### ✅ Example:

```javascript
try {
  console.log("Try block");
} catch (e) {
  console.log("Error");
} finally {
  console.log("Always executed");
}
```

---

### 🔥 Use Case:

* Cleanup operations
* Closing resources (files, DB connections)

---

## 103. What is Custom Error?

Custom errors are **user-defined errors** to provide better control and meaningful messages.

---

### ✅ Example:

```javascript
function withdraw(amount) {
  if (amount > 1000) {
    throw new Error("Limit exceeded");
  }
  return "Success";
}
```

---

### 🔥 Advanced (Custom Class):

```javascript
class CustomError extends Error {
  constructor(message) {
    super(message);
    this.name = "CustomError";
  }
}

throw new CustomError("Something went wrong");
```

---

## 104. What is throw?

`throw` is used to **manually generate an error**

---

### ✅ Example:

```javascript
function checkAge(age) {
  if (age < 18) {
    throw "You must be 18+";
  }
  return "Allowed";
}
```

---

### 🔥 Best Practice:

```javascript
throw new Error("Invalid input");
```

👉 Always throw Error objects instead of strings

---

## 105. What is Error Object?

The Error object contains **information about an error**

---

### 🔥 Properties:

* `name` → type of error
* `message` → error message
* `stack` → stack trace

---

### ✅ Example:

```javascript
try {
  JSON.parse("invalid");
} catch (err) {
  console.log(err.name);    // SyntaxError
  console.log(err.message); // Unexpected token
}
```

---

# 🚀 Final Interview Tips (IMPORTANT 🔥)

If interviewer goes deeper, mention:

* Use `try-catch` only for **runtime errors (not syntax errors)**
* Always use `finally` for cleanup
* Prefer:

  ```javascript
  throw new Error("message");
  ```
* Custom errors improve debugging

---

# 🔥 Most Asked Follow-Up

👉 Difference between:

* `throw` vs `return`
* `Error` vs `Custom Error`

---
Here are **interview-level, practical explanations (VERY IMPORTANT 🔥)** for **Performance & Optimization** 👇

---

# 🚀 JavaScript Interview Answers

## 📌 12. Performance & Optimization (Detailed)

---

## 106. How to optimize JavaScript performance?

Optimizing JS means making your app **faster, efficient, and responsive**.

### 🔥 Key Techniques:

* Minimize DOM manipulation
* Use **debouncing/throttling**
* Use **async/await properly**
* Avoid global variables
* Use **code splitting & lazy loading**
* Optimize loops & algorithms
* Use caching

---

### ✅ Example (Bad vs Good):

```javascript
// ❌ Bad (multiple DOM updates)
for (let i = 0; i < 1000; i++) {
  document.body.innerHTML += "<p>Hello</p>";
}

// ✅ Good (single update)
let html = "";
for (let i = 0; i < 1000; i++) {
  html += "<p>Hello</p>";
}
document.body.innerHTML = html;
```

---

## 107. What is Lazy Loading?

Lazy loading means **loading resources only when needed**

---

### 🔥 Use Case:

* Images
* Components (React)

---

### ✅ Example:

```html
<img src="image.jpg" loading="lazy" />
```

---

### 🔥 Benefit:

* Faster initial load
* Saves bandwidth

---

## 108. What is Code Splitting?

Code splitting means **breaking large JS bundles into smaller chunks**

---

### 🔥 Use Case:

* Load only required code

---

### ✅ Example (React):

```javascript
const Home = React.lazy(() => import("./Home"));
```

---

### 🔥 Benefit:

* Improves performance
* Faster page load

---

## 109. What is Tree Shaking?

Tree shaking removes **unused code during build process**

---

### 🔥 Example:

```javascript
// utils.js
export const a = () => {};
export const b = () => {};
```

```javascript
// app.js
import { a } from "./utils";
```

👉 `b` is removed from final bundle

---

### 🔥 Tools:

* Webpack
* Vite

---

## 110. What is Memory Leak?

Memory leak happens when **unused memory is not released**

---

### 🔥 Causes:

* Unremoved event listeners
* Closures holding references
* Timers not cleared

---

### ✅ Example:

```javascript
let arr = [];
setInterval(() => {
  arr.push(new Array(1000000));
}, 1000);
```

👉 Memory keeps increasing ❗

---

## 111. How to avoid Memory Leaks?

### 🔥 Best Practices:

* Remove event listeners
* Clear timers (`clearInterval`, `clearTimeout`)
* Avoid global variables
* Use WeakMap/WeakSet
* Dereference unused objects

---

### ✅ Example:

```javascript
const id = setInterval(() => {}, 1000);

clearInterval(id); // cleanup
```

---

## 112. What is Web Worker?

Web Worker allows JS to run in **background thread**

---

### 🔥 Why?

JS is single-threaded → heavy tasks block UI

---

### ✅ Example:

```javascript
const worker = new Worker("worker.js");

worker.postMessage("start");

worker.onmessage = (e) => {
  console.log(e.data);
};
```

---

### 🔥 Benefit:

* Smooth UI
* Heavy computation handling

---

## 113. What is Caching?

Caching stores data **temporarily to reuse later instead of re-fetching**

---

### 🔥 Types:

* Browser cache
* API cache
* Memory cache

---

### ✅ Example:

```javascript
if (cache[data]) {
  return cache[data];
}
```

---

### 🔥 Benefit:

* Faster response
* Reduced API calls

---

## 114. What is CDN?

CDN = **Content Delivery Network**

It is a network of servers that **deliver content from nearest location**

---

### 🔥 Examples:

* Cloudflare
* AWS CloudFront

---

### 🔥 Benefit:

* Faster loading
* Reduced latency

---

## 115. How to reduce API calls?

---

### 🔥 Techniques:

* Debouncing API calls
* Caching responses
* Pagination / infinite scroll
* Avoid duplicate calls
* Use batching

---

### ✅ Example (Debounce):

```javascript
const search = debounce((query) => {
  fetch(`/api?q=${query}`);
}, 500);
```

---

# 🚀 Final Interview Tips (VERY IMPORTANT 🔥)

If interviewer goes deeper, mention:

* Performance = **user experience**
* Use:

  * Lazy loading + code splitting
  * Caching + CDN
* Avoid:

  * Memory leaks
  * Unnecessary re-renders

---

# 🔥 MOST ASKED QUESTIONS

👉 Difference between:

* Lazy loading vs Code splitting
* Debounce vs Throttle
* Cache vs CDN

---
Here are **clear, interview-ready + real-world explanations (VERY IMPORTANT 🔥)** for **JavaScript Security** 👇

---

# 🚀 JavaScript Interview Answers

## 📌 13. Security (Detailed)

---

## 116. What is XSS?

XSS (Cross-Site Scripting) is a vulnerability where attackers **inject malicious JavaScript into a website**, which runs in other users’ browsers.

---

### 🔥 Types:

* Stored XSS
* Reflected XSS
* DOM-based XSS

---

### ❌ Example:

```html
<input value="<script>alert('Hacked')</script>" />
```

---

### 🔥 Impact:

* Steal cookies
* Session hijacking
* Redirect users

---

### ✅ Prevention:

* Escape/encode user input
* Use libraries/frameworks (React auto-escapes)
* Use CSP (Content Security Policy)

---

## 117. What is CSRF?

CSRF (Cross-Site Request Forgery) tricks a user into **performing unwanted actions on a trusted site**

---

### 🔥 Example:

User logged into bank → attacker sends hidden request → money transfer happens

---

### 🔥 Impact:

* Unauthorized transactions
* Data modification

---

### ✅ Prevention:

* CSRF tokens
* SameSite cookies
* Authentication checks

---

## 118. What is CORS?

CORS (Cross-Origin Resource Sharing) allows/restricts **requests between different origins**

---

### 🔥 Example:

Frontend → `localhost:3000`
Backend → `api.com`

👉 Different origins → blocked unless allowed

---

### ✅ Server Example:

```javascript
app.use(cors({
  origin: "http://localhost:3000"
}));
```

---

### 🔥 Headers:

* `Access-Control-Allow-Origin`
* `Access-Control-Allow-Methods`

---

## 119. What is Same-Origin Policy?

Same-Origin Policy is a browser security rule that **blocks access between different origins**

---

### 🔥 Origin = Protocol + Domain + Port

---

### ✅ Example:

* `https://example.com`
* `http://example.com` ❌ (different protocol)

---

### 🔥 Purpose:

* Prevent malicious websites from accessing sensitive data

---

## 120. How to secure API calls?

---

### 🔥 Best Practices:

### 🔹 1. Use HTTPS

* Encrypts data

---

### 🔹 2. Authentication

* JWT (JSON Web Token)
* OAuth

---

### 🔹 3. Authorization

* Role-based access

---

### 🔹 4. Validate Input

```javascript
if (!email.includes("@")) {
  throw new Error("Invalid email");
}
```

---

### 🔹 5. Rate Limiting

* Prevent abuse

---

### 🔹 6. Use Secure Headers

* Helmet (Node.js)

---

### 🔹 7. Avoid exposing secrets

❌ Never expose API keys in frontend

---

### 🔹 8. Use CORS properly

* Allow only trusted origins

---

# 🚀 Final Interview Tips (VERY IMPORTANT 🔥)

If interviewer goes deep, say:

* XSS → inject script
* CSRF → trick user action
* CORS → allow cross-origin
* Same-Origin Policy → restrict access

---

# 🔥 Most Asked Differences

👉 XSS vs CSRF
👉 CORS vs Same-Origin Policy

---
Here are **scenario-based, coding-focused answers (VERY IMPORTANT for interviews 🔥)** with clean logic + examples 👇

---

# 🚀 JavaScript Interview Answers

## 📌 14. Scenario-Based Questions (Coding + Explanation)

---

## 121. How to implement a counter without global variable?

👉 Use **closure**

### ✅ Example:

```javascript
function createCounter() {
  let count = 0;

  return function () {
    return ++count;
  };
}

const counter = createCounter();

console.log(counter()); // 1
console.log(counter()); // 2
```

### 🔥 Why:

* `count` is private (not global)
* Maintained using closure

---

## 122. How to implement debounce function?

### ✅ Example:

```javascript
function debounce(fn, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);

    timer = setTimeout(() => {
      fn.apply(this, args);
    }, delay);
  };
}
```

### 🔥 Use:

* Search input
* API calls optimization

---

## 123. How to reverse a string?

### ✅ Method 1:

```javascript
let str = "hello";

let reversed = str.split("").reverse().join("");
console.log(reversed); // olleh
```

---

### ✅ Method 2 (manual):

```javascript
function reverse(str) {
  let res = "";
  for (let i = str.length - 1; i >= 0; i--) {
    res += str[i];
  }
  return res;
}
```

---

## 124. How to remove duplicates from array?

### ✅ Using Set:

```javascript
const arr = [1, 2, 2, 3];

const unique = [...new Set(arr)];
console.log(unique); // [1,2,3]
```

---

### ✅ Using filter:

```javascript
const unique = arr.filter((item, index) => arr.indexOf(item) === index);
```

---

## 125. How to flatten an array?

### ✅ Using flat():

```javascript
const arr = [1, [2, [3]]];

console.log(arr.flat(Infinity)); // [1,2,3]
```

---

### ✅ Recursive:

```javascript
function flatten(arr) {
  return arr.reduce((acc, val) =>
    Array.isArray(val)
      ? acc.concat(flatten(val))
      : acc.concat(val),
  []);
}
```

---

## 126. How to check palindrome?

### ✅ Example:

```javascript
function isPalindrome(str) {
  let reversed = str.split("").reverse().join("");
  return str === reversed;
}

console.log(isPalindrome("madam")); // true
```

---

### 🔥 Case-insensitive:

```javascript
str = str.toLowerCase();
```

---

## 127. How to find second largest number?

### ✅ Example:

```javascript
const arr = [10, 5, 8, 20];

const sorted = [...new Set(arr)].sort((a, b) => b - a);

console.log(sorted[1]); // second largest
```

---

### 🔥 Optimized:

```javascript
function secondLargest(arr) {
  let first = -Infinity, second = -Infinity;

  for (let num of arr) {
    if (num > first) {
      second = first;
      first = num;
    } else if (num > second && num !== first) {
      second = num;
    }
  }

  return second;
}
```

---

## 128. How to deep clone an object?

### ✅ Modern:

```javascript
const clone = structuredClone(obj);
```

---

### ✅ Old:

```javascript
const clone = JSON.parse(JSON.stringify(obj));
```

---

### 🔥 Note:

* JSON method fails for:

  * functions
  * undefined
  * Date

---

## 129. How to implement custom map function?

### ✅ Example:

```javascript
Array.prototype.myMap = function (callback) {
  let result = [];

  for (let i = 0; i < this.length; i++) {
    result.push(callback(this[i], i, this));
  }

  return result;
};
```

---

### ✅ Usage:

```javascript
[1, 2, 3].myMap(x => x * 2); // [2,4,6]
```

---

## 130. How to implement custom reduce function?

### ✅ Example:

```javascript
Array.prototype.myReduce = function (callback, initial) {
  let acc = initial;

  for (let i = 0; i < this.length; i++) {
    acc = acc !== undefined
      ? callback(acc, this[i], i, this)
      : this[i];
  }

  return acc;
};
```

---

### ✅ Usage:

```javascript
[1, 2, 3].myReduce((a, b) => a + b, 0); // 6
```

---

# 🚀 Final Interview Tips (VERY IMPORTANT 🔥)

If interviewer asks coding:

* Always explain:

  1. Approach
  2. Time complexity
  3. Edge cases

---

### 🔥 MUST PRACTICE:

* Debounce
* Flatten array
* Second largest
* Custom map/reduce

---
Here are **very important output-based questions (🔥 frequently asked in interviews)** with **clear explanation + reasoning** 👇

---

# 🚀 JavaScript Interview Answers

## 📌 15. Coding Output-Based Questions

---

## 131. What will be the output of this closure example?

### ✅ Code:

```javascript
function outer() {
  let x = 10;
  return function () {
    console.log(x);
  };
}

const fn = outer();
fn();
```

### ✅ Output:

```text
10
```

### 🔥 Explanation:

* Inner function **remembers `x` (closure)**
* Even after `outer()` finishes

---

## 132. What will be output of setTimeout loop?

### ❌ Code (var):

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1000);
}
```

### ✅ Output:

```text
3
3
3
```

### 🔥 Why:

* `var` is function-scoped
* All callbacks share same `i` (final value = 3)

---

## 133. What will be output of var vs let loop?

### ✅ Code (let):

```javascript
for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1000);
}
```

### ✅ Output:

```text
0
1
2
```

### 🔥 Why:

* `let` is block-scoped
* New `i` created each iteration

---

## 134. What happens when Promise.reject?

### ✅ Code:

```javascript
Promise.reject("Error")
  .then(res => console.log(res))
  .catch(err => console.log(err));
```

### ✅ Output:

```text
Error
```

### 🔥 Explanation:

* Promise goes to **rejected state**
* `.catch()` handles it

---

## 135. What is output of typeof null?

### ✅ Code:

```javascript
console.log(typeof null);
```

### ✅ Output:

```text
object
```

### 🔥 Explanation:

* Historical bug in JS
* `null` is primitive but returns `"object"`

---

## 136. What happens when you add number + string?

### ✅ Code:

```javascript
console.log(5 + "5");
```

### ✅ Output:

```text
"55"
```

### 🔥 Explanation:

* Type coercion → number converted to string

---

## 137. What is output of [] + {}?

### ✅ Code:

```javascript
console.log([] + {});
```

### ✅ Output:

```text
"[object Object]"
```

### 🔥 Explanation:

* `[]` → ""
* `{}` → "[object Object]"
* Result → string concatenation

---

## 138. What is output of {} + []?

### ✅ Code:

```javascript
console.log({} + []);
```

### ✅ Output:

```text
0   (in some environments)
```

### 🔥 Explanation:

* `{}` treated as block
* `+[]` → 0

👉 So result = 0

---

## 139. What is output of NaN === NaN?

### ✅ Code:

```javascript
console.log(NaN === NaN);
```

### ✅ Output:

```text
false
```

### 🔥 Explanation:

* NaN is **not equal to anything (even itself)**

---

## 140. What is output of 0.1 + 0.2?

### ✅ Code:

```javascript
console.log(0.1 + 0.2);
```

### ✅ Output:

```text
0.30000000000000004
```

### 🔥 Explanation:

* Floating point precision issue (binary representation)

---

# 🚀 Final Interview Tips (VERY IMPORTANT 🔥)

These are **tricky + high-probability questions**, so remember:

### 🔥 MUST REMEMBER:

* `var` vs `let` in loops
* `NaN !== NaN`
* `typeof null → object`
* `0.1 + 0.2` precision issue
* `[] + {}` weird coercion

---

# 🎯 PRO TIP

If interviewer asks **WHY**, always explain:

* Scope (var vs let)
* Type coercion
* JS engine behavior

---
Here are **short, crisp, one-line answers (Rapid Fire 🔥)** — perfect for interviews 👇

---

# 🚀 JavaScript Interview Answers

## 📌 16. Real Interview Rapid Fire

---

## 141. Difference between synchronous and asynchronous?

👉 **Synchronous:** Executes code line by line (blocking)
👉 **Asynchronous:** Executes tasks without blocking (non-blocking)

---

## 142. What is event loop in one line?

👉 Event loop is a mechanism that **moves async tasks from queue to call stack when it's empty**

---

## 143. What is closure in one line?

👉 Closure is a function that **remembers variables from its outer scope**

---

## 144. What is promise in one line?

👉 Promise is an object that **represents future success or failure of an async operation**

---

## 145. What is async/await in one line?

👉 async/await is a **clean way to handle promises using synchronous-like syntax**

---

## 146. What is arrow function in one line?

👉 Arrow function is a **short syntax function that inherits `this` from parent scope**

---

## 147. What is spread operator?

👉 Spread operator (`...`) is used to **expand elements of arrays/objects**

---

## 148. What is destructuring?

👉 Destructuring is extracting **values from arrays/objects into variables**

---

## 149. What is callback?

👉 Callback is a **function passed into another function to be executed later**

---

## 150. What is higher order function?

👉 Higher-order function is a function that **takes or returns another function**

---

# 🚀 Final Tip (VERY IMPORTANT 🔥)

In rapid fire:

* Keep answers **short + confident**
* Add **1 keyword explanation if asked further**

---

# 🎯 YOU ARE INTERVIEW READY 💯🔥

You now have:
✅ **150 JavaScript Questions + Answers COMPLETE**
✅ Covers **Theory + Coding + Advanced + Rapid Fire**

---
