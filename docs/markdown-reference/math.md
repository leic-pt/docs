# Fórmulas Matemáticas

Para UCs como Cálculo, Álgebra e até ASA, é necessário utilizar expressões matemáticas nos resumos.
Para isso, é possível utilizar [KaTeX](https://katex.org/docs/supported.html) (um _subset_ de LaTeX)
nos ficheiros Markdown.

## Inline

Fórmulas matemáticas no meio do texto são delimitadas por um dólar (`$`).

```md
Seja $f$ uma função $f: \R \to \R$ tal que ...
```

!!! tip

    Caso se pretenda utilizar o símbolo dólar dentro do KaTeX ou em texto normal
    sem criar uma fórmula matemática, pode-se fazer _escape_: `\$`.
