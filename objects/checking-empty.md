# Checking if an object is empty

We can use lodash to help with that!

```javascript
import _ from 'lodash';

const emptyObject = {};
const objectWithKeys = { firstName : 'Bob' };

if (_.isEmpty(emptyObject)) {
  console.log('This is empty!');
}

if (! _.isEmpty(objectWithKeys)) {
  console.log('This is not empty');
}
```