Translated by [@Mathias54](https://github.com/Mathias54)

# Customizando o CSS selecion

Customizar o Estilo do selecion do CSS é divertido!  🎉

O ::selecion CSS pseudo-elemento permite você aplicar estilos no texto quando ele está em destaque. É uma ótima forma de adicionar mais cores no seu site. 💃

```css
p::selection {
  background: DeepPink;
  color: white;
}
```

Para o Firefox, você precisa utilizar o ::-moz-selection 👍

```css
p::-moz-selection {
  background: DeepPink;
  color: white;
}
```

## Referências

- https://css-tricks.com/almanac/selectors/s/selection/
