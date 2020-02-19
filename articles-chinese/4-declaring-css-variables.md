Translated by [@baooab](https://github.com/baooab)

# 声明 CSS 变量

别用 Sass 了，因为我们有 CSS 变量了！

当然我还是喜欢 Sass 的。但原生 CSS 已经支持这个特性了。✅ 不需要预处理器 & 不再需要编译！

```css
:root { /* 1a. 全局作用域 */
  --color: blue;
}

.fun { /* 1b. 局部作用域 */
  --color: red;
  /* ☝️ 这个变量仅在 .fun 的作用域内有效 */
  color: var(--color); /* red */
}

/* 2. 使用 CSS 变量 */
div {
  color: var(--color); /* blue */
}
```

## 资源

- https://medium.freecodecamp.org/everything-you-need-to-know-about-css-variables-c74d922ea855
