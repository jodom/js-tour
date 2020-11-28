# Control Structures
[**docs**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling)

Selecting code paths and staying in control for every path!

**The Block**
Code within a pair of curly braces are in one logical unit:
The block. Execution is sequential, top down [*](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous)

```js
{
    // do thing one
    // do thing two
    ...
    // do thing n
}
```

## Conditional Branching

checking conditions

**if**

```js
if (condition) {
    // execute this block
}
```

**if** chaining

```js
if (condition1) {
    // execute block one
}

if (condition2) {
    // execute block two
}
```

**if** chaining with **else if** and **else**

```js
if (condition1) {
    // execute block one
} else if (condition2) {
    // execute block two
} else {
    // execute this other block for all other conditions
}
```

Note

-  A `condition` takes the form `left part === right part` or `left part == right part`.

**switch**

When (if) **if** chains have become unmanageable

```js
switch (value) {
    case match1:
        // execute this logic
        break;
    case match2:
        // execute this other logic
        break;
    default:
        // execute this in all other cases
        break;
}
```

Note

- `condition1`, `conditionX` ... `match1`, `matchX` shown here evaluate to **truthy** or **falsy**. So we can use any of the falsies and truthies without using comparator `===`.

- Remember to `break` on switches

```js
if (undefined) {
    // huh block, never executes
} else {
    // this block gets executed
}
```


## Loops and Iterations
Executes a block `n` times, until a condition fails.

**for** loops

Syntax: `for (start; stop; steps){ /* executable block */ }`

```js
  for (let i = 0; i <= 5; i++) { // notice use of `let`
    console.log(i);
  }
```

**for-of** and **for-in** loops

```js
  for (let i of [0, 1, 2, 3, 4, 5]) {
    console.log(i);
  }

  for (let i in [0, 1, 2, 3, 4, 5]) {
    console.log(i);
  }
```

**while** loops

```js
  let i = 0;
  while (i <= 5) {
    console.log(i);
    i++; // this is very important, I think :)
  }
```

## Exceptional events, Handling and Graceful Recovery

**throw** 🤷🏾‍♀️

Javascript code raises exceptions via a `throw` statement. "Something has gone terribly wrong, we are giving up at this point"🤷🏾‍♂️

```js
    throw "we failed!!!"; // we failed!!! exception

    throw true; // true exception

    // But we should throw proper JS error objects

    throw new Error('We failed!!!');

    // So failure is a great thing, when we are expecting them :)
    if(failCondition) {
        throw new Error('We failed!!!');
    }
```

**handling exceptions**

Whenever we **try** stuff, we should also expect and be ready to **catch** failures.

```js
try {
    // this block gets executed
    // but it has an error in logic that raises an exception
    throw new Error('Stop the count!!!');
} catch {
    // Okay, we saw that coming,
    // Plan E gets executed
}
```

Remember

- All switch cases need a break
- Wrap everything in try catch

Look up
- nested control flows.
- inspecting exceptions with `catch(e) { /* inspect e */}`
- Promise `rejections` and how to handle them
- `finally`
- early returns / early exits
- exhaustive switch statements
- **do-while** control flow
