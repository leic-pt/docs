# Correr o site localmente

Agora que já tens o repositório Git no teu computador, podes ligar o site localmente e ver como ficam as alterações que fazes sem precisar de fazer _commit_ (se ainda não sabes o que isso é, não te preocupes, iremos lá chegar).

Abre o terminal (ou PowerShell/Command Prompt no Windows) e executa os seguintes commandos na pasta `resumos-leic`.

!!! info

    Podes usar os [comandos `cd` e `ls` para navegares o teu sistema pelo terminal](https://www.digitalocean.com/community/tutorials/how-to-use-cd-pwd-and-ls-to-explore-the-file-system-on-a-linux-server).

!!! tip

    Se estiveres no Windows, podes clicar com o botão direito, **enquanto pressionas <kbd>SHIFT</kbd>**, no file explorer para abrir o _context menu_ com mais opções, incluindo a de abrir a PowerShell na pasta atual.

```
yarn         # Instala as dependências necessárias (equivalente a 'yarn install')
yarn dev     # Liga o servidor na porta 8000
```

Por vezes, pode haver atualizações às dependências.
É boa prática executares ambos estes comandos quando quiseres ligar o servidor.
O `yarn` é inteligente o suficiente para não fazer nada se já tiveres todas as dependências atualizadas!

Após executares o comando `yarn dev`, irá aparecer no terminal que podes ir ao endereço [http://localhost:8000](http://localhost:8080) para veres o site.

Para desligar o site, faz <kbd>CTRL</kbd>+<kbd>C</kbd> (sim, no terminal este shortcut não é para copiar).
