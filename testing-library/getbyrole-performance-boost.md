## Explanation
`getByRole` function is a time consuming function since it considers the accessibility, styles and [`accname`](https://www.w3.org/TR/accname-1.1/) spec.

## Solution
We can use `getByRole(role, { hidden: true })`, this will avoid expensive visibility checks **but will also include inaccessible elements**.
