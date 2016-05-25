# _.transform

## Problem 1

You have an object with strings and want to actually make them booleans (or vice versa)

```javascript

const payload = {
  isAdmin: 'Yes',
  isSupport: 'No',
}

const roles = _.transform(payload, (result, value, key) => {
  if (value === 'Yes') {
    return result[key] = true;
  }

  return result[key] = false;
});

console.log('User Roles', roles);

```

[Fiddle](https://jsfiddle.net/5otr9wen/)
