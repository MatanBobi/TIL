## Problem
When working with objects, you sometimes need to remove a property and get only the rest of the properties in an object.

## Solution
Use spread to get the "rest" of the properties.

```js
const myObject = { isLoading: true, data: [], isError: false }
const { isLoading, ...restProperties } = myObject
console.log(restProprties) // ==> Logs { data: [], isError: false }
```
