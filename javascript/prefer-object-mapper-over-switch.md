## Problem
When having a `switch` that maps every case to a speific object, the code may become hard to read and maintain.

## Solution
We can use an object mapper instead of a `switch` statement:

```js
switch(objectType){
  case OBJECT_TYPES.string:
    return 'a string return value';
  case OBJECT_TYPES.object:
    return {};
  case OBJECT_TYPES.array:
    return [];
}
```

But this can be done easily with:

```js
const objectTypesMapper = {
  [OBJECT_TYPES.string]: 'a string return value',
  [OBJECT_TYPES.object]: {},
  [OBJECT_TYPES.array]: []
}
```
