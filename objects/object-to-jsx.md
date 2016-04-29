# Map over an object and display the keys and values as JSX

We can use lodash to help with that!

```javascript
const person = { firstName : 'Bob', lastName : 'Smith' };
```

We have an object with the keys `firstName` and `lastName`. It is stored in a variable called `person`.

In React, we can display all the keys and the values using lodash's `_.map` function.

```javascript

const jsx = _.map(person, (value, key) => {
  return (
    <div key={key}>
      {key}: {value}
    </div>
  );
});
```

In the above example, any time you map over something and return it as JSX the top-level DOM element needs a key to tell React it is unique from the other DOM elements inside that loop.

Inside JSX, we can get access to our JS variables with `{}` (curly brackets). So in the example, when the person object gets looped over it will get:

1. value = 'Bob', key = 'firstName'
1. value = 'Smith', key = 'lastName'

And it will return two unique divs that are stored in the `jsx` variable

