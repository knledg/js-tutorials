# _.get

## Problem 1

I have a deeply nested object and I want to easily see if a deeply nested key has a value of true

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

console.log('Can the user make sales calls?', user.roles.sales.canMakeCalls);

```

Because the key `sales` doesn't exist on the `roles` object inside the `user` object, the above code throws this error: `Uncaught TypeError: Cannot read property 'canMakeCalls' of undefined`.


[Fiddle](https://jsfiddle.net/5dvnjLfv/)

Normally to fix that, you would have to check that each key exists all the way down to `canMakeCalls`:

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

console.log('Can the user make sales calls?', user && user.roles && user.roles.sales && user.roles.sales.canMakeCalls);

```

[Fiddle](https://jsfiddle.net/7usbcoxc/)

But we can shorten that logic with `_.get`

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

console.log('Can the user make sales calls?', _.get(user, 'roles.sales.canMakeCalls'));

```

[Fiddle](https://jsfiddle.net/494Lxsef/)
