# _.groupBy

## Problem 1

We have an array of objects and we want to group those objects together

```javascript

const users = [{
  firstName: 'Jay',
  role: 'Support',
}, {
  firstName: 'Lily',
  role: 'Admin',
}, {
  firstName: 'Bob',
  role: 'Admin',
}];

const usersGroupedByRole = _.groupBy(users, 'role');

console.log('Users Grouped By Role', usersGroupedByRole);

```

[Fiddle](https://jsfiddle.net/n6c4cf9a/)

