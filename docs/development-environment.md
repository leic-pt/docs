# Ambiente de Desenvolvimento

Para contribuires para os [Resumos LEIC](https://resumos.leic.pt), precisas de ter os seguintes programas instalados:

- `git`
- `node` ([NodeJS](https://nodejs.org) v18+)
- `yarn`
- Um editor de texto (por exemplo, [VSCode](https://code.visualstudio.com/))

Segue abaixo o tutorial para o teu sistema operativo.

## GNU/Linux

### Debian ou Ubuntu

Caso não esteja instalado, pode-se instalar o `git` com:

```bash
sudo apt install git
```

Os repositórios do Debian/Ubuntu têm uma versão desatualizada do `node`, pelo que se deve utilizar o `nvm` para a instalação.  
Para isso, corre-se [o script que se encontra na página de GitHub do `nvm`](https://github.com/nvm-sh/nvm#install--update-script).
Por exemplo:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

De seguida, instalar a última versão do NodeJS:

```bash
nvm install --lts
```

Finalmente, instalar o `yarn`:

```bash
npm i -g yarn
```

Para instalar o VSCode, pode-se usar o `snap` ou fazer download do ficheiro `.deb`.  
Instruções mais detalhadas estão na [documentação do VSCode](https://code.visualstudio.com/docs/setup/linux).

### ArchLinux/Manjaro

Instalar `git`, `nodejs` e `yarn`:

```bash
sudo pacman -S git nodejs yarn
```

Alternativamente, pode-se seguir os passos do Ubuntu para instalar o `node` através do `nvm`.

Finalmente, instalar o VSCodium **ou** o VSCode:

```bash
sudo pacman -S code                   # open source version of vscode
paru -S visual-studio-code-bin        # proprietary binary by microsoft (from AUR)
```

## Windows

### Com WSL

**Embora seja possível utilizar o Windows, recomenda-se o uso de Linux ou WSL.**  
Ao usar [WSL (Windows Subsystem for Linux)](https://docs.microsoft.com/en-us/windows/wsl/install),
deve-se seguir as instruções de Linux (Ubuntu) para a instalação do `git`, `node`, e `yarn`.

O [VSCode](https://code.visualstudio.com/) deve-se instalar no Windows, mas instalar a [extensão para o WSL](https://code.visualstudio.com/docs/remote/wsl-tutorial).

### Sem WSL

Fazer download e instalar o [Git Bash](https://git-scm.com/downloads) e o [NodeJS](https://nodejs.org/en/download/) (versão LTS).

Após a instalação do NodeJS, pode-se instalar o `yarn` através do terminal.  
Na PowerShell ou Command Prompt:

```
npm i -g yarn
```

## MacOS

Instalar Xcode (na App Store) ou instalar as command line tools do Xcode (mais leve e recomendado):

```bash
xcode-select --install
```

Instalar o package manager Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Instalar `node`:

```bash
brew install node
```

Em seguida, instalar o `yarn`:

```bash
npm i -g yarn
```

Por último, instalar o VSCodium **ou** o VSCode:

```bash
brew install visual-studio-code  # proprietary binary by microsoft
brew install vscodium            # open source version of vscode
```
