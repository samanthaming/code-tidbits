# Prevent Error with Default `{}` when Destructuring

When you use destructuring, make sure to set a default value of empty `{}` to prevent it from throwing an error!

```javascript
function hi (person) {
  const {age} = person
}
hi() // ❌ Ahh, TypeError


function hi (person = {}) {
  const {age} = person
}

hi() // ✅ Yay, no errors
```

### The story behind this tidbit

So this happened to me the other day. Took me forever to debug my code. Then I realized I made a function call and the data that was being passed was undefined. So whenever you write a function that you will be performing destructuring. ALWAYS. I mean always make sure you set a empty `{}` to prevent your app from crashing! 🤦🏻‍♀️

## Why does it thrown an Error?

This is because you can’t destructure `undefined` and `null` values

```javascript
const { age } = null;
age; // TypeError

const { name } = undefined;
name; // TypeError
```

When you call a function and you forget to pass an argument. The value is by default `undefined`.

```javascript
function hi (person) {
  return typeof person;
}

hi(); // undefined
```

## Other values that won't thrown an Error

Here's a list of other values that you can destructure that won't throw an error.

```javascript
const { emptyString } = '';
const { nan } = NaN;
const {emptyObject } = {};

emptyString; // undefined
nan; // undefined
emptyObject; // undefined
```

## Community Input

_[CJ J.](https://www.linkedin.com/in/~cj-johnson):_ A similar issue is what lead to the optional chaining proposal

https://github.com/tc39/proposal-optional-chaining

_[CJ J.](https://www.linkedin.com/in/~cj-johnson):_ This is similar to an internal function at Facebook used both in Hack and Javascript called idx.

_[CJ J.](https://www.linkedin.com/in/~cj-johnson):_ You pass in a callback and it calls your callback inside a try-catch so that the error doesn't propagate and it just gives you a sentinel value instead.

```javascript
const obj = {};
const val = idx(obj, _ => _.x.y);
```

<br>

_[CJ J.](https://www.linkedin.com/in/~cj-johnson):_ But for correctness, you can't just catch all exceptions. You have to check for TypeError and then make sure it's a TypeError around reading a property of undefined or null. That way your callback can safely throw exceptions of its own types and not have them be accidentally caught by the idx function.

## Resources

- [Getting to Grips with ES6: Destructuring](https://hackernoon.com/getting-to-grips-with-es6-destructuring-e5b5ddb34990)

- [Destructuring Default Values](http://exploringjs.com/es6/ch_destructuring.html#sec_default-values-destructuring)

- [David Walsh Blog: Destructuring and Function Arguments](https://davidwalsh.name/destructuring-function-arguments)
