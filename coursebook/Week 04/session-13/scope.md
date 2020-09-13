## Scope

**Scope in JavaScript**

JavaScript has a feature called scope. Understanding scope will make your code stand out, reduce errors and help you make powerful design patterns with it.

**What is Scope?**

Scope is the accessibility of variables, functions, and objects in some particular part of your code during runtime. In other words, scope determines the visibility of variables and other resources in areas of your code.

When you start writing JavaScript in a document, you are already in the global scope. There is only one global scope throughout a JavaScript document. A variable that is in the global scope is defined everywhere in the code.

**Example (1)**

```javascript
// the scope is by default global

var name = 'Ali';
```

- Variables inside the global scope can be accessed and altered in any other part of the code.

**Example (2)**

```javascript
var name = 'Ali';

console.log(name); // logs 'Ali'

function logName() {
  console.log(name); // logs 'Ali'

  // 'name' is accessible here and in everywhere else
}
```

---

## Differences between (`var`, `let`, `const`)

One of the features that came with ES6 is the addition of `let` and `const` which can be used for variable declaration. The question now is, what makes them different from `var` which has been in use?

**1. `var`**

Before the advent of ES6, `var` declarations ruled as a King. Let us get to understand `var` more.

- Scope of `var`:

  In the following example, `var` declaration is global, which means that it can be accessed everywhere in the code.

**Example (1)**

```javascript
// Here, greeter is globally scoped.

var greeter = 'hey hi';

console.log(greeter); // result: hey hi
```

- `var` variables can be re-declared:

**Example (2)**

```javascript
// Re-declare var

var greeter = 'hey hi';

var greeter = 'say Hello instead';

console.log(greeter); // result: say Hello instead
```

- `var` variables can be updated:

**Example (3)**

```javascript
// Update var

var greeter = 'hey hi';

greeter = 'say Hello instead';

console.log(greeter); // result: say Hello instead
```

- Hoisting of `var`:

  Hoisting is a JavaScript mechanism where variables declarations are moved to the top of their scope before code execution. What this means is that if we do:

**Example (4)**

```javascript
console.log(greeter); // result: undefined

var greeter = 'say hello';
```

...it is interpreted like

**Example (5)**

```javascript
var greeter;

console.log(greeter); // result: undefined

greeter = 'say hello';

console.log(greeter); // result: say hello
```

So `var` variables are hoisted to the top of their scope and initialized with a value of `undefined`.

**2. `let`**

`let` is preferred for variable declaration now. It's no surprise as it comes as an improvement to the `var` declarations.

**Example (1)**

```javascript
let greeting = 'say Hi';

let times = 4;

if (times > 3) {
  let hello = 'say Hello instead';

  console.log(hello); // result: say Hello instead
}
```

- `let` can be updated:

  Like `var`, `let` can be updated.

**Example (2)**

```javascript
let greeting = 'say Hi';

greeting = 'say Hello instead';

console.log(greeting); // result: say Hello instead
```

- `let` declarations are hoisted to the top:

  Unlike `var` which is initialized with a value of `undefined`, the let keyword is not initialized. So if you try to use a let variable before declaration, you'll get a Reference Error.

**Example (3)**

```javascript
console.log(greeting); // Uncaught ReferenceError: Cannot access 'greeting' before initialization.

let greeting = 'say Hello instead';
```

- `let` can't be re-declared:

**Example (4)**

```javascript
// This will return an error:

let greeting = 'say Hi';

let greeting = 'say Hello instead'; //error: Identifier 'greeting' has already been declared
```

**3. `const`**

Variables declared with `const` maintain constant values. `const` declarations share some similarities with `let` declarations.

- `const` cannot be updated or re-declared:

  This means that the value of a variable declared with `const` remains the same. It cannot be updated or re-declared. So if we declare a variable with `const`, we can neither do:

**Example (1)**

```javascript
const greeting = 'say Hi';

greeting = 'say Hello instead'; //error: Assignment to constant variable.
```

...nor

**Example (2)**

```javascript
const greeting = 'say Hi';

const greeting = 'say Hello instead'; //error: Identifier 'greeting' has already been declared
```

- Hoisting of `const`:

  Just like `let`, `const` declarations are hoisted to the top but are not initialized.

**Example (3)**

```javascript
console.log(greeting); // Uncaught ReferenceError: Cannot access 'greeting' before initialization.

const greeting = 'say Hello instead';
```
