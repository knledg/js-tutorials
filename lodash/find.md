# _.find

## Problem 1

You have an array of objects, and you want to get back the FIRST object that matches your filters.

```javascript

const users = [
  { firstName: 'Jason', favoriteFood: 'Burger' },
  { firstName: 'Bob', favoriteFood: 'Fries' },
  { firstName: 'Tom', favoriteFood: 'Burger' },
  { firstName: 'Lily', favoriteFood: 'Carrots' },
];

const userWhoLikesBurgers = _.find(users, { favoriteFood: 'Burger' });
console.log('Users who like burgers: ', userWhoLikesBurgers);

const userWhoLikesCarrots = _.find(users, { favoriteFood: 'Carrots' });
console.log('Users who like carrots: ', userWhoLikesCarrots);

```

[Fiddle](https://jsfiddle.net/eqjpsdba/1/)


## Problem 2 - You need to filter but you need to filter on something more than a string match

Let's find the first user who has an income > 50

```javascript

const users = [
  { firstName: 'Jason', income: 10  },
  { firstName: 'Bob', income: 100 },
  { firstName: 'Tom', income: 75 },
  { firstName: 'Lily', income: 20 },
];

const userWithIncomeOver50 = _.find(users, user => {
  return user.income > 50;
});
console.log('Users with income over 50: ', userWithIncomeOver50);
```

[Fiddle](https://jsfiddle.net/mz9qfsyp/)

