# _.reduce

## Problem 1

Sometimes you want to add a bunch of numbers together. You could create a function that adds all the numbers and returns the result, or you could use `_.reduce`


```javascript

const users = [{
  firstName: 'Jay',
  savings: 500,
}, {
  firstName: 'Lily',
  savings: 1000,
}, {
  firstName: 'Bob',
  savings: 200,
}, {
  firstName: 'Tommen',
  savings: 0,
}];

const startingValue = 0;

const totalSavings = _.reduce(users, (memo, user) => {
  // during each iteration, memo is what was returned from the last iteration. It starts at startingValue of 0
  // then becomes 500
  // then becomes 1500
  // then becomes 1700
  // then stays 1700
  console.log('What is the memo?', memo);
  return memo + user.savings;
}, startingValue);

console.log('Total savings: ', totalSavings);

```

[Fiddle](https://jsfiddle.net/1acf6jxq/1/)


## Problem 2

`_.reduce` isn't just for adding numbers, you can also check if the user has permission to login:


```javascript

const user = {
  firstName: 'Jay',
  roles: {
    admin : {
      canAnswerCalls: true,
    },
    support : {
      canAnswerCalls: true,
    },
    sales : {
      canAnswerCalls: false,
    },
    chef : {
      canAnswerCalls: false,
    },
    hr : {
      canAnswerCalls: false,
    },
  },
}

const defaultAnswerCallsPermission = false;

const canJayAnswerCalls = _.reduce(user.roles, (memo, role) => {
  return memo || role.canAnswerCalls; // if any of them are true, canJayAnswerCalls will be true
}, defaultAnswerCallsPermission);

console.log('Can Jay answer calls?', canJayAnswerCalls);

```

[Fiddle](https://jsfiddle.net/574Ltfqb/1/)
