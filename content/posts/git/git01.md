---
title: "Git e GitHub: #1 — Instalação e Configurações Iniciais"
date: 2021-06-07T14:18:31-03:00
draft: false
---

O Git é um sistema de controle de versão e organização de código fonte. Foi inicialmente desenvolvido por Linus Torvalds para para gerir as versões do código fonte do Linux.

> Objetivos:
> 1. Realizar a instalação do Git
> 2. Identificar o usuário que irá utilizar o Git
> 3. Criar um repositório

## 1. Instalação

![git](/posts/git/git.png)

**Linux**

Para usuários Linux a instalação do git pode ser feita via terminal através do comando:

```bash
$ sudo apt-get install git
```

**Mac**

Para usuários de Mac o download do pacote de instalação pode ser feito através do site oficial do git.

**Windows**

Em máquinas windows faça o download do instalador de acordo com o sistema operacional através da página oficial do git. Nesse instalador para sistemas windows já vem integrado o gitBash, um interpretador de código do git que roda em sistemas micrisoft. Vamos utilizar esse interpretador para executar os comandos do git.
Para esse guia foi utilizado o Windows 10 como sistema operacional.

Após a instalação o gitBash pode ser acessado através do botão direito do mouse.

![git02](/posts/git/git02.gif)



## 2. Configurações Iniciais

Vamos verificar se está tudo certo e se o git foi instalado corretamente. Utilize o seguinte comando no terminal do linux/mac ou no gitBash para computadores windows.

```bash
$ git --version
```



![gitversion](/posts/git/gitversion.png)



## 2.2. Identificando o Usuário

> *Essa identificação irá servir para que o git identifique qual usuário está fazendo as alterações nos arquivos. A medida que utilizarmos o git para criar registros de nossos projetos será gravado quem foi o usuário que o fez.*

Para identificar o usuário que irá utilizar o git iremos preencher as variáveis globais `user.name` e `user.email`.

```
$ git config --global user.name "Thiago Guimarães Tavares"
$ git config --global user.email "thiagogmta@gmail.com"
```

Para verificar a configuração utilize o comando:

```
$ git config --list
```

![Configuração das Variáveis de Usuário](/posts/git/variaveisdeusuario.png)



## 3. Um Repositório no Git (criar, verificar e excluir)

> *O ato de iniciar um repositório no Git consiste em informar que aquele diretório criado para armazenar o projeto deve ser monitorado.*

Para armazenar nossos arquivos do projeto (seja código fonte ou outro tipo de documento), normalmente criamos um diretório no computador e inserimos os arquivos ali dentro. O ato de iniciar um repositório no Git consiste em informar que aquele diretório criado deve ser monitorado.

### 3.1. Criar: Iniciando um Repositório

Você deve navegar até o diretório onde estão os arquivos do seu projeto e executar o comando logo a seguir:

```
$ git init
```

Como estamos utilizando o windows para este guia, basta navegar até a pasta do projeto, clicar com o botão direito do mouse, selecionar gitBash e executar o comando.

![Git init](/posts/git/gitinit.gif)



Esse guia por exemplo está sendo escrito em MarkDown e como exemplo foi iniciado um repositório no Git dentro do diretório que armazena o projeto.

Ao executar o comando `git init` é criado um diretório chamado: `.git` que é um diretório criado pelo git com as informações do repositório. Esse diretório mantem-se oculto no sistema de arquivos.

### 3.2. Verificar: Status do repositório

Podemos verificar a situação do nosso repositório através de um comando específico. Dentro do diretório do projeto (no gitBash) execute o comando:

```
$ git status
```

Para este ambiente de testes temos o seguinte retorno:

```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Git e GitHub.md
        Guia de estudo_ Front-end.md
        Registro de Estudo Front-end.md

nothing added to commit but untracked files present (use "git add" to track)
```

O retorno do comando informa que existem arquivos que não estão sendo monitorados `untracked files:` e que não foi feito nenhum`commit` no nosso projeto.

### 3.3. Excluir: Apagar um Repositório

Caso não seja mais necessário o acompanhamento desse projeto (ou de qualquer outro) podemos desfazer o repositório apagando seus arquivos com o comando:

```
$ rm -f .git
```

## Conclusão do capítulo

Caso tudo tenha ocorrido bem até aqui, temos o git instalado, as variáveis de ambiente configuradas e quem sabe um repositório iniciado. No próximo post iremos adicionar arquivos para que o git faça monitoramento e gravar em seu registro. Até lá!