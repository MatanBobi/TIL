## Problem

Sometime when you use `screen.debug()` you'll get a very large DOM so the output in the terminal will get truncated.

## Solution
To extend the output's default length you can either use: `screen.debug(null, 20000)` or set an environment variable called `DEBUG_PRINT_LIMIT` with the number of characters you want to see.
