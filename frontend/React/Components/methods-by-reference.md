
# TIL: Methods by reference


## `onClick={parentMethod}` 

`parentMethod` is a reference to a method, so it does not need `()`. We are directly using an existing function without creating anything new.

## `onClick={() => parentMethod()}` 

By doing this, we are saying, "For each click, create a new function that executes the `parentMethod` function." Essentially, it’s a function that wraps and calls another function.

👉 [watch here](https://youtu.be/GMnWXlJnbNo?si=l8cG0U_V4FTcWm1I&t=7271)
