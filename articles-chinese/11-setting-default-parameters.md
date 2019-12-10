Translated by [@baooab](https://github.com/baooab)

# 设置参数默认值

使用 ES6 设置参数默认值非常简单 👏‬

传统方式是运用三目运算符（`?:`）对值做判断，如果是 `undefined` 的话，就使用默认值。

使用 ES6 可以直接为函数参数设置默认值 🎉

```javascript
// 传统方式
function coffeeOrTea(drink) {
  drink = drink !== undefined ? drink : '🍵';
}

// ES6 的写法
function coffeeOrTea2(drink = '🍵') {

}
```

## 资源

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters
