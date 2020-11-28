# Functions
[**docs**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

Predefined, canned and reusable logic.

```js

// Print Hello World to the console
console.log('Hello World');

/**
 * Print Hello World to the console,
 * usng Python like print()
 */
function print() {
  console.log('Hello World');
}

/**
 * Print one thing to the console,
 * usng Python like print()
 */
function print(foo) {
  console.log(foo);
}

/**
 * Print anything to the console,
 * usng Python like print()
 */
function print(...args) {
  console.log(args);
}
```

## Highlights

**Fat arrow** or simply **arrow** syntax for declaring functions

```js
/**
 * Print Hello World to the console,
 * usng Python like print()
 */
const print = () => {
  console.log('Hello World');
}
```

**Default values for arguments**

```js
/**
 * Print Hello World to the console,
 * usng Python like print()
 */
function print(greeting = 'Hello World') {
  console.log(greeting);
}
```


**Asynchronous Programming.** Promises, Async/Await

Fire and forget long running actions and logic chains

```js
/**
 * It takes very long (10 seconds) to fetch this data,
 * Example, this could be a network call
 */
function getDataFromServerOrDatabase() {
    const someGeoJson = setTimeut(() => { return [] }, 10000);

    return new Promise(someGeoJson)
}

```

Promise pattern
```js
// Load data and do something when it's available
getDataFromServerOrDatabase().then(data => {
    // Success. Do something with data
    console.log(...data);
}).catch(error => {
    // Failure: Do something with error
    console.error(error);
})
```

Async-await pattern
```js
// Load data and do something when it's available
async function loadData() {
    try {
        const data = await getDataFromServerOrDatabase();

        // Success. Do something with data
        console.log(...data);
    } catch (error) {
        // Do something with error
        console.error(error);
    }
}
```

Remember

- Traditional `function` and `arrow` syntax for declaring functions
- Functions can `return` some results of their operation. By default, all functions return `undefined`
- order of arguments, default arguments, optional arguments


Look up

- Asynchronous programming in JS
- Execution context in JS
- What is [this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
- Closures
- Currying / Chaining
- Generators
- Higher order functions. Callbacks!
- (Immediately Invoked Function Expressions) IIFEs
- Recursion!
