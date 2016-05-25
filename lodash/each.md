# _.each

## Problem 1

I have an array or an object and I need to loop over each of the cells or keys respectively but I don't need to return any data.

### Example

I have an array of objects (users) and I want to see if any of them are named Tom.

```javascript

let tomExists = false;

const users = [
  { firstName: 'Jason' },
  { firstName: 'Bob' },
  { firstName: 'Tom' },
  { firstName: 'Lily' },
];

_.each(users, user => {
  if (user.firstName === 'Tom') {
    tomExists = true;
  }
});

console.log('Does Tom Exist?', tomExists);

```

[Fiddle](https://jsfiddle.net/tcqw3qfh/)


## Behavior

Nothing gets returned from `_.each`, if you want to return values, use `_.map`

[Fiddle](https://jsfiddle.net/mctu89xt/1/)
