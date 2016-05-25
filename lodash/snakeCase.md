# _.snakeCase

## Problem 1

You are about to save data to the database and your data needs to be snake_cased because that's how your table's columns are set up.

```javascript

const user = { firstName: 'Jason', lastName: 'Walsh' };


let transformedUser = {}
_.each(user, (value, key) => {
  transformedUser[_.snakeCase(key)] = value;
});

console.log('Saving user to database: ', transformedUser);


```

[Fiddle](https://jsfiddle.net/scpnjpej/1/)
