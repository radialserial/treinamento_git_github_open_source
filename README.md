## Este repositório foi criado para o treinamento de versionamento de código EducaGuardIA

# Configurando o Git e Github

* Crie uma conta no Github
* No Git Bash digite esse comando

`git config --global user.name "UsuarioGithub"`
`git config --global user.email "emailDoGithub"`

#### Verificando

`git config --list`

# Conectando Git ao GitHub

* Verificar se tem pares de Chave SSH

`ls -al ~/.ssh`
    >Provavelment o comando vai retornar um erro dizendo que a chave não existe, crie uma

*  Autenticação SSH

ssh-keygen -t ed25519 -C "emailUsuarioGit@hotmail.com"
    > Verifique novamente | `ls -al ~/.ssh`

* Copie a Chave para o GitHub

    > Dentro da sua conta, em configurações, acesse a aba SSH e GPG Keys
    > Clique em New SSH Key
    > Volte para o Git Navegue até o diretório em que a chave foi criada
`cd /c/Users/seuUser/.ssh/` **Essa pasta é dada na hora da criação da chave** aperte o enter
    > digite ls ou dir para listar os documentos
    > Entre com o comando
`cat id_ed25519.pub` **Aqui precisa ser a chave pública encontrada na pasta**
    > copie a chave e cole no GitHub

### Faça um Fork desse Repositório para o seu GitHub
### Faça um Clone do Repositório Remoto para sua máquina

`git clone https://github.com/SEU_USERNAME/treinamento_git_github_open_source.git` **copie o link do fork do seu repositório**

### Adicione o remote upstream para manter seu repositório local atualizado. 
Por exemplo: `git remote add upstream https://github.com/maysamkt/treinamento_git_github_open_source.git`;
    > Utilize o comando `git pull upstream main` para baixar e mesclar as alterações no seu repositório local com base na branch `main` deste repositório original de onde você fez o fork, ou `git fetch upstream main` para baixar sem mesclar. 

### Crie/Referêncie uma nova **branch** e nomeie como 
`feat/colaborador/SEU_USERNAME`: `git checkout -b feat/colaborador/SEU_USERNAME`;
    > Exemplo: `git checkout -b feat/colaborador/maysamkt`

### Dentro da pasta [`colaborador`](https://github.com/maysamkt/treinamento_git_github-open-source/tree/main/colaborador), crie um arquivo em Markdown (extensão `.md`) e nomeie com o mesmo nome do seu usuário no GitHub;
    > Exemplo: `maysamkt.md` <br>

###  Desenvolva o seu Arquivo. Para isso, você pode ver exemplos de sintaxe markdown na pasta [`community`](https://github.com/maysamkt/treinamento_git_github-open-source/tree/main/colaborador);

### Adicione suas alterações a "staging area" com o comando `git add colaborador/SEU_USERNAME.md`;
### Crie um commit e adicione a mensagem indicando a adição do seu arquivo `git commit -m"feat: add SEU_USERNAME profile"`;
### Envie as alterações para o seu repositório remoto `git push origin feat/community/SEU_USERNAME`;
### Crie um *Pull Request*

# Vendo como fazer o commit diretamente pelo vscode
    > mostrado em tempo real

Esse projeto open source foi baseado no projeto da DIO.me que vocês podem encontrar no link [DIO.ME](https://github.com/digitalinnovationone/dio-lab-open-source.git).

