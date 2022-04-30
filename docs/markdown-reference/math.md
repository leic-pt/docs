# Fórmulas Matemáticas

Para UCs como Cálculo, Álgebra e até ASA, é necessário utilizar expressões matemáticas nos resumos.
Para isso, é possível utilizar [KaTeX](https://katex.org/docs/supported.html) (um _subset_ de LaTeX)
nos ficheiros Markdown.

## Sintaxe

### Inline

Fórmulas matemáticas no meio do texto são delimitadas por um dólar (`$`).

```md
Seja $f$ uma função $f: \R \to \R$ tal que ...
```

!!! tip

    Caso se pretenda utilizar o símbolo dólar dentro do KaTeX ou em texto normal
    sem criar uma fórmula matemática, pode-se fazer _escape_: `\$`.

### Block

Um bloco de KaTeX é delimitado por dois dólares (`$$`) uma linha acima e abaixo da expressão.

```md
$$
x^2
$$
```

## Cores

É possível usar as [mesmas cores que se usa em texto](./text-color.md) nos blocos de KaTeX, através
da função `\smartcolor`.

```md
$$
x^{\smartcolor{orange}{2}}
$$
```

## Atalhos

Foram criados alguns atalhos para facilitar expressões escritas frequentemente.  
A lista completa pode ser encontrada na configuração do plugin `gatsby-remark-katex`
no ficheiro [`gatsby-config.js`](https://github.com/leic-pt/resumos-leic/blob/master/gatsby-config.js).

Os mais importantes são os seguintes:

| Atalho   | Expansão                       | Descrição                              |
| -------- | ------------------------------ | -------------------------------------- |
| `\d`     | `\mathop{}\!\mathrm d`         | Símbolo `d` para utilizar em derivadas |
| `\op{}`  | `\operatorname{#1}`            | _Alias_ para `\operatorname`           |
| `\car`   | `\operatorname{car}`           | Característica de uma matriz           |
| `\ondiv` | `\operatorname{div}`           | Divergência                            |
| `\rot`   | `\operatorname{rot}`           | Rotacional                             |
| `\lapt`  | `\mathcal{L}\left\{#1\right\}` | Transformação de Laplace               |
