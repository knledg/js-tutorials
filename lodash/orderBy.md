# _.orderBy

## Problem 1

You have an array of objects, and you want to order them alphabetically

```javascript

const users = [
  { firstName: 'Jason', favoriteFood: 'Burger' },
  { firstName: 'Bob', favoriteFood: 'Fries' },
  { firstName: 'Tom', favoriteFood: 'Burger' },
  { firstName: 'Lily', favoriteFood: 'Carrots' },
];

const orderedUsers = _.orderBy(users, 'firstName');

console.log('Ordered Users' orderedUsers);
```

[Fiddle](https://jsfiddle.net/w07yzz9z/1/)
