# _.isEmpty

## Problem 1

We want to return early from a function if the object doesn't exist, but an empty object isn't falsy

```javascript

function saveNonEmptyObject(obj) {
  if (! obj) {
    console.log('Cannot save, object is empty');
    return false;
  }

  console.log('Saving obj to database'); // Unexpected behavior
}


const obj = {};
saveNonEmptyObject(obj);


```

[Fiddle](https://jsfiddle.net/z0dgxcux/1/)



So instead we can use `_.isEmpty` for our objects to

```javascript

function saveNonEmptyObject(obj) {
  if (_.isEmpty(obj)) {
    console.log('Cannot save, object is empty');
    return false; // behaves as expected
  }

  console.log('Saving obj to database');
}


const obj = {};
saveNonEmptyObject(obj);
```

[Fiddle](https://jsfiddle.net/ukLut14f/1/)
