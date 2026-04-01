# ✅ 1. Print numbers from 1 to 100

### 🔹 Approach 1: Simple loop

```javascript
for (let i = 1; i <= 100; i++) {
  console.log(i);
}
```

### 🔹 Approach 2: Using Array + built-in

```javascript
Array.from({ length: 100 }, (_, i) => i + 1).forEach((num) => console.log(num));
```

---

# ✅ 2. Print even numbers from 1 to 100

### 🔹 Approach 1: Using condition

```javascript
for (let i = 1; i <= 100; i++) {
  if (i % 2 === 0) {
    console.log(i);
  }
}
```

### 🔹 Approach 2: Optimized loop

```javascript
for (let i = 2; i <= 100; i += 2) {
  console.log(i);
}
```

---

# ✅ 3. Swap two numbers without third variable

### 🔹 Approach 1: Using arithmetic

```javascript
let a = 5,
  b = 10;

a = a + b;
b = a - b;
a = a - b;

console.log(a, b);
```

### 🔹 Approach 2: Using destructuring (modern JS)

```javascript
let a = 5,
  b = 10;
[a, b] = [b, a];
console.log(a, b);
```

---

# ✅ 4. Factorial of a number

### 🔹 Approach 1: Loop

```javascript
let n = 5;
let fact = 1;

for (let i = 1; i <= n; i++) {
  fact *= i;
}

console.log(fact);
```

### 🔹 Approach 2: Function

```javascript
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}

console.log(factorial(5));
```

---

# ✅ 5. Check if number is prime

### 🔹 Explanation:

Prime = divisible only by 1 and itself

### 🔹 Approach 1: Basic

```javascript
let num = 7;
let isPrime = true;

if (num <= 1) isPrime = false;

for (let i = 2; i < num; i++) {
  if (num % i === 0) {
    isPrime = false;
    break;
  }
}

console.log(isPrime);
```

### 🔹 Approach 2: Optimized (√n)

```javascript
function isPrime(num) {
  if (num <= 1) return false;

  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }

  return true;
}

console.log(isPrime(7));
```

---

# ✅ 6. Fibonacci Series

### 🔹 Approach 1: Loop

```javascript
let n = 10;
let a = 0,
  b = 1;

for (let i = 0; i < n; i++) {
  console.log(a);
  let next = a + b;
  a = b;
  b = next;
}
```

### 🔹 Approach 2: Function

```javascript
function fibonacci(n) {
  let arr = [0, 1];

  for (let i = 2; i < n; i++) {
    arr[i] = arr[i - 1] + arr[i - 2];
  }

  return arr;
}

console.log(fibonacci(10));
```

---

# ✅ 7. Largest of three numbers

### 🔹 Approach 1: If-else

```javascript
let a = 10,
  b = 25,
  c = 15;

let largest;

if (a >= b && a >= c) {
  largest = a;
} else if (b >= a && b >= c) {
  largest = b;
} else {
  largest = c;
}

console.log(largest);
```

### 🔹 Approach 2: Built-in

```javascript
console.log(Math.max(10, 25, 15));
```

---

# ✅ 8. Reverse a number

### 🔹 Approach 1: Loop

```javascript
let num = 1234;
let rev = 0;

while (num > 0) {
  let digit = num % 10;
  rev = rev * 10 + digit;
  num = Math.floor(num / 10);
}

console.log(rev);
```

### 🔹 Approach 2: Using string (built-in)

```javascript
let num = 1234;
let reversed = Number(num.toString().split("").reverse().join(""));
console.log(reversed);
```

---

# ✅ 9. Count digits in a number

### 🔹 Approach 1: Loop

```javascript
let num = 12345;
let count = 0;

while (num > 0) {
  count++;
  num = Math.floor(num / 10);
}

console.log(count);
```

### 🔹 Approach 2: Built-in

```javascript
let num = 12345;
console.log(num.toString().length);
```

---

# ✅ 10. Armstrong Number

### 🔹 Explanation:

Example: 153
👉 1³ + 5³ + 3³ = 153

### 🔹 Approach 1: Loop

```javascript
let num = 153;
let sum = 0;
let temp = num;

while (temp > 0) {
  let digit = temp % 10;
  sum += digit ** 3;
  temp = Math.floor(temp / 10);
}

console.log(sum === num);
```

### 🔹 Approach 2: Dynamic (any digits)

```javascript
function isArmstrong(num) {
  let digits = num.toString().split("");
  let power = digits.length;

  let sum = digits.reduce((acc, d) => acc + Math.pow(d, power), 0);

  return sum === num;
}

console.log(isArmstrong(153));
```

---

# ✅ 11. Reverse a string

### 🔹 Approach 1: Using loop

```javascript
let str = "hello";
let reversed = "";

for (let i = str.length - 1; i >= 0; i--) {
  reversed += str[i];
}

console.log(reversed);
```

### 🔹 Approach 2: Built-in

```javascript
let str = "hello";
console.log(str.split("").reverse().join(""));
```

---

# ✅ 12. Check if string is palindrome

👉 Same forward and backward (e.g., "madam")

### 🔹 Approach 1: Using reverse

```javascript
let str = "madam";
let reversed = str.split("").reverse().join("");

console.log(str === reversed);
```

### 🔹 Approach 2: Loop (optimized)

```javascript
function isPalindrome(str) {
  let left = 0;
  let right = str.length - 1;

  while (left < right) {
    if (str[left] !== str[right]) return false;
    left++;
    right--;
  }

  return true;
}

console.log(isPalindrome("madam"));
```

---

# ✅ 13. Count vowels in a string

### 🔹 Approach 1: Loop

```javascript
let str = "javascript";
let count = 0;

for (let char of str.toLowerCase()) {
  if ("aeiou".includes(char)) {
    count++;
  }
}

console.log(count);
```

### 🔹 Approach 2: Using regex

```javascript
let str = "javascript";
let count = str.match(/[aeiou]/gi)?.length || 0;
console.log(count);
```

---

# ✅ 14. Remove duplicates from string

### 🔹 Approach 1: Using Set

```javascript
let str = "programming";
let result = [...new Set(str)].join("");
console.log(result);
```

### 🔹 Approach 2: Loop

```javascript
let str = "programming";
let result = "";

for (let char of str) {
  if (!result.includes(char)) {
    result += char;
  }
}

console.log(result);
```

---

# ✅ 15. Find longest word in sentence

### 🔹 Approach 1

```javascript
let str = "I am learning JavaScript programming";

let words = str.split(" ");
let longest = "";

for (let word of words) {
  if (word.length > longest.length) {
    longest = word;
  }
}

console.log(longest);
```

### 🔹 Approach 2: Built-in

```javascript
let str = "I am learning JavaScript programming";

let longest = str.split(" ").reduce((a, b) => (b.length > a.length ? b : a));

console.log(longest);
```

---

# ✅ 16. Capitalize first letter of each word

### 🔹 Approach 1

```javascript
let str = "hello world";

let result = str
  .split(" ")
  .map((word) => word.charAt(0).toUpperCase() + word.slice(1))
  .join(" ");

console.log(result);
```

---

# ✅ 17. Check if two strings are anagrams

👉 Same characters, different order
Example: "listen" & "silent"

### 🔹 Approach 1: Sorting

```javascript
function isAnagram(str1, str2) {
  let s1 = str1.split("").sort().join("");
  let s2 = str2.split("").sort().join("");

  return s1 === s2;
}

console.log(isAnagram("listen", "silent"));
```

### 🔹 Approach 2: Frequency count

```javascript
function isAnagram(str1, str2) {
  if (str1.length !== str2.length) return false;

  let map = {};

  for (let char of str1) {
    map[char] = (map[char] || 0) + 1;
  }

  for (let char of str2) {
    if (!map[char]) return false;
    map[char]--;
  }

  return true;
}
```

---

# ✅ 18. Replace all spaces with hyphen

### 🔹 Approach 1

```javascript
let str = "hello world javascript";
console.log(str.replace(/ /g, "-"));
```

### 🔹 Approach 2

```javascript
console.log(str.split(" ").join("-"));
```

---

# ✅ 19. Find frequency of characters

### 🔹 Approach 1

```javascript
let str = "hello";
let freq = {};

for (let char of str) {
  freq[char] = (freq[char] || 0) + 1;
}

console.log(freq);
```

### 🔹 Output:

```
{ h:1, e:1, l:2, o:1 }
```

---

# ✅ 20. Remove special characters

### 🔹 Approach 1: Regex

```javascript
let str = "hello@123#world!";
let clean = str.replace(/[^a-zA-Z0-9 ]/g, "");
console.log(clean);
```

---

# ✅ 21. Find maximum number in array

### 🔹 Logic:

Compare all elements and keep track of max.

```javascript
let arr = [3, 7, 2, 9, 5];
let max = arr[0];

for (let num of arr) {
  if (num > max) max = num;
}

console.log(max);
```

### 🔹 Built-in

```javascript
console.log(Math.max(...arr));
```

---

# ✅ 22. Find minimum number in array

```javascript
let min = arr[0];

for (let num of arr) {
  if (num < min) min = num;
}

console.log(min);
```

### 🔹 Built-in

```javascript
console.log(Math.min(...arr));
```

---

# ✅ 23. Remove duplicates from array

### 🔹 Using Set

```javascript
let arr = [1, 2, 2, 3, 4, 4];
let unique = [...new Set(arr)];
console.log(unique);
```

---

# ✅ 24. Reverse an array

### 🔹 Manual

```javascript
let arr = [1, 2, 3];
let reversed = [];

for (let i = arr.length - 1; i >= 0; i--) {
  reversed.push(arr[i]);
}

console.log(reversed);
```

### 🔹 Built-in

```javascript
console.log(arr.reverse());
```

---

# ✅ 25. Sort array ascending & descending

```javascript
let arr = [5, 2, 9, 1];

// Ascending
arr.sort((a, b) => a - b);

// Descending
arr.sort((a, b) => b - a);
```

---

# ✅ 26. Find second largest number

### 🔹 Approach

```javascript
let arr = [10, 20, 5, 8];

let unique = [...new Set(arr)];
unique.sort((a, b) => b - a);

console.log(unique[1]);
```

---

# ✅ 27. Merge two arrays

```javascript
let a = [1, 2];
let b = [3, 4];

let merged = [...a, ...b];
console.log(merged);
```

---

# ✅ 28. Flatten nested array

```javascript
let arr = [1, [2, [3, 4]]];

// Built-in
console.log(arr.flat(Infinity));
```

---

# ✅ 29. Find missing number in array

👉 Example: [1,2,4,5] → missing 3

```javascript
let arr = [1, 2, 4, 5];
let n = 5;

let total = (n * (n + 1)) / 2;
let sum = arr.reduce((a, b) => a + b, 0);

console.log(total - sum);
```

---

# ✅ 30. Find intersection of two arrays

```javascript
let a = [1, 2, 3];
let b = [2, 3, 4];

let result = a.filter((x) => b.includes(x));
console.log(result);
```

---

# ✅ 31. Rotate array by k positions

👉 Right rotation

```javascript
let arr = [1, 2, 3, 4, 5];
let k = 2;

k = k % arr.length;

let rotated = arr.slice(-k).concat(arr.slice(0, -k));
console.log(rotated);
```

---

# ✅ 32. Find sum of array elements

```javascript
let arr = [1, 2, 3, 4];

let sum = arr.reduce((a, b) => a + b, 0);
console.log(sum);
```

---

# ✅ 33. Find duplicate elements

```javascript
let arr = [1, 2, 3, 2, 4, 1];
let seen = new Set();
let duplicates = new Set();

for (let num of arr) {
  if (seen.has(num)) duplicates.add(num);
  else seen.add(num);
}

console.log([...duplicates]);
```

---

# ✅ 34. Count frequency of elements

```javascript
let arr = [1, 2, 2, 3, 1, 1];
let freq = {};

for (let num of arr) {
  freq[num] = (freq[num] || 0) + 1;
}

console.log(freq);
```

---

# ✅ 35. Move zeros to end

```javascript
let arr = [0, 1, 0, 3, 12];

let nonZero = arr.filter((x) => x !== 0);
let zeros = arr.filter((x) => x === 0);

console.log([...nonZero, ...zeros]);
```

---

# ✅ 36. Debounce Function

### 🔹 Logic:

Delay execution until user stops triggering (used in search input)

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

// Usage
const search = debounce(() => console.log("API Call"), 500);
```

---

# ✅ 37. Throttle Function

### 🔹 Logic:

Limit execution (run once per interval)

```javascript
function throttle(fn, limit) {
  let lastCall = 0;

  return function (...args) {
    let now = Date.now();

    if (now - lastCall >= limit) {
      lastCall = now;
      fn.apply(this, args);
    }
  };
}
```

---

# ✅ 38. Custom map()

### 🔹 Logic:

Apply function to each element → return new array

```javascript
Array.prototype.myMap = function (callback) {
  let result = [];

  for (let i = 0; i < this.length; i++) {
    result.push(callback(this[i], i, this));
  }

  return result;
};

// Usage
[1, 2, 3].myMap((x) => x * 2);
```

---

# ✅ 39. Custom filter()

```javascript
Array.prototype.myFilter = function (callback) {
  let result = [];

  for (let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) {
      result.push(this[i]);
    }
  }

  return result;
};
```

---

# ✅ 40. Custom reduce()

```javascript
Array.prototype.myReduce = function (callback, initial) {
  let acc = initial ?? this[0];
  let start = initial ? 0 : 1;

  for (let i = start; i < this.length; i++) {
    acc = callback(acc, this[i], i, this);
  }

  return acc;
};
```

---

# ✅ 41. Closure Example

### 🔹 Logic:

Function remembers its outer scope

```javascript
function outer() {
  let count = 0;

  return function inner() {
    count++;
    console.log(count);
  };
}

const fn = outer();
fn(); // 1
fn(); // 2
```

---

# ✅ 42. Counter using closure

```javascript
function createCounter() {
  let count = 0;

  return {
    increment: () => ++count,
    decrement: () => --count,
    get: () => count,
  };
}

const counter = createCounter();

console.log(counter.increment()); // 1
console.log(counter.increment()); // 2
console.log(counter.get()); // 2
```

---

# ✅ 43. Memoization

### 🔹 Logic:

Cache results → improve performance

```javascript
function memoize(fn) {
  let cache = {};

  return function (...args) {
    let key = JSON.stringify(args);

    if (cache[key]) return cache[key];

    let result = fn(...args);
    cache[key] = result;

    return result;
  };
}

// Example
const add = (a, b) => a + b;
const memoAdd = memoize(add);

console.log(memoAdd(2, 3)); // calculated
console.log(memoAdd(2, 3)); // cached
```

---

# ✅ 44. Currying Function

### 🔹 Logic:

Convert function with multiple args → nested functions

```javascript
function curry(a) {
  return function (b) {
    return function (c) {
      return a + b + c;
    };
  };
}

console.log(curry(1)(2)(3)); // 6
```

### 🔹 Modern (arrow)

```javascript
const curry = (a) => (b) => (c) => a + b + c;
```

---

# ✅ 45. Deep Clone Function

### 🔹 Basic (Interview level)

```javascript
function deepClone(obj) {
  return JSON.parse(JSON.stringify(obj));
}
```

### 🔹 Advanced (handles objects/arrays)

```javascript
function deepClone(obj) {
  if (obj === null || typeof obj !== "object") return obj;

  let copy = Array.isArray(obj) ? [] : {};

  for (let key in obj) {
    copy[key] = deepClone(obj[key]);
  }

  return copy;
}
```

---

# ✅ 46. Merge two objects

### 🔹 Using spread (most common)

```javascript id="5a9e1k"
let obj1 = { a: 1 };
let obj2 = { b: 2 };

let merged = { ...obj1, ...obj2 };
console.log(merged);
```

### 🔹 Using Object.assign

```javascript id="dy9r6u"
let merged = Object.assign({}, obj1, obj2);
```

---

# ✅ 47. Deep copy object

### 🔹 Basic (interview level)

```javascript id="8h6d4s"
let copy = JSON.parse(JSON.stringify(obj));
```

### 🔹 Recursive (better)

```javascript id="n2g0rq"
function deepClone(obj) {
  if (obj === null || typeof obj !== "object") return obj;

  let copy = Array.isArray(obj) ? [] : {};

  for (let key in obj) {
    copy[key] = deepClone(obj[key]);
  }

  return copy;
}
```

---

# ✅ 48. Convert object to array

```javascript id="j9nq8k"
let obj = { a: 1, b: 2 };

// Keys
Object.keys(obj);

// Values
Object.values(obj);

// Entries
Object.entries(obj);
```

---

# ✅ 49. Convert array to object

```javascript id="z2h7tm"
let arr = [
  ["a", 1],
  ["b", 2],
];

let obj = Object.fromEntries(arr);
console.log(obj);
```

---

# ✅ 50. Find nested property safely

### 🔹 Using optional chaining

```javascript id="6p3w4r"
let user = { address: { city: "Mumbai" } };

console.log(user?.address?.city);
```

---

# ✅ 51. Remove property from object

```javascript id="3r5u1q"
let obj = { a: 1, b: 2 };

delete obj.b;
console.log(obj);
```

### 🔹 Without mutation

```javascript id="9xk1pz"
let { b, ...rest } = obj;
console.log(rest);
```

---

# ✅ 52. Compare two objects

### 🔹 Simple (not deep)

```javascript id="c0l9qv"
JSON.stringify(obj1) === JSON.stringify(obj2);
```

### 🔹 Deep compare

```javascript id="8f3d2m"
function isEqual(a, b) {
  if (a === b) return true;

  if (typeof a !== "object" || typeof b !== "object") return false;

  let keysA = Object.keys(a);
  let keysB = Object.keys(b);

  if (keysA.length !== keysB.length) return false;

  for (let key of keysA) {
    if (!isEqual(a[key], b[key])) return false;
  }

  return true;
}
```

---

# ✅ 53. Count object keys

```javascript id="7n2m9d"
let obj = { a: 1, b: 2, c: 3 };

console.log(Object.keys(obj).length);
```

---

# ✅ 54. Group array of objects by property

### 🔹 VERY IMPORTANT (asked in interviews)

```javascript id="f1k3jz"
let users = [
  { name: "A", age: 20 },
  { name: "B", age: 20 },
  { name: "C", age: 25 },
];

let grouped = users.reduce((acc, curr) => {
  let key = curr.age;

  if (!acc[key]) acc[key] = [];
  acc[key].push(curr);

  return acc;
}, {});

console.log(grouped);
```

---

# ✅ 55. Sort array of objects

```javascript id="k8m2qv"
let users = [
  { name: "A", age: 25 },
  { name: "B", age: 20 },
];

// Ascending
users.sort((a, b) => a.age - b.age);

// Descending
users.sort((a, b) => b.age - a.age);
```

---

# ✅ 56. Select element by id

### 🔹 Logic:

Use DOM selector to access element

```javascript id="g1f2h3"
let element = document.getElementById("myId");
console.log(element);
```

---

# ✅ 57. Change text content dynamically

```javascript id="a2b3c4"
let el = document.getElementById("text");
el.textContent = "Updated Text";
```

### 🔹 Alternative

```javascript id="d5e6f7"
el.innerText = "Hello";
el.innerHTML = "<b>Hello</b>";
```

---

# ✅ 58. Add event listener to button

```javascript id="h7j8k9"
let btn = document.getElementById("btn");

btn.addEventListener("click", function () {
  alert("Button clicked!");
});
```

---

# ✅ 59. Create dynamic list items

```javascript id="l1m2n3"
let ul = document.getElementById("list");

let items = ["Apple", "Banana", "Mango"];

items.forEach((item) => {
  let li = document.createElement("li");
  li.textContent = item;
  ul.appendChild(li);
});
```

---

# ✅ 60. Remove element from DOM

```javascript id="o4p5q6"
let el = document.getElementById("removeMe");
el.remove();
```

---

# ✅ 61. Create modal popup

### 🔹 HTML

```html id="r7s8t9"
<button onclick="openModal()">Open</button>

<div id="modal" style="display:none;">
  <p>Modal Content</p>
  <button onclick="closeModal()">Close</button>
</div>
```

### 🔹 JS

```javascript id="u1v2w3"
function openModal() {
  document.getElementById("modal").style.display = "block";
}

function closeModal() {
  document.getElementById("modal").style.display = "none";
}
```

---

# ✅ 62. Toggle dark mode

```javascript id="x4y5z6"
function toggleDarkMode() {
  document.body.classList.toggle("dark");
}
```

### 🔹 CSS idea

```css id="c1c2c3"
.dark {
  background: black;
  color: white;
}
```

---

# ✅ 63. Create counter app

```javascript id="d4d5d6"
let count = 0;

function increment() {
  count++;
  document.getElementById("count").textContent = count;
}

function decrement() {
  count--;
  document.getElementById("count").textContent = count;
}
```

---

# ✅ 64. Form validation using JS

```javascript id="e7e8e9"
function validateForm() {
  let name = document.getElementById("name").value;

  if (name.trim() === "") {
    alert("Name is required");
    return false;
  }

  return true;
}
```

---

# ✅ 65. Create image slider

### 🔹 Logic:

Change image index on button click

```javascript id="f1f2f3"
let images = ["img1.jpg", "img2.jpg", "img3.jpg"];
let index = 0;

function next() {
  index = (index + 1) % images.length;
  document.getElementById("slider").src = images[index];
}

function prev() {
  index = (index - 1 + images.length) % images.length;
  document.getElementById("slider").src = images[index];
}
```

---

# ✅ 66. Create Promise example

### 🔹 Logic:

Promise has **resolve / reject**

```javascript id="p1a2b3"
let promise = new Promise((resolve, reject) => {
  let success = true;

  if (success) resolve("Success");
  else reject("Error");
});

promise.then((res) => console.log(res)).catch((err) => console.log(err));
```

---

# ✅ 67. Convert callback to Promise

### 🔹 Callback version

```javascript id="c1c2c3"
function getData(callback) {
  setTimeout(() => {
    callback("Data received");
  }, 1000);
}
```

### 🔹 Promise version

```javascript id="c4c5c6"
function getData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Data received");
    }, 1000);
  });
}
```

---

# ✅ 68. Use async/await with fetch

```javascript id="f7f8f9"
async function fetchData() {
  try {
    let res = await fetch("https://jsonplaceholder.typicode.com/posts");
    let data = await res.json();
    console.log(data);
  } catch (err) {
    console.log(err);
  }
}
```

---

# ✅ 69. Handle API errors

```javascript id="e1e2e3"
async function fetchData() {
  try {
    let res = await fetch("https://api.example.com/data");

    if (!res.ok) {
      throw new Error("API Error");
    }

    let data = await res.json();
    console.log(data);
  } catch (err) {
    console.error("Error:", err.message);
  }
}
```

---

# ✅ 70. Create delay function

```javascript id="d1d2d3"
function delay(ms) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}

// Usage
async function run() {
  console.log("Start");
  await delay(2000);
  console.log("After 2 seconds");
}
```

---

# ✅ 71. Implement retry logic

```javascript id="r1r2r3"
async function retry(fn, retries = 3) {
  try {
    return await fn();
  } catch (err) {
    if (retries === 0) throw err;
    return retry(fn, retries - 1);
  }
}
```

---

# ✅ 72. Promise.all

### 🔹 Logic:

Run multiple promises in parallel

```javascript id="a1a2a3"
Promise.all([fetch("/api1"), fetch("/api2"), fetch("/api3")])
  .then((res) => console.log(res))
  .catch((err) => console.log(err));
```

---

# ✅ 73. Promise.race

### 🔹 Logic:

Returns fastest promise

```javascript id="b1b2b3"
Promise.race([fetch("/fast"), fetch("/slow")]).then((res) => console.log(res));
```

---

# ✅ 74. Simulate API call

```javascript id="s1s2s3"
function fakeAPI() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("API response");
    }, 1000);
  });
}
```

---

# ✅ 75. Timeout wrapper

### 🔹 Logic:

Fail if request takes too long

```javascript id="t1t2t3"
function withTimeout(promise, ms) {
  let timeout = new Promise((_, reject) => {
    setTimeout(() => reject("Timeout"), ms);
  });

  return Promise.race([promise, timeout]);
}

// Usage
withTimeout(fetch("/api"), 2000)
  .then((res) => console.log(res))
  .catch((err) => console.log(err));
```

---

# ✅ 76. Closure in loop

```javascript
for (var i = 1; i <= 3; i++) {
  setTimeout(() => console.log(i), 1000);
}
```

### 👉 Output:

```
4 4 4
```

### 🔹 Why?

- `var` is **function-scoped**
- Loop ends → `i = 4`
- All callbacks share same `i`

### ✅ Fix (important!)

```javascript
for (let i = 1; i <= 3; i++) {
  setTimeout(() => console.log(i), 1000);
}
```

👉 Output: `1 2 3`

---

# ✅ 77. var vs let in loop

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 0);
}
```

👉 Output:

```
3 3 3
```

```javascript
for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 0);
}
```

👉 Output:

```
0 1 2
```

### 🔹 Explanation:

- `var` → shared variable
- `let` → new binding per iteration

---

# ✅ 78. setTimeout inside loop

```javascript
for (let i = 1; i <= 3; i++) {
  setTimeout(() => console.log(i), i * 1000);
}
```

👉 Output:

```
1 (after 1s)
2 (after 2s)
3 (after 3s)
```

---

# ✅ 79. 0.1 + 0.2

```javascript
console.log(0.1 + 0.2);
```

👉 Output:

```
0.30000000000000004
```

### 🔹 Why?

- JS uses **floating point (IEEE 754)**
- Precision error

### ✅ Fix

```javascript
Number(0.1 + 0.2).toFixed(1); // "0.3"
```

---

# ✅ 80. [] + {}

```javascript
console.log([] + {});
```

👉 Output:

```
"[object Object]"
```

### 🔹 Why?

- `[]` → "" (empty string)
- `{}` → object → string conversion

---

# ✅ 81. typeof null

```javascript
console.log(typeof null);
```

👉 Output:

```
"object"
```

### 🔹 Why?

- **JS bug (legacy issue)**

---

# ✅ 82. NaN === NaN

```javascript
console.log(NaN === NaN);
```

👉 Output:

```
false
```

### ✅ Correct way

```javascript
Number.isNaN(NaN); // true
```

---

# ✅ 83. this in arrow function

```javascript
let obj = {
  name: "Ashish",
  greet: () => {
    console.log(this.name);
  },
};

obj.greet();
```

👉 Output:

```
undefined
```

### 🔹 Why?

- Arrow function **does not have its own `this`**
- Takes `this` from **outer scope**

---

# ✅ 84. Promise chaining output

```javascript
Promise.resolve(1)
  .then((x) => x + 1)
  .then((x) => {
    throw new Error("Error");
  })
  .then((x) => console.log(x))
  .catch((err) => console.log("Caught"));
```

👉 Output:

```
Caught
```

### 🔹 Explanation:

- Error jumps directly to `.catch()`

---

# ✅ 85. Event loop execution order

```javascript
console.log("Start");

setTimeout(() => console.log("Timeout"), 0);

Promise.resolve().then(() => console.log("Promise"));

console.log("End");
```

👉 Output:

```
Start
End
Promise
Timeout
```

---

# 🔥 SUPER IMPORTANT (INTERVIEW GOLD)

### Event Loop Priority:

1. **Synchronous code**
2. **Microtasks (Promise)**
3. **Macrotasks (setTimeout)**

---

# ✅ 86. To-Do App

### 🔹 Logic:

- Add task
- Display list
- Delete task

```html
<input id="task" placeholder="Enter task" />
<button onclick="addTask()">Add</button>
<ul id="list"></ul>

<script>
  function addTask() {
    let input = document.getElementById("task");
    let li = document.createElement("li");

    li.textContent = input.value;

    li.onclick = () => li.remove(); // delete on click

    document.getElementById("list").appendChild(li);
    input.value = "";
  }
</script>
```

---

# ✅ 87. Counter App

```html
<h2 id="count">0</h2>
<button onclick="inc()">+</button>
<button onclick="dec()">-</button>

<script>
  let count = 0;

  function inc() {
    document.getElementById("count").textContent = ++count;
  }

  function dec() {
    document.getElementById("count").textContent = --count;
  }
</script>
```

---

# ✅ 88. Stopwatch

### 🔹 Logic:

- Start / Stop / Reset
- Use `setInterval`

```javascript
let time = 0;
let interval;

function start() {
  interval = setInterval(() => {
    time++;
    console.log(time);
  }, 1000);
}

function stop() {
  clearInterval(interval);
}

function reset() {
  time = 0;
}
```

---

# ✅ 89. Digital Clock

```javascript
function clock() {
  let now = new Date();
  let time = now.toLocaleTimeString();
  document.getElementById("clock").textContent = time;
}

setInterval(clock, 1000);
```

---

# ✅ 90. Calculator

```javascript
function calc(op) {
  let a = Number(document.getElementById("a").value);
  let b = Number(document.getElementById("b").value);

  let result;

  if (op === "+") result = a + b;
  if (op === "-") result = a - b;
  if (op === "*") result = a * b;
  if (op === "/") result = a / b;

  console.log(result);
}
```

---

# ✅ 91. Search Filter

```javascript
function filterList() {
  let input = document.getElementById("search").value.toLowerCase();
  let items = document.querySelectorAll("li");

  items.forEach((item) => {
    item.style.display = item.textContent.toLowerCase().includes(input)
      ? ""
      : "none";
  });
}
```

---

# ✅ 92. Pagination

### 🔹 Logic:

- Show limited items per page

```javascript
let data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let perPage = 3;
let page = 1;

function showPage() {
  let start = (page - 1) * perPage;
  let end = start + perPage;

  console.log(data.slice(start, end));
}
```

---

# ✅ 93. Infinite Scroll

```javascript
window.addEventListener("scroll", () => {
  if (window.innerHeight + window.scrollY >= document.body.offsetHeight) {
    console.log("Load more data...");
  }
});
```

---

# ✅ 94. Drag and Drop

```html
<div id="drag" draggable="true">Drag me</div>
<div id="drop">Drop here</div>

<script>
  let drag = document.getElementById("drag");
  let drop = document.getElementById("drop");

  drag.addEventListener("dragstart", (e) => {
    e.dataTransfer.setData("text", "Dragged!");
  });

  drop.addEventListener("dragover", (e) => e.preventDefault());

  drop.addEventListener("drop", (e) => {
    e.preventDefault();
    drop.textContent = e.dataTransfer.getData("text");
  });
</script>
```

---

# ✅ 95. Debounced Search

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

const search = debounce((e) => {
  console.log("API call:", e.target.value);
}, 500);

document.getElementById("search").addEventListener("input", search);
```

---

# ✅ 96. LRU Cache

### 🔹 Logic:

- Store recent items
- Remove least recently used

```javascript
class LRUCache {
  constructor(limit) {
    this.limit = limit;
    this.cache = new Map();
  }

  get(key) {
    if (!this.cache.has(key)) return -1;

    let val = this.cache.get(key);
    this.cache.delete(key);
    this.cache.set(key, val);

    return val;
  }

  put(key, value) {
    if (this.cache.has(key)) {
      this.cache.delete(key);
    }

    this.cache.set(key, value);

    if (this.cache.size > this.limit) {
      let firstKey = this.cache.keys().next().value;
      this.cache.delete(firstKey);
    }
  }
}
```

---

# ✅ 97. Polyfill for bind()

```javascript
Function.prototype.myBind = function (context, ...args) {
  let fn = this;

  return function (...newArgs) {
    return fn.apply(context, [...args, ...newArgs]);
  };
};
```

---

# ✅ 98. EventEmitter

### 🔹 Logic:

- on → subscribe
- emit → trigger

```javascript
class EventEmitter {
  constructor() {
    this.events = {};
  }

  on(event, listener) {
    if (!this.events[event]) this.events[event] = [];
    this.events[event].push(listener);
  }

  emit(event, data) {
    if (this.events[event]) {
      this.events[event].forEach((fn) => fn(data));
    }
  }
}
```

---

# ✅ 99. Promise from scratch

### 🔹 Basic version (interview level)

```javascript
class MyPromise {
  constructor(executor) {
    this.callbacks = [];

    const resolve = (value) => {
      this.callbacks.forEach((cb) => cb(value));
    };

    executor(resolve);
  }

  then(cb) {
    this.callbacks.push(cb);
    return this;
  }
}
```

---

# ✅ 100. setTimeout from scratch (conceptual)

### 🔹 Logic:

JS doesn't have real setTimeout → browser handles it

```javascript
function mySetTimeout(fn, delay) {
  let start = Date.now();

  function loop() {
    if (Date.now() - start >= delay) {
      fn();
    } else {
      requestAnimationFrame(loop);
    }
  }

  loop();
}
```

---

# ✅ 101. Flatten object

```javascript
function flatten(obj, parent = "", res = {}) {
  for (let key in obj) {
    let newKey = parent ? `${parent}.${key}` : key;

    if (typeof obj[key] === "object" && obj[key] !== null) {
      flatten(obj[key], newKey, res);
    } else {
      res[newKey] = obj[key];
    }
  }

  return res;
}
```

---

# ✅ 102. Deep freeze object

```javascript
function deepFreeze(obj) {
  Object.freeze(obj);

  for (let key in obj) {
    if (typeof obj[key] === "object" && obj[key] !== null) {
      deepFreeze(obj[key]);
    }
  }

  return obj;
}
```

---

# ✅ 103. Observer Pattern

```javascript
class Subject {
  constructor() {
    this.observers = [];
  }

  subscribe(fn) {
    this.observers.push(fn);
  }

  notify(data) {
    this.observers.forEach((fn) => fn(data));
  }
}
```

---

# ✅ 104. Simple Router

```javascript
class Router {
  constructor() {
    this.routes = {};
  }

  add(path, cb) {
    this.routes[path] = cb;
  }

  navigate(path) {
    if (this.routes[path]) {
      this.routes[path]();
    }
  }
}
```

---

# ✅ 105. Rate Limiter

### 🔹 Logic:

Limit number of calls per time

```javascript
function rateLimiter(fn, limit, interval) {
  let calls = 0;

  setInterval(() => {
    calls = 0;
  }, interval);

  return function (...args) {
    if (calls < limit) {
      calls++;
      fn.apply(this, args);
    } else {
      console.log("Rate limit exceeded");
    }
  };
}
```

---

# ✅ 106. Reverse Linked List (JS)

### 🔹 Logic:

Reverse pointers one by one

```javascript
function reverseList(head) {
  let prev = null;
  let curr = head;

  while (curr) {
    let next = curr.next;
    curr.next = prev;
    prev = curr;
    curr = next;
  }

  return prev;
}
```

---

# ✅ 107. Implement Stack

### 🔹 LIFO (Last In First Out)

```javascript
class Stack {
  constructor() {
    this.items = [];
  }

  push(val) {
    this.items.push(val);
  }

  pop() {
    return this.items.pop();
  }

  peek() {
    return this.items[this.items.length - 1];
  }
}
```

---

# ✅ 108. Implement Queue

### 🔹 FIFO (First In First Out)

```javascript
class Queue {
  constructor() {
    this.items = [];
  }

  enqueue(val) {
    this.items.push(val);
  }

  dequeue() {
    return this.items.shift();
  }
}
```

---

# ✅ 109. Balanced Parentheses

### 🔹 Logic:

Use stack

```javascript
function isValid(str) {
  let stack = [];
  let map = { ")": "(", "}": "{", "]": "[" };

  for (let char of str) {
    if (["(", "{", "["].includes(char)) {
      stack.push(char);
    } else {
      if (stack.pop() !== map[char]) return false;
    }
  }

  return stack.length === 0;
}
```

---

# ✅ 110. Two Sum

### 🔹 Logic:

Use hashmap

```javascript
function twoSum(arr, target) {
  let map = {};

  for (let i = 0; i < arr.length; i++) {
    let diff = target - arr[i];

    if (map[diff] !== undefined) {
      return [map[diff], i];
    }

    map[arr[i]] = i;
  }
}
```

---

# ✅ 111. Binary Search

### 🔹 Requires sorted array

```javascript
function binarySearch(arr, target) {
  let left = 0,
    right = arr.length - 1;

  while (left <= right) {
    let mid = Math.floor((left + right) / 2);

    if (arr[mid] === target) return mid;
    else if (arr[mid] < target) left = mid + 1;
    else right = mid - 1;
  }

  return -1;
}
```

---

# ✅ 112. Merge Intervals

```javascript
function merge(intervals) {
  intervals.sort((a, b) => a[0] - b[0]);

  let res = [intervals[0]];

  for (let i = 1; i < intervals.length; i++) {
    let last = res[res.length - 1];

    if (intervals[i][0] <= last[1]) {
      last[1] = Math.max(last[1], intervals[i][1]);
    } else {
      res.push(intervals[i]);
    }
  }

  return res;
}
```

---

# ✅ 113. Longest Substring Without Repeating

### 🔹 Sliding Window

```javascript
function longestSub(str) {
  let set = new Set();
  let left = 0,
    max = 0;

  for (let right = 0; right < str.length; right++) {
    while (set.has(str[right])) {
      set.delete(str[left]);
      left++;
    }

    set.add(str[right]);
    max = Math.max(max, right - left + 1);
  }

  return max;
}
```

---

# ✅ 114. Majority Element

👉 Appears > n/2 times

```javascript
function majority(arr) {
  let count = 0,
    candidate = null;

  for (let num of arr) {
    if (count === 0) candidate = num;
    count += num === candidate ? 1 : -1;
  }

  return candidate;
}
```

---

# ✅ 115. First Non-Repeating Character

```javascript
function firstUnique(str) {
  let map = {};

  for (let char of str) {
    map[char] = (map[char] || 0) + 1;
  }

  for (let char of str) {
    if (map[char] === 1) return char;
  }

  return null;
}
```

---

# ✅ 116. Optimize large list rendering

### 🔹 What to say:

👉 “I’ll use virtualization (render only visible items)”

### 🔹 Simple approach

```javascript
function renderList(data, start, end) {
  let visible = data.slice(start, end);
  console.log(visible);
}
```

### 🔥 Real answer:

- Use **virtual scrolling**
- In React → `react-window`

---

# ✅ 117. Dark mode toggle

```javascript
function toggleTheme() {
  document.body.classList.toggle("dark");
}
```

### 🔥 Better:

```javascript
localStorage.setItem("theme", "dark");
```

---

# ✅ 118. Role-based UI access

### 🔹 Logic:

Show UI based on role

```javascript
function canAccess(role) {
  const roles = {
    admin: ["create", "edit", "delete"],
    user: ["view"],
  };

  return roles[role] || [];
}
```

---

# ✅ 119. Dynamic form builder

### 🔹 Logic:

Generate fields from config

```javascript
let fields = [
  { type: "text", label: "Name" },
  { type: "email", label: "Email" },
];

fields.forEach((f) => {
  let input = document.createElement("input");
  input.type = f.type;
  input.placeholder = f.label;
  document.body.appendChild(input);
});
```

---

# ✅ 120. Search with debounce

```javascript
function debounce(fn, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
```

---

# ✅ 121. Caching API

### 🔹 Logic:

Store response → avoid repeat calls

```javascript
let cache = {};

async function fetchData(url) {
  if (cache[url]) return cache[url];

  let res = await fetch(url);
  let data = await res.json();

  cache[url] = data;
  return data;
}
```

---

# ✅ 122. Chat UI logic

### 🔹 Logic:

- Append messages
- Scroll to bottom

```javascript
function addMessage(msg) {
  let div = document.createElement("div");
  div.textContent = msg;

  let chat = document.getElementById("chat");
  chat.appendChild(div);

  chat.scrollTop = chat.scrollHeight;
}
```

---

# ✅ 123. Undo-Redo functionality

### 🔹 Logic:

Use stack

```javascript
let history = [];
let redoStack = [];

function doAction(state) {
  history.push(state);
}

function undo() {
  let last = history.pop();
  redoStack.push(last);
}

function redo() {
  let last = redoStack.pop();
  history.push(last);
}
```

---

# ✅ 124. Handle offline mode

### 🔹 Logic:

Detect network

```javascript
window.addEventListener("offline", () => {
  console.log("Offline mode");
});

window.addEventListener("online", () => {
  console.log("Back online");
});
```

---

# ✅ 125. Theme switcher

```javascript
function setTheme(theme) {
  document.body.className = theme;
  localStorage.setItem("theme", theme);
}
```

---
