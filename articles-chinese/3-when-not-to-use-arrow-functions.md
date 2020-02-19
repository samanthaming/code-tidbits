Translated by [@baooab](https://github.com/baooab)

# 什么时候别用箭头函数

箭头函数是极好的，但并不适用于所有情况。要避免在对象里使用箭头函数，因为箭头函数里的 'this' 总被限定在父级作用域——比如。下面的情况下，this 指向的是 'window' 而非 'burger'。

> 译者注：这里的所谓“限定在父级作用域”是指箭头函数没有自己的 this，它的 this 就是父级作用域里的 this。

```javascript
const burger = {
    type: '🍔',
    eat: () => { // 应该用 function()
        console.log(this) // 'this' 指向 window，而非 burger
    }
};

// 避免在对象里使用箭头函数
```

## 资源

- https://wesbos.com/arrow-function-no-no/
