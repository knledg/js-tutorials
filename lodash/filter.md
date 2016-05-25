# _.filter

## Problem 1

You have an array of objects, and you want to get back ALL objects that match your filters.

```javascript

const users = [
  { firstName: 'Jason', favoriteFood: 'Burger' },
  { firstName: 'Bob', favoriteFood: 'Fries' },
  { firstName: 'Tom', favoriteFood: 'Burger' },
  { firstName: 'Lily', favoriteFood: 'Carrots' },
];

const usersWhoLikeBurgers = _.filter(users, { favoriteFood: 'Burger' });
console.log('Users who like burgers: ', usersWhoLikeBurgers);

const usersWhoLikeCarrots = _.filter(users, { favoriteFood: 'Carrots' });
console.log('Users who like carrots: ', usersWhoLikeCarrots);

```

[Fiddle](https://jsfiddle.net/5p0ejtpk/)


## Problem 2 - You need to filter but you need to filter on something more than a string match

Let's find all users who have an income > 50

```javascript

const users = [
  { firstName: 'Jason', income: 10  },
  { firstName: 'Bob', income: 100 },
  { firstName: 'Tom', income: 75 },
  { firstName: 'Lily', income: 20 },
];

const usersWithIncomeOver50 = _.filter(users, user => {
  return user.income > 50;
});
console.log('Users with income over 50: ', usersWithIncomeOver50);
```

[Fiddle](https://jsfiddle.net/p6o37swu/)

