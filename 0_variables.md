
# Variables

Labels of places (in memory). Places where you store things

**keyword + descriptiveName** makes a variable.

**keyword + descriptiveName = value** assigns value to a variable.

`const`, `let` and the old `var` keywords

Declaration
```js
// using `const`
const favoriteLanguage = 'Python';

favoriteLanguage = 'JavaScript'; // reassignment is illegal ✖


// using `let`
let favoriteLanguage = 'Python';
favoriteLanguage = 'JavaScript'; // reassignment is allowed ✔


// using `var`
var favoriteLanguage = 'Python';

favoriteLanguage = 'JavaScript'; // reassignment was always allowed ✔
```

Remember

- use `const` for values you will never change again
- use `let` for values you will want to change (reassign)
- don't use `var`. Just forget about it😛

Look up

- scopes of variables
- variable shadowing
