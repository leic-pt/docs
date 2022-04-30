# CommonMark

O _parser_ de Markdown dos ResumosLEIC segue a especificação [CommonMark](https://commonmark.org/),
que contém as seguintes funcionalidades:

## Headers

```md
# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6
```

## Formatação básica

```md
Texto em **bold**, _itálico_ ou _**ambos**_.
```

Para fazer um parágrafo, deixa-se uma linha em branco entre texto:

```md
Parágrafo acima

Parágrafo abaixo
```

Para mudar de linha dentro do mesmo parágrafo, isto é, fazer um _line break_, deve-se deixar **dois espaços no fim da linha**.

## Links

```md
[Para links externos](https://example.com)
[Ou para uma página do site](/fis-1/kinematics-1d)
```

## Imagens

Todas as imagens devem ter _alt text_, isto é, uma pequena descrição da mesma para o caso
de não ser possível carregar a imagem (e.g. conexão fraca) ou para _screen readers_.

```md
![Descrição da imagem](./assets/XXXX-imagem.png)
```

Os Resumos LEIC incluem uma adição às imagens que permite [aplicar-lhes filtros](./image-filters.md),
como por exemplo _dark mode_.

## Blockquotes

Não usado muito frequentemente, mas pode ser útil para citações.

```md
> Blockquote
```

## Listas

É possível fazer listas ordenadas e não ordenadas, assim como combinações de ambas (ou do mesmo tipo):

```md
- Item
- Item
- Item

1. Item 1
2. Item 2
3. Item 3

- Item
  1. Item
  2. Item
- Item
```

## Linha Horizontal

Usada geralmente para separar conteúdo não relacionado.

```md
Conteúdo acima

---

Conteúdo abaixo
```

## Blocos de Código

É possível usar blocos de código _in-line_, isto é, em texto corrido, com um _backtick_ <code>&#96;</code>:

```md
Para os resumos, necessitas de `git`, `node` e `yarn`.
```

Também existem _codeblocks_ para trechos maiores, com _syntax highlighting_ (opcional):

    ```python
    print("Hello World!")
    ```
