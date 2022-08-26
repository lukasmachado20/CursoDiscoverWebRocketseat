# Shorthand

* junção de propriedades deixando mais resumido e legível.

```css
{
    /* background properties */
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;

    /* background shorthand */
    background: #000 url(images/br.gif) no-repeat left top;
}
```

## Detalhes

* não irá considerar anteriores, ou seja, irá sobrescrever anteriores.
* valores não especificados irão assumir o valor padrão.
* a ordem, geralmente, não importa, mas se houver muitar propriedades com valores semelhantes, poderemos encontrar problemas.

**https://developer.mozilla.org/pt-BR/docs/Web/CSS/Shorthand_properties**