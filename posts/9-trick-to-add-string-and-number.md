# Trick to Adding String and Number

The unary + operator is a shortcut to convert a string into a number 🤩

Problem: Adding strings that contain numbers does NOT add them. Instead, the strings are concatenated ❌

Solution: Convert the string into a number. Then you can calculate the sum ✅


```javascript
const string = "100";
const number = 5;

// This doesn't return the sum, it's concatentated
console.log(string + number) // 1005

// Prepend string with "+" to calculate the sum
console.log(+string + number) // 105
```

## Like this Post

**[Like this on Twitter]https://twitter.com/samantha_ming/status/980157046698909696)**

**[Like this on Instagram](https://www.instagram.com/p/Bg_54HGAT-f/?taken-by=samanthaming)**


## Resources

- https://medium.com/@nikjohn/cast-to-number-in-javascript-using-the-unary-operator-f4ca67c792ce


## Image Download

![Download](9-trick-to-add-string-and-number.png)
