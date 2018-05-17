# When NOT to use Arrow Functions

Arrow functions are terrific, but not suitable for all situations. Avoid them in objects because 'this' is always scoped to the parent -- which is the 'window' in this case. 

```javascript

  type: '🍔',
  eat: () => { // Should use function() instead
    console.log(this); // 'this' is Window, not burger
  }
}

// Avoid Arrow Functions in Objects
```

## Resources

- https://wesbos.com/arrow-function-no-no/


## Image Download

[Download](https://github.com/samanthaming/code-tidbits/blob/master/images/3-when-not-to-use-arrow-functions.png)
