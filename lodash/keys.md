# _.keys

## Problem 1

Sometimes the keys for an object can be important and we need to use them. Here we want to show all the user's roles but don't care about their permissions.


```javascript

const user = {
  firstName: 'Jay',
  roles: {
    admin : {
      canEditOtherUsers: true,
    },
    support : {
      canAnswerCalls: true,
    },
  },
}

const roles = _.keys(user.roles);

console.log('Users roles: ', roles);

```

[Fiddle](https://jsfiddle.net/uug4joeo/)
