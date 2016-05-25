# _.cloneDeep

## Problem 1

In javascript, as you pass variables between functions you can accidentally modify the variable's contents. Take a look at the example below with an array:

```javascript

function showFormattedNames(users) {
  _.each(users, user => {
    user.firstName = _.capitalize(user.firstName);
  });

  console.log(users);
}


let users = [{
  firstName: 'jay',
}];

showFormattedNames(users);


console.log('Now what is the original list of users like again?', users);

```

Oops! We overwrote the original value. That can be fixed with `_.cloneDeep`.

[Fiddle](https://jsfiddle.net/oq7yxvbd/)


We can fix this with `_.cloneDeep`

```javascript
function showFormattedNames(users) {
  let tmpUsers = _.cloneDeep(users);

  _.each(tmpUsers, user => {
    user.firstName = _.capitalize(user.firstName);
  });

  console.log(tmpUsers);
}


let users = [{
  firstName: 'jay',
}];

showFormattedNames(users);


console.log('Now what is the original list of users like again?', users);

```

[Fiddle](https://jsfiddle.net/oq7yxvbd/2/)
