## Problem

Sometimes, we want to style our `console.log` statements so they'll pop right away.

## Solution

In Chrome DevTools, we can do this by creating a styles object and passing it to our console log.

```js
const style = 'background-color: deeppink; color: black; border: 3px solid grey; font-size: 2em; padding: 1em'
console.log("%cHi twitter friends", style);
```

And the result:
![image](https://user-images.githubusercontent.com/12711091/155277347-0e28629f-7037-430b-a9a4-e80244c0657c.png)
