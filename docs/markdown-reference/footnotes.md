# Footnotes

Por vezes pode ser útil dar indicações ou informações adicionais que não se enquandram
no conteúdo da página.

Para isto, podemos usar footnotes, que irão ficar no fim da página.

## Sintaxe

```md
Então, $f'(a)h$ é uma transformação linear[^trans-lin] em $h$.

[^trans-lin]: Para relembrar transformações lineares, ...
```

!!! bug

    Existe atualmente um bug em que o texto que fica no link para a footnote
    é o _id_ da mesma (no exemplo acima, `trans-lin`) em vez de um número (e.g. `1`).
