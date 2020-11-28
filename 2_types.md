
# Types

Categories of values.

## Number
[**docs**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

All JS numbers are floats!

Declaration
```js
const one = 1; // simple primitive declaration
// console.log(typeof one)

const twoHalf = 2.5; // with float

const two = Number(2); // const two = 2;

const three = Number('3');

const weirdNumber = Number('aaaa'); // Number(undefined); // Number(null) << returns NaN
```

Remember
- Asserting number type : `typeof x === 'number'`
- `NaN` is a number

Look up
- [Overflows](https://en.wikipedia.org/wiki/Integer_overflow), and representing large numbers using [BigInts (new)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt)


## Boolean
[**docs**]()

Either `true` or `false`.

Things that are falsy:
- `false`
- empty string: `''` or `""` but NOT `new String('')`.
- numbers `0`, `-0`, `0n` and `NaN`
- `undefined` and `null`

Things that are truthy:
- `true`
- everything else not falsy 😎

Declaration
```js
// from primitives
const funJs = true; // const funJs = false;

// from evaluaton of a chain of boolean operations
const greatJs = true || false;

// from object constructor with any known type 
const justBool = Boolean(0); // Boolean('string'); ...
```

Remember
- Equality checks using `===` or `==` evaluate to booleans.
- Always use `===`. Avoid surprises!
- Make use of known truthy vs falsy categorization. More on this later



## String
[**docs**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#String_primitives_and_String_objects)

Declaration
```js
const hello = 'Hello'; // using single quotes
// console.log(typeof hello)

const world = "World"; // using double quote

const helloWorld = `Hello World`; // using template literals

const helloJs = String("Hello JS") // using object constructor
```

Remember
- Asserting string type : `typeof x === 'string'`
- String objects from `new String()` are treated different from string primitives.

Look up
- Operations on strings: length checks, concatenation, casing, getting substrings, iterating over characters...
- [Regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)


## Object
[**docs**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

Representing collections in `key`, `value` pairs. Equivalent to **Dictionaries** in python.

Declaration
```js
    let firstObj = {
        firstProp: 1234,
        secondProp: undefined
    };
    // console.log(typeof firstObj)

    let booleanObj = Object(true); // equal to `new Boolean(true)`

    let stringObj = Object('') // equal to new String("")

    let compObject = new Object({
        obj: firstObj,
        bool: booleanObj,
        str: stringObj
    })

    // reading values of object properties
    let value = obj.secondProp;
    let value = obj['secondProp'];

    // reassigning values of object properties
    obj.firstProp = 1234;
    obj['firstProp'] = 1234;
```

Remember
- Except for primitives, all other things in JS are objects!
- Dot vs bracket notation for setting and getting values of object properties.
- Property values can be anything, including other objects!

Look up
- Static and instance methods on objects. Examples
  - Access all keys using `Object.keys()`
  - Access all values using `Object.values()`
  - Access both keys and values using `Object.entries()`

- deleting object properties
- copying, deep copying objects
- Specialized objects
  - [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
  - [Maps](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
  - [WeakMaps](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)
  - [Sets](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)
  - [WeakSets](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet)

## undefined

```js
let empty; // unassigned variables have value of undefined by default
```

## null
[**docs**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null)

```js
let empty = null; // variable value is intentionally left absent
```

## Supplementary Topics, Stuff. 🐣

**Symbols**

[Frst class uniqueness](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol). If anything, this signifies a continued evolution of JS

**For LoLs**

[Evidence of absence](https://en.wikipedia.org/wiki/Evidence_of_absence). How you represent 'complete emptiness', or 'nothing'
