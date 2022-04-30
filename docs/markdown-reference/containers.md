# Containers

É bastante útil realçar conteúdo como exemplos, dicas, definições de conceitos,
avisos ou até esconder conteúdo extenso e menos relevante, como grandes exemplos
e demonstrações.

## Sintaxe

Para criar um _container_, basta usar a delimitação `:::` seguido do tipo do mesmo.

```md
:::tip

Some content

:::
```

É possível colocar qualquer tipo de conteúdo dentro do container, mesmo [outros containers](#nesting).

### Nesting

Para colocar um _container_ dentro de outro, basta alterar a delimitação do _container_ exterior
para `::::` (e assim sucessivamente).

```md
::::tip

Some content

:::details
More content
:::

::::
```

!!! warning "Evitar"

    Colocar um _container_ dentro de outro já é, muitas vezes, desnecessário e confuso.
    Deve-se evitar colocar mais ainda.

### Título

Por omissão, cada tipo de _container_ tem o seu tipo como título.
É, no entanto, possível alterar este título para algo com mais significado dependendo
da situação.

```md
:::info[Exemplo]

Some content

:::
```

## Tipos de Containers

Existem os seguintes tipos de _containers_:

- `info` (azul): Deve ser usado para exemplos principais e curtos ou para informação não essencial.
- `tip` (verde): Deve ser usado para dar dicas, para definições de conceitos ou conteúdos a reter.
- `warning` (amarelo): Deve ser usado para avisar erros comuns
- `danger` (vermelho): Deve ser usado para avisar erros comuns (mas mais graves)
- `details`: É colapsável, pelo que é ideal para exemplos longos ou demonstrações.
