# Clonar Repositório Git

Para contribuires, é necessário criares uma _fork_ do repositório.
Para isso, clica no botão "Fork" no canto superior direito que aparece [no repositório dos resumos-leic](https://github.com/leic-pt/resumos-leic).
Alternativamente, usa este [link direto](https://github.com/leic-pt/resumos-leic/fork).

Após criares a tua fork, poderás criar _pull requests_, isto é, sugestões de alterações de conteúdo, no repositório dos resumos.

A forma mais fácil e segura de te autenticares perante o GitHub é usando SSH.
Se ainda não tens uma chave SSH, segue o tutorial na [documentação do GitHub sobre criar e adicionar à tua conta uma chave SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh).  
Não precisas de te autenticar para fazer download (_pull_), mas é necessário para fazeres upload (_push_).

Agora que já tens uma chave SSH, podes fazer _clone_ da tua fork!

No terminal (ou no GitBash se estiveres no Windows), escreve o seguinte comando na pasta onde queres guardar o repositório (e.g. na pasta `Documents`). Podes encontrar o URL SSH o botão verde "Code" na interface do GitHub.

```bash
git clone git@github.com:<o-teu-username>/resumos-leic.git     # Por exemplo git@github.com:diogotcorreia/resumos-leic.git
```

Após fazeres clone, é importante adicionares outro _remote_, denominado _upstream_, isto é, o repositório original de onde fizeste fork.
Isto permitir-te-á manter a tua fork atualizada.

```bash
git remote add upstream https://github.com/leic-pt/resumos-leic.git
```

Se fizeres `git remote -v` irás ver a lista de todos os _remotes_ que tens associados:

```
origin		git@github.com:<o-teu-username>/resumos-leic.git (fetch)
origin		git@github.com:<o-teu-username>/resumos-leic.git (push)
upstream	https://github.com/leic-pt/resumos-leic.git (fetch)
upstream	https://github.com/leic-pt/resumos-leic.git (push)
```

Parabéns, já tens o repositório Git no teu computador!

Trata este repositório como se fosse exclusivamente teu - cria _branches_ para a adição de _features_ e faz `commit` sempre que achares pretinente.

Caso esta seja a primeira vez que estás a usar Git, é recomendado veres a [palestra do Missing Semester do MIT sobre Git](https://missing.csail.mit.edu/2020/version-control/). Sim, é 1h30, mas aprendes tudo o que precisas, e acredita, saberes Git ir-te-á ser útil para os projetos que vais fazer ao longo do curso!  
Para além disso, no fim da página encontra-se uma _Cheet Sheet_ com os comandos mais usados.
