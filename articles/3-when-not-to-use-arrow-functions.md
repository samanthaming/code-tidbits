# When NOT to use Arrow Functions

Arrow functions are terrific, but not suitable for all situations. Avoid them in objects because 'this' is always scoped to the parent -- which is the 'window' in this case. 

```javascript
const burger = {
    type: '🍔',
    eat: () => { // should use function() instead
        console.log(this) // 'this' is window, not burger
    }
};

// Avoid Arrow Functions in Objects
```

## Resources

- https://wesbos.com/arrow-function-no-no/
