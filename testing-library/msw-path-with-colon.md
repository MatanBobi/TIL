## Problem
MSW uses an "express like" route matching mechanism and in some scenarios, our URL's can contain `:` as part of the URL and not to be defined as a route param.

## Solution
We can escape the `:` character or any other character by putting double backslashes before the character (`\\`).

```
// Used to match '/api/v1/resource:action'
rest.get('/api/v1/resource\\:action', (req, res, ctx) => res(ctx.json({ ... })))
```
