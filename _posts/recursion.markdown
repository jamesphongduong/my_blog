# Recursion definition

Recursion is a programming pattern that's effective when the task at hand can be broken down into repetitive or similar steps.

A function is a "recursive function" when the function _calls itself_. A recursive function requires a condition to stop calling itself (aka _base condition_), otherwise it will infinitely call itself.

# Syntax

```
function recurse() {
    recurse();
}
```

recurse();

This is a recursive function as it calls itself, however it will be stuck in an
