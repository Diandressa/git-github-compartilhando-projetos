<!-- 
# Título  

## Descrição
O que faz o app
Com o que ele foi construído 
Por que foi contruído

## Pré requisitos
  instalaçao node, git...

## Instrução de instalação
```bash
  npm install
```

## Instrução de uso
  Como utilizar o projeto em passos ou em bash. Podemos usar prints ou gifs

## Licença

### Permissão para uso comercial
### se inspirar
### Educacional
### Não comercial

## Contribuição

## Gitflow 
Quais padrões os dev podem seguir para contribuir

## badges

[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE) <br>
https://github.com/Ileriayo/markdown-badges/blob/master/README.md

## Contruibuidores  ou Owner (donos do projeto)
  reconhecimentos

Podemos usar templates de README
https://github.com/Fernanda-Kipper/Readme-Templates?tab=readme-ov-file 
-->

# [Curso Git e GitHub: compartilhando e colaborando em projetos - Alura](https://cursos.alura.com.br/course/git-github-compartilhando-colaborando-projetos)

![Imagem do curso](/img/img.jpg)


## Descrição
Anotações das aulas e comandos relevantes.

## Pré requisitos
  * git
  * github

## Comandos 

### Criar repositório e comitar

Comandos               | Descrição
---------              | ------
git init               | Sincroniza o repositório
git add .              | Adiciona alterações no commit
git commit -m ""       | Comita com o título
git commit -m "" -m "" | Comitar com o título e descrição
git branch -M main
git remote add origin {URL do repositório} | origin é o nome que damos para repositório
git push -u origin main
git pull origin main | Traz as mudanças do repositório remoto

### Definir usuário do commit

Comandos                          | Descrição
---------                         | ------
git config --global user.email "" | Defini o email em todos os projetos
git config --global user.name ""  | Defini o nome em todos os projetos
git config user.email ""  | Defini o email naquele projeto (local)
git config user.name ""  | Defini o nome naquele projeto (local)
git config user.email | Verifica o email informado
git config user.name | Verifica o nome informado

### Comandos Repositórios
Comandos                 | Descrição
---------                | ------
git remote -v            | Listar os repositórios
git remote remove origin | Remover o repositório origin
git remote set -URLatual origin URLnova | Altera URL de um repositório remoto
git remote rename origin novoapelido | Altera apelido de um repositório remoto

### Comandos verificar estado dos Commit e Repositórios
Comandos                 | Descrição
---------                | ------
git status               | Indica quais arquivos foram modificados
git clone URLrepositorio | Clonar o repositório
git log                  | Listar histórico de commits (quais commits e quem fez)
git log --oneline        | Exibe apenas as mensagens dos commits
git remote               | Listar os repositórios . Ex: origin
git remote -v            | Mostra a URL que o repositório está conectado
git diff                 | Mostra as diferenças e mudanças entre os commits


## Alterar commits
Comandos                 | Descrição
---------                | ------
git revert IDdoCommit    | Desfaz um commit específico, cria um novo commit com essa reversão. git log mostra se reverteu
git --amend -m "Nova mensagem | Alterar a mensagem do último commit 

### Apagar/Resetar commits
Indicado quando não subimos o commit para o repositório remoto
Comandos                 | Descrição
---------                | ------
git log    | Consultar o ID do commit
git reset --hard IDdoCommit anterior ao que queremos deletar, reverte até aquele ponto.

## Reverter commits
Comandos                 | Descrição
---------                | ------
git revert -n IDdoCommit | Reverte vários commits, depois do revert preciso realizar um novo commit

### Para adicionar Colaboradores
no github -> settings -> colaboradores -> add people

### Anotações
tecla `q`
sai do terminal

README.md com markdown para documentar o projeto
Podemos usar templates de README

[Repositório Fernanda Kipper - templates](https://github.com/Fernanda-Kipper/Readme-Templates?tab=readme-ov-file) 

[Repositório com Badges](https://github.com/Ileriayo/markdown-badges/blob/master/README.md)

Criar um arquivo com os logs dos commits

`git log > logs.txt`

### Ignorar arquivos

Precisamos criar o arquivo para dizer para o git quais diretórios e arquivos ele vai ignorar na hora do add .

`.gitignore`

No arquivo colocamos os caminhos dos arquivos que queremos ignorar, cada linha um arquivo.

Se colocarmos *.css todos os arquivos com extenção CSS serão ignorados

temp/ -> todos os arquivo na pasta temp criado dentro do projeto serão ignorados

Adicionamos no commit o gitignore e subimos as mudanças

Existem site geradores de gitignore: [gitignore.io](https://www.toptal.com/developers/gitignore/)

### Compartilhando Códigos com Gist

Compartilhar só um trecho do projeto atravás de uma URL

ir no site github -> `+ ▼` -> `<> New gist`
Compatilha a linha de código deseja 

## Gerar Chave SSH

Configuração de segurança para permitir a pessoa específica, com a conta específica que foi vinculada no github, fazer os commits

`git clone urlSSH` ou `git remote add origin urlSSH`

>The authenticity of host 'github.com (20.201.28.151)' can't be established.   
ED25519 key fingerprint is chaveSSHgeradanoterminal
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 

Yes

> Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.      

Please make sure you have the correct access rights
and the repository exists.

Não reconhece meu computador, preciso permitir o acesso na minha conta do github

Ir na minha conta > setting > SSH and GPG keys > `New SSH Keys`

Precisamos colocar a chave (key) no formulário.

A chave foi passada no terminal.
Podemos recupera-la em pasta do nosso usuário > .ssh (pasta oculta) > gerar no terminal o arquivo com o comando

`ssh-keygen -t ed25519 -C "email@gmail.com"`

Pergunta onde quero salvar o arquivo, posso dar um enter e ele salva default na pasta .ssh

Pergunta se quero criar uma senha toda vez que sincronizar com o github, se eu dar entre não é criado uma senha

Gera dois arquivos, um da chave privada e um da pública. Precisamos abrir a chave pública. Abrimos com o bloco de notas.

Colocamos essa chave no formulário no github

Pronto! ✅

[Como gerar chave SSH](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## Licença
[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE) 
