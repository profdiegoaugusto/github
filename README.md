# Git/Github

Created: February 25, 2022 8:13 AM
Tags: desenvolvimento, git, github, jogos, lab, mobile, web

![git_banner_2.png](git_banner_2.png)

**Git** é um *Sistema de Controle de Versão* distribuído gratuito e de código aberto projetado para lidar com tudo, desde projetos pequenos a muito grandes com velocidade e eficiência. Na Engenharia de Software, Controle de Versão é um componente do Gerenciamento de Configurações, também conhecido como: controle de revisão, controle de origem ou gerenciamento de código-fonte. 

Gerenciamento de versões, envolve manter o acompanhamento de várias versões de componentes do sistema e assegurar que as mudanças nos componentes, realizadas por diferentes desenvolvedores, não interfiram umas nas outras.  O **GitHub** é uma plataforma de hospedagem de código para controle de versão e colaboração. Ele permite que você e outras pessoas trabalhem juntos em projetos à partir de qualquer lugar.

# Sumário

# Se prepare para a aula

Vamos reservar alguns minutos para configurar o seu ambiente de trabalho local.

## Passo 1: Crie a sua conta no GitHub

1. Acesse [GitHub.com](http://github.com/) e clique em **Sign up**;
2. Escolha a conta gratuita;
3. Você receberá um e-mail de verificação no endereço fornecido;
4. Clique no link para concluir o processo de verificação.

<aside>
💡 O GitHub foi projetado para ser executado nas versões atuais de todos os principais navegadores. Em particular, se você usa o Internet Explorer (IE) da Microsoft, deve estar usando a versão mais recente. Dê uma olhada na lista de [navegadores suportados.](https://docs.github.com/en/get-started/using-github/supported-browsers)

</aside>

## Passo 2: Instale o Git

No coração do GitHub está o *Sistema de Controle de Versão* de código aberto chamado Git. O Git é responsável por tudo  que acontece localmente no seu computador relacionado ao GitHub.

Vamos verificar se o Git já não está instalado em sua máquina. Abra o **Terminal** se estiver em um Mac ou **PowerShell** se estiver em uma máquina Windows e digite:

```bash
git --version
```

Após executar o código no Terminal, você deverá ver algo do tipo:

```bash
git version 2.22.0.windows.1
```

### Baixe e Instale o Git

Caso não tenha o Git instalado, faça download e instale a versão mais recente do Git. neste link: [https://git-scm.com/downloads](https://git-scm.com/downloads)

- Se você estiver trabalhando no Windows, é recomendado usar o Git Bash que já vem instalado com o pacote Git;
- Se você estiver trabalhando em um Mac ou outro sistema baseado em Unix, você pode usar o aplicativo Terminal integrado.

### Configure o seu nome de usuário no Git

O Git usa um nome de usuário para associar os commits a uma identidade, ou seja, toda vez que você enviar o seu código para o GitHub esse nome de usuário do git será usado para te identificar como autor do código enviado dentro do repositório no GitHub. 

<aside>
💡 O nome de usuário do Git é diferente do nome de usuário do GitHub.

</aside>

Para configurar o seu nome de usuário do Git para todos os seus repositórios no computador, faça:

1. Abra o Git Bash.
2. Defina um nome de usuário do Git

```bash
git config --global user.name "Ada Lovelace"
```

1. Confirme que você configurou o nome de usuário corretamente no Git, digitando:

```bash
git config --global user.name
> Ada Lovelace
```

## Passo 3: Clone um Repositório

Após instalar e configurar o Git vamos testar a instalação, para isto, experimente clonar um repositório do GitHub para sua máquina. Clonar um repositório significa criar uma cópia local no seu computador dos arquivos que estão armazenados em um repositório do GitHub.

Abra o **Terminal** se estiver em um Mac ou **PowerShell** se estiver em uma máquina Windows e digite:

```bash
git clone https://github.com/githubschool/scratch
```

Se tudo estiver funcionando corretamente, os arquivos do repositório *scratch* pertencentes ao usuário *githubschool* do Github, serão baixados para a sua máquina, e, você verá a seguinte mensagem no terminal:

```bash
Cloning into 'scratch'...
remote: Enumerating objects: 9, done.
remote: Total 9 (delta 0), reused 0 (delta 0), pack-reused 9
Unpacking objects: 100% (9/9), done.
```

## Passo 4: Prepare o seu Editor de Texto

Para esta aula, usaremos um editor de texto básico para interagir com nosso código, e, esteja pronto para trabalhar com linha de comando usando o terminal. Você pode usar quase qualquer editor de texto, mas terá mais sucesso se usar qualquer um dos seguintes editores:

- Visual Studio Code: [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
- Atom: [https://atom.io/](https://atom.io/)
- Sublime: [https://www.sublimetext.com/3](https://www.sublimetext.com/3)
- Notepad++: [https://notepad-plus-plus.org/downloads/](https://notepad-plus-plus.org/downloads/)
- Notepad, Vi or Vim, GitPad.

<aside>
💡 Use o **Visual Studio Code** 😉

</aside>

Após instalar um editor de texto, verifique se você pode abri-lo à partir da linha de comando no terminal. Por exemplo, se tudo estiver instalado corretamente, se você digitar o comando abaixo no **Terminal** ou **PowerShell**, o *Visual Studio Code* vai abrir.

```bash
code .
```

# Repositórios

Um repositório contém todos os arquivos do seu projeto e o histórico de revisão de cada arquivo. Você pode discutir e gerenciar o trabalho do projeto dentro do repositório. Geralmente são usados para organizar um único projeto e podem conter: pastas e arquivos, imagens, vídeos, planilhas e conjuntos de dados. Os repositórios incluem um arquivo README escritos na linguagem de marcação Markdown, com informações sobre o seu projeto, bem como, um arquivo indicando qual é a licença do seu projeto.

<aside>
💡 Um repositório pode ser um lugar onde você armazena ideias, recursos ou até mesmo compartilha e discute coisas com outras pessoas

</aside>

## Crie um Repositório Git local

Abra o **Terminal** se estiver em um Mac ou **Git Bash** se estiver em uma máquina Windows. Usando o comando `cd` (*change directory*)  navegue para o diretório onde você deseja colocar a pasta do seu projeto.  Por exemplo, digite o comando abaixo, caso queira colocar a pasta do seu projeto na Área de Trabalho do Windows.

```bash
cd ~/Desktop
```

Use o comando `mkdir`  (*make directory*) para criar a pasta do seu projeto através da linha de comando. 

```bash
mkdir sistema-erp
```

Usando novamente o comando `cd` (*change directory*), entre na pasta *sistema-erp* que acabamos de criar para nosso projeto.

```bash
cd sistema-erp
```

Execute o comando `git init` para inicializar um novo repositório git no diretório raiz da pasta *sistema-erp.*  Após executar o comando você vai ver a seguinte mensagem: *"Initialized empty Git repository in ...”*; no terminal.

```bash
git init
```

### Adicione um Novo Arquivo no Repositório

Vamos adicionar um novo arquivo para nosso repositório usando comando `touch`. 

```bash
touch arquivo.txt
```

<aside>
💡 Esse comando não está disponível no **Prompt de Comand** ou **PowerShell** em ambientes Windows, por isso, **use o Git Bash** que já vem instalado com o pacote Git.

</aside>

Depois de criar o novo arquivo, vamos usar o comando `git status` para ver quais arquivos estão sendo monitorados pelo Git em nosso repositório.

```bash
git status
```

```bash
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        **arquivo.txt**

nothing added to commit but untracked files present (use "git add" to track)
```

Após executar o comando `git status` você vai ler na tela uma mensagem dizendo que o Git viu que você criou o arquivo chamado **`arquivo.txt`** , porém, a menos que você use o comando ****`git add` ele será ignorado pelo git. Execute o comando abaixo para que o git monitore o arquivo que criamos:

```bash
git add arquivo.txt
```

Para adicionar todos os arquivos de uma pasta ao git, use o **ponto final** ao invés de informar o nome do arquivo. 

```bash
git add .
```

<aside>
💡 Essa ação será necessária sempre que qualquer arquivo for alterado ou acrescentado na pasta do seu proejto. Então, quando estiver pronto para salvar uma cópia do estado atual do projeto, você prepara as alterações com o comando `git add` , em seguida, você faz commit no histórico do projeto com `git commit`

</aside>

### Faça um commit

> Você pode salvar pequenos grupos de mudanças significativas como commits.
> 

Vamos criar nosso commit, executando o comando abaixo:

```bash
git commit -m "Primeiro commit"
```

Após executar o terminal irá mostrar as seguintes mensagens, com a quantidade de arquivos alterados, e, quantas inclusões e exclusões foram feitas.

```bash
[master (root-commit) f1d0d18] primeiro commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 arquivo.txt
```

Assim como salvamos um arquivo que foi editado, um commit registra alterações em um ou mais arquivos. O Git atribui a cada commit um ID exclusivo, denominado SHA ou hash, que identifica:

- Cada uma das alterações feitas;
- O momento em que as alterações foram feitas;
- O autor das alterações.

Ao fazer um commit, você deve incluir uma mensagem que descreva brevemente as alterações. A mensagem no final do commit deve ser algo relacionado ao conteúdo do commit, por exemplo: uma nova funcionalidade, uma correção de bug, correção de erros de digitação.

<aside>
⚠️ **Não coloque uma mensagem sem significado**, tais como: "asdfadsf" ou "foobar".

</aside>

## Crie um Repositório no Github

Acesse [https://docs.github.com/pt/get-started/quickstart/hello-world#creating-a-repository](https://docs.github.com/pt/get-started/quickstart/hello-world#creating-a-repository) e siga o passo a passo para criar um novo repositório chamado: **gestao-empresarial**; na sua conta do GitHub. 

<aside>
💡 Os nomes dos repositórios devem ser escritos em letra minúscula (caixa baixa), usando traço (-) para separar espaços em brancos. Não utilize acentos nem caracteres especiais nos nomes dos seus respositórios.

</aside>

Após criar um repositório no Github, você pode:

- Clonar o repositório para sua máquina, ou seja, fazer uma cópia local; usando o comando `git clone`
- Enviar um repositório git local para o github, através da linha de comando.

## Adicione seu Repositório Local no Github

Para adicionar o repositório git que criamos em nossa máquina no github, execute os comandos abaixo:

```bash
git remote add origin https://github.com/<NOME_DE_USUÁRIO>/gestao-empresarial.git
git branch -M main
git push -u origin main
```

<aside>
⚠️ Não esqueça de substituir <NOME_DE_USUÁRIO> pelo seu nome de usuário do GitHub

</aside>
