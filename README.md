# Manual de Sobrevivência Git/GitHub

Este e um trabalho de um manual de sobrevivência para Git e GitHub! O git é um sistema de controle de versão distribuida bastante utilizado no desenvolvimento de software, que a possibilidade do desenvolvendo rastrear as mudancas, permite a colaboracao entres os desenvolvedores de maneira eficiente e segura, mantendo a intregridade
do historico da versões do projeto.

## Índice

- [Manual de Sobrevivência Git/GitHub](#manual-de-sobrevivência-gitgithub)
  - [Índice](#índice)
  - [ 1. Múltiplos Branches](#-1-múltiplos-branches)
  - [ 2. Navegar Entre Branches](#-2-navegar-entre-branches)
  - [ 3. Manutenção Local e Produção Remota](#-3-manutenção-local-e-produção-remota)
    - [Configurando o Repositório Remoto](#configurando-o-repositório-remoto)
    - [Atualizando Seu Repositório Local](#atualizando-seu-repositório-local)
  - [ 4. Integração com VSCode, Eclipse e Android Studio](#-4-integração-com-vscode-eclipse-e-android-studio)
    - [VSCode](#vscode)
    - [Eclipse](#eclipse)
    - [Android Studio](#android-studio)
  - [ 5. Tag de Versão](#-5-tag-de-versão)
  - [ 6. Commits Intermediários na Versão de Desenvolvimento](#-6-commits-intermediários-na-versão-de-desenvolvimento)
  - [ 7. Branch Separada para Feature](#-7-branch-separada-para-feature)

---

## <a name="multiplos-branches"></a> 1. Múltiplos Branches

Branches são uma parte fundamental do Git que permitem que você trabalhe em diferentes funcionalidades, correções de bugs ou experimentos de forma isolada, como uma linha do tempo que pode sofrem alteracões e teste sem causar maiores danos a versao principal. Para criar um novo branch, utilize o comando:

```sh
git branch nome-do-branch
```

Para listar todos os branches:

```sh
git branch
```

## <a name="navegar-entre-branches"></a> 2. Navegar Entre Branches

Para alternar entre branches, use o comando:

```sh
git checkout nome-do-branch
```

Ou, se você estiver usando Git 2.23 ou posterior, pode usar o comando:

```sh
git switch nome-do-branch
```

## <a name="manutencao-local-e-producao-remota"></a> 3. Manutenção Local e Produção Remota

### Configurando o Repositório Remoto

Para adicionar um repositório remoto, use:

```sh
git remote add origin https://github.com/seu-usuario/seu-repositorio.git
```

Para enviar suas alterações para o repositório remoto:

```sh
git push origin master
```

### Atualizando Seu Repositório Local

Para atualizar seu repositório local com as últimas alterações do repositório remoto, use:

```sh
git pull origin master
```

## <a name="integracao-vscode-eclipse-android-studio"></a> 4. Integração com VSCode, Eclipse e Android Studio
O git tem facilidade para se intergrar com varias IDEs, que facilitam o desenvolvimento e também a experiencia no desenvolvimento.

### VSCode

Instale a extensão oficial do Git no VSCode para uma integração suave. Você pode clonar um repositório diretamente do VSCode:

1. Abra o VSCode.
2. Pressione `Ctrl+Shift+P` para abrir a paleta de comandos.
3. Digite `Git: Clone` e insira a URL do repositório.

### Eclipse

Para integrar Git no Eclipse:

1. Vá para `Help` > `Eclipse Marketplace`.
2. Procure por `EGit` e instale o plugin.
3. Após a instalação, vá para `File` > `Import` > `Git` > `Projects from Git`.

### Android Studio

Para configurar Git no Android Studio:

1. Vá para `File` > `Settings` > `Version Control` > `Git`.
2. Certifique-se de que o caminho para o executável Git está correto.
3. Para clonar um repositório, vá para `VCS` > `Get from Version Control`.

## <a name="tag-de-versao"></a> 5. Tag de Versão

Tags são usadas para marcar pontos específicos na história do seu repositório, uma pratica essencial para identificar as versões do codigo. As Tags de Versão sao utilizadas para criar pontos de referencia permanentes no historico de commits. Para criar uma tag:

```sh
git tag -a v1.0 -m "Versão 1.0"
```

Para empurrar tags para o repositório remoto:

```sh
git push origin --tags
```

## <a name="commits-intermediarios"></a> 6. Commits Intermediários na Versão de Desenvolvimento

É uma boa prática fazer commits frequentemente na branch de desenvolvimento. Estes commits intermediários ajudam a salvar o progresso e facilitam o rastreamento de mudanças. Para fazer um commit:

```sh
git add .
git commit -m "Descrição do commit"
```

## <a name="branch-separada-feature"></a> 7. Branch Separada para Feature

Para manter o desenvolvimento organizado, crie uma branch separada para cada nova funcionalidade:

```sh
git checkout -b feature/nome-da-feature
```

Após terminar a funcionalidade, faça o merge de volta para a branch principal (geralmente `master` ou `main`):

```sh
git checkout master
git merge feature/nome-da-feature
```
---
Este foi trabalho sobre os conhecimento de Git/Github!
