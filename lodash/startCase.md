# _.startCase

## Problem 1

Sometimes you get string data back from the server that isn't formatted well, but you still want to display the data to the user. You can use `_.startCase` to clean it up.

```javascript

const username = 'jason tetri';
const address = '365 e chestnut rd. phoenix, arizona 85010';

console.log(_.startCase(username));
console.log(_.startCase(address));


```

[Fiddle](https://jsfiddle.net/L7vp4L6a/)
