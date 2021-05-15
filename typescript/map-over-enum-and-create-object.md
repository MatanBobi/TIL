## Problem

I'd like to map over a typescript enum in order to create a new object which is built on all the enum's keys.

## Solution

Let's say we have an enum that looks like this:

```ts
enum ResponsesTypes {
  USERS = 'USERS',
  USER_DETAILS = 'USER_DETAILS',
  USER_CHATS = 'USER_CATHS'
}
```

And we want to create an object that will be built on the enum so that whenever the enum changes, the object's type will also change.  
Based on the example above, the object's type should look like this:
```
{
  USERS: string
  USER_DETAILS: string
  USER_CHATS: string
}
```

To solve this we can create a helper type:
```ts
type ResponsesTypesMapperObject<T> = {
  [K in ResponsesTypes]?: T
}
```

And then our object will be defined as:
```ts
 const DataMapper:ResponsesTypesMapperObject<string>;
```
