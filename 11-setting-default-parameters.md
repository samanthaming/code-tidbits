# Setting Default Parameters

Super simple to set Default Parameters with ES6 👏‬

The old way was to use a ternary operator to assign the default value if it was undefined.

With ES6, you can set the default value right inside the function parameters 🎉


```javascript
// Old Way
function coffeeOrTea(drink) {
  drink = drink !== undefined ? drink : '🍵';
}

// ES6 Way
function coffeeOrTea2(drink = '🍵') {

}
```

## Like this Post

**[Twitter](https://twitter.com/samantha_ming/status/985230884969185281)**

**[Instagram](https://www.instagram.com/p/Bhj9ITfhlNT/?taken-by=samanthaming)**


## Resources

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters


## Image Download

![Download](11-setting-default-parameters.png)
