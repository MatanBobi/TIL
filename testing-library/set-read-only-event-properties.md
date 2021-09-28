## Problem
Sometimes when using `fireEvent` setting initial properties for the event, the event won't be intialized.  
This can happen because some properties like `currentTarget`, `timeStamp`, `cancelable` and more are defined as read-only.

## Solution
To set values for these kind of properties, you need to use `Object.defineProperty` after creating the custom event using `createEvent`.  
Here's an example:

```
const myEvent = createEvent.submit(form);
Object.defineProperty(myEvent, "currentTarget", { value: form });
fireEvent(form, myEvent);
```
