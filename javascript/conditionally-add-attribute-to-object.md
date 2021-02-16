## Problem

When working with objects, you sometimes need to add an attribute conditionally.

## Solution
Usually we had to do something like this:

```js
let myObject = { isLoading: true }
if (shouldAddProp) {
  myNewObject = { ...myNewObject, newProp: true }
}
if (shouldAddAnotherProp) {
  myNewObject = { ...myNewObject, anotherProp: false }
}
```

But this can be done easily by:

```js
const myNewObject = {
  isLoading: false,
  ...(shouldAddProp && { newProp: true }),
  ...(shouldAddAnotherProp && { anotherProp: false })
}
```
