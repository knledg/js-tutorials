# _.assign

## Problem 1

In javascript, as you pass variables between functions you can accidentally modify the variable's contents. Take a look at the example below:

```javascript

function calculateHypotheticalRaise(user, raiseAmount) {
  user.income = user.income + raiseAmount;

  console.log(`The user\'s income would become ${user.income}`);
}


let user = {
  firstName: 'Jason',
  income: 1,
};

calculateHypotheticalRaise(user, 100);


console.log('Now what is the original income amount again?', user.income);

```

Oops! We overwrote the original value. That can be fixed with `_.assign`.

[Fiddle](https://jsfiddle.net/5ysxocv4/1/)


```javascript

function calculateHypotheticalRaise(user, raiseAmount) {
  let tmpUser = _.assign({}, user);
  tmpUser.income = tmpUser.income + raiseAmount;

  console.log(`The user\'s income would become ${tmpUser.income}`);
}


let user = {
  firstName: 'Jason',
  income: 1,
};

calculateHypotheticalRaise(user, 100);


console.log('Now what is the original income amount again?', user.income);

```

[Fiddle](https://jsfiddle.net/ndbcxyjg/1/)


## Problem 2

We are on a list view for users and we want to set some defaults for filters that get passed to the backend, but we also want users to be able to overwrite those defaults.

In the example below, a user search will have an offset of `0` and a limit of `25` by default but that can be overriden.

(Note you can also use `_.defaults`)

```javascript

function createFilters(userFilters = {}) {
  const filters = _.assign({}, {offset: 0, limit: 25}, userFilters);

  console.log('The filters are: ', filters);
}

// Just use the defaults
createFilters();

// Now change the limit to 50
createFilters({limit: 50});

```

[Fiddle](https://jsfiddle.net/4jug3dq9/1/)
