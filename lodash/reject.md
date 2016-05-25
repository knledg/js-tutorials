# _.reject

## Problem 1

You have an array of objects, and you want to get a subset of those objects back based on exclusion.

```javascript

const users = [
  { firstName: 'Jason', favoriteFood: 'Burger' },
  { firstName: 'Bob', favoriteFood: 'Fries' },
  { firstName: 'Tom', favoriteFood: 'Burger' },
  { firstName: 'Lily', favoriteFood: 'Carrots' },
];

const vegans = _.reject(users, { favoriteFood: 'Burger' });
console.log('Users who are vegans: ', vegans);

```

[Fiddle](https://jsfiddle.net/9ptxu030/)

(You can also specify a callback function just like with `_.filter` or `_.find` is you need to reject based on
more than just a string match)
