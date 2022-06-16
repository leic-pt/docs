# Submeter alterações

Agora que já fizeste as alterações no teu computador, podes fazer uma `PR` - [Pull Request](https://www.pagerduty.com/resources/learn/what-is-a-pull-request/) - ou seja, passar pelo processo de submissão para o website oficial.  

Para isso, tens que proceder como se estivesses a trabalhar num repositório teu:

1. Fazer um (ou vários) `commit` das alterações (Ex. `git commit -m "[BD] - Added guide on .cgi"`);
2. Fazer `push` para o ***teu*** repositório com as alterações (Ex. `git push`);

Assim que tiveres feito `push` para o ***teu*** repositório, irá aparecer a opção de fazer uma `PR` no *GitHub*:

![GitHub PR](/static/PullRequest.png)  
<br>  

Irá então aparecer uma página que permite escrever um titulo e uma descrição da `PR`:  

![GitHub PR Description](/static/PullRequestMenu.png)  
*Nota*: É importante seguir o formato para o título descrito no comentário na descrição -  
"Para garantir consistência, todos os títulos de pull requests devem seguir o formato:
`[Sigla da UC] Breve descrição (com a primeira letra maiúscula e sem ponto final)`"
<br> 

Assim que o título e a descrição estiverem escritas, pasta clicar no botão `Create pull request` e o pedido será feito com sucesso!  

## Pull request vs Push request

Poderão existir dúvidas na nomenclatura usada - porquê `Pull request` e não `Push request`, visto que estamos a "empurrar" conteúdos para o repositório principal?

Esta dúvida é perguntada muitas vezes, por exemplo [aqui](https://stackoverflow.com/questions/21657430/why-is-a-git-pull-request-not-called-a-push-request).  

A ideia é que fazer `Push` de mudanças locais para um repositório efetivamente significa "enviar" as mudanças para o repositório - Nós "empurramos" novo conteúdo (A mesma lógica aplica-se para quando fazemos `Pull`).  

Contudo, quando se fala em `Pull request`, estamos a pedir (*request*) ao repositório de destino que faça `Pull` das nossas mudanças pois nós não somos *maintainers* do repositório e portanto não temos permissões para fazer `Push` - para sermos nós a "empurrar" as mudanças.
