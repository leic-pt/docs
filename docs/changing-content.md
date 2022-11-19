# Efetuar Alterações

## Estrutura do Site

Antes de se começar a efetuar alterações ao conteúdo, é importante perceber como está estruturado o site.

```
$ tree
.
├── content
│   ├── ...
│   ├── fis-i
│   │   ├── 0001-kinematics-1d.md
│   │   ├── 0002-kinematics-2d.md
│   │   ├── assets
│   │   │   ├── 0001-path.png
│   │   │   ├── ...
│   │   │   └── 0002-projectile-launch-velocity-vector-decomposition.svg
│   │   ├── cheatsheets
│   │   │   └── 0001-main-cheatsheet.md
│   │   ├── exercicios
│   │   │   └── 0999-fichas-2021-2022.md
│   │   ├── guides
│   │   │   ├── 0001-recap-highschool.md
│   │   │   └── assets
│   │   │       ├── 0001-force-decomposition.svg
│   │   │       ├── 0001-inclined-plane.svg
│   │   │       └── 0001-movement-graphs.svg
│   │   └── index.md
│   └── ...
├── plugins
│   └── ...
├── src
│   └── ...
├── README.md
└── ...
```

A pasta `content` tem todo o conteúdo do site e é onde nos vamos focar, visto que tudo o resto é relacionado com o site em si.  
Dento da pasta `content` existem várias pastas, uma para cada UC do curso.
De forma a facilitar a gestão de conteúdos, cada UC tem um _maintainer_ associado, que será quem irá aceitar/rejeitar as alterações propostas.

Dentro da pasta de cada UC, encontram-se ficheiros do tipo `XXXX-nome-da-pagina.md`,
uma pasta `assets`, um ficheiro `index.md` e possivelmente outras pastas.

- `index.md`: Página principal da UC, onde normalmente se encontra uma pequena descrição sobre a mesma,
  assim como alguns recursos úteis ou outras informações importantes.
- `XXXX-nome-da-pagina.md`: Uma página com conteúdo. `XXXX` refere-se ao identificador incremental da
  página de forma a manter a ordem na _sidebar_.
- `assets`: Pasta onde se guarda ficheiros auxiliares, como imagens. Geralmente, usa-se o
  formato `XXXX-pequena-descricao.png` onde `XXXX` é o identificador da página onde são usados.

## Criar um Novo Branch

Antes de começares a efetuar alterações, **deves criar um _branch_**.
Isto também se pode fazer no final, mas depois corre-se o risco de nos esquecermos.  
Quando fores [submeter alterações](./submitting-changes.md), vais fazê-lo ao submeter
o teu _branch_. Podes pensar num _branch_ como um conjunto de alterações face ao atual.

!!! info "O que é um _branch_?"

    No contexto de desenvolvimento de software, um _branch_ deve ser criado quando se
    pretende adicionar uma nova _feature_, corrigir um _bug_ existente, etc.
    Aqui temos algo semelhante, mas para alterações.

É boa prática agrupar alterações relacionadas num só _branch_, sendo que um _branch_ pode ter
vários _commits_.

Por exemplo, se quisermos fazer resumos de **CDI-I** e **BD** e corrigir erros
ortográficos de uma página de **SO**, devemos criar os seguintes _branches_,
através do comando `git branch <branch name>`.

- `git branch cdi1/add-content-sucessoes`;
- `git branch bd/add-content-dmbs`;
- `git branch so/fix-typos`.

Para mudar de _branch_, deves fazer `git checkout <branch name>`, sendo que o nome
do _default branch_ é `master`.

!!! note

    Os nomes dos branches são arbitrários, pelo que podes lhes dar o nome que quiseres.
    Os nomes acima servem apenas de exemplo.

!!! failure "Alterações para o `master`"

    **Nunca** faças alterações diretamente para o `master`! Dado que estás a trabalhar
    com uma _fork_, o teu _branch_ `master` deverá estar sempre sincronizado com o
    _branch_ `master` do repositório principal (frequentemente apelidado de _upstream_).

## Editar Páginas Existentes

Para editar um página já existente, basta abrir o respetivo ficheiro e editar o seu conteúdo.

Os ficheiros são escritos em [Markdown](https://en.wikipedia.org/wiki/Markdown), pelo que é muito
simples usar formatação adicional, como bold, itálico, headers, links, imagens, etc.

Os Resumos LEIC usam algumas extensões de Markdown para certo tipo de formatação, como a inserção de fórmulas
matemáticas ([KaTeX](https://katex.org/)), cores no texto, _containers_ (_info_, _tip_, _warning_, _error_ e _details_), etc.

É recomendado ver a [Referência Markdown](./markdown-reference/common-mark.md) para uma lista completa.

## Criar uma Nova Página

Como já foi referido, as páginas devem ter um nome do tipo `XXXX-nome-da-pagina.md`.
O nome do ficheiro não deve conter acentos.

Todas as páginas começam com _frontmatter_, isto é, _metadata_ que define o título, descrição, link, etc. da página.

```yaml
---
title: Cinemática 1D
description: >-
  Cinemática a 1 dimensão.
  Deslocamento.
  Velocidade Média e Velocidade Instantânea.
  Aceleração Média e Aceleração Instantânea.
path: /fis-i/kinematics-1d
type: content
---
```

- `title`: Título da página que irá aparecer na _tab_ do browser assim como na _sidebar_ do site.
  O título que aparece na página em si é independente e tem de ser definido em Markdown com um _heading_ de nível 1.
- `description`: Descrição da página. Aparece apenas quando o link é partilhado em redes sociais e/ou plataformas como Discord.
  Deve conter títulos de tudo o que é abordado na página.
- `path`: Link da página. Deverá ser `/uc/nome-da-pagina`. Não deve conter acentos.
- `type`: Tipo da página, que afeta o seu posicionamento na `sidebar`.

Os seguinte tipos de páginas estão disponíveis:

- `topLevelPage`: Página principal de cada UC
- `content` (_default_)
- `exercises`
- `cheatsheets`
- `guides`
- `tools`
- `labsProg`: Laboratórios de Programação
- `misc`

## Finalizar Alterações

Após efetuares as tuas alterações, deves correr o formatter para garantir que o estilo de código
está de acordo com as normas do projeto.

```
yarn format
```

Se tiveres um editor como o VSCode, podes instalar a extensão do Prettier para executares a formatação
sempre que guardas um ficheiro.
