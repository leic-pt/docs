# Filtros em Imagens

Surgiu a necessidade de aplicar filtros dinamicamente às imagens, por exemplo, de forma a que
estas tivessem _dark mode_ quando o _dark mode_ do site está ativo.

Deste modo, é possível adicionar um parâmetro ao link da imagem, de forma a aplicar
estes filtros.

## Dark Mode

Este filtro inverte as cores da imagem quando o _dark mode_ no site está ativo.
Basta adicionar `#dark=<mode>` ao fim do link da imagem para aplicar este filtro,
em que `<mode>` é um dos modos abaixo.  
Por exemplo:

```md
![Descrição da imagem](./link/to/image#dark=1)
```

Os filtros aplicados com a propriedade [`filter` de CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/filter) são, consoante o modo:

- `1`: `#!css invert(1) hue-rotate(180deg) saturate(5)`
- `2`: `#!css invert(1) hue-rotate(180deg) saturate(3)` (recomendado)
- `3`: `#!css invert(1) hue-rotate(180deg)`
- `4`: `#!css invert(1)`
