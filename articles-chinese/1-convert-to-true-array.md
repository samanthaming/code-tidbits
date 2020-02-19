Translated by [@baooab](https://github.com/baooab)

# 将类数组对象转换成数组

很酷！这是我从 [@wesbos](https://twitter.com/wesbos) 的 ES6 课程里新学到的  🔥

```javascript
const nodeList = document.querySelectorAll('ul li');

// 方法 1: 转换成数组
Array.from(nodeList);

// 方法 2: 转换成数组
[...nodeList];

// 现在可以使用 map 或其他方法做循环了
```

## 资源

- https://github.com/wesbos/es6-articles/blob/master/25%20-%20Array.from()%20and%20Array.of().md
