# _.values

## Problem 1

Sometimes we want to display just the values of an object and ignore everything else. Below we want to create a list of foods for a select dropdown based on any type of food that was mentioned.


```javascript

const user = {
  firstName: 'Jay',
  foodPreferences: {
    favorite: 'Burger',
    hates: 'Asparagus',
    lateNightSnack: 'Oreos',
  }
}

const foods = _.values(user.foodPreferences);

console.log('Food options: ', foods);

```

[Fiddle](https://jsfiddle.net/syhcfvp0/)
