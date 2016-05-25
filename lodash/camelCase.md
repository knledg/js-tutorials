# _.camelCase

## Problem 1

Your codebase all uses camelCasing for your variable names but an external api uses snake_casing for their variables and you want to standardize their output.

```javascript

const apiOutput = { result_set: [], record_count: 10 };

let transformedOutput = {}
_.each(apiOutput, (value, key) => {
  transformedOutput[_.camelCase(key)] = value;
});

console.log(transformedOutput);


```

[Fiddle](https://jsfiddle.net/4ua5souy/1/)
