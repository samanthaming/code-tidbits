Translated by [@baooab](https://github.com/baooab)

# 自定义 CSS 选择样式

自定义 CSS 选择样式很有趣！🎉

使用 CSS 的 ::selection 伪元素选择器，定义文本被选择时的样式。这不失为一个为站点增添点颜色的好办法 💃

```css
p::selection {
  background: DeepPink;
  color: white;
}
```

Firefox 浏览器的话，需要使用 ::-moz-selection 👍

```css
p::-moz-selection {
  background: DeepPink;
  color: white;
}
```

## 资源

- https://css-tricks.com/almanac/selectors/s/selection/
