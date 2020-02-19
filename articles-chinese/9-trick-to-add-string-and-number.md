Translated by [@baooab](https://github.com/baooab)

# 字符串与数字相加时的一个技巧

一元 + 操作符可以作为字符串转数字的一种快捷方式 🤩

问题：字符串与数字相加，得到的不是两数之和。而是字符串连接在一起的结果 ❌

解决：将字符串转为数字。然后再计算两数之和 ✅

```javascript
const string = "100";
const number = 5;

// 这里得到不是和，而是字符串连接起来的结果
console.log(string + number) // 1005

// 在 string 前面跟一个 "+" 结果就是两数之和了
console.log(+string + number) // 105
```

## 资源

- https://medium.com/@nikjohn/cast-to-number-in-javascript-using-the-unary-operator-f4ca67c792ce
