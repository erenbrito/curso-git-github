# Curso Git e Github

Este é um repositório para guardar minhas anotações do curso de Git e Github do Willian Justen.

---

## Comandos

- **Como configurar nome de usuário, email e editor no git**
```
git config --global user.name "Mariana Brito"
git config --global user.email "mariana.bsouza@hotmail.com"
git config --global core.editor sub
```

- **Mostrando o nome e email configurados**
```
git config user.name
git config user.email
```

- **Mostra todas as informações configuradas do meu git**
```
git config --list
```

- **Criando pasta dentro do terminal**
```
mkdir nomeDaPastaDesejada
```

- **Entrando na pasta**
```
cd nomeDaPastaDesejada
```

- **Saindo da pasta**
```
cd ..
```

- **Iniciando repositório git dentro da sua pasta**
```
git init
```

- **Mostra os arquivos da pasta**
```
ls
```

- **Como está o repositório no momento**
```
git status
```

- **Para commitar**
```
git add nomeDoSeuArquivo.html
git commit -m "Adicionei o arquivo e fiz o commit"
```
ou
```
git commit -am "Adicionei o arquivo e fiz o commit tudo em um comando só"
```

- **Histórico de alterações feitas**

```
git log #Mostra todos os logs
git log --decorate #Histórico mais detalhado
git log --author="Mariana" #Filtrar por autor
git shortlog #Ordem alfabética dos contribuintes
git log --graph #Mostra o que acontece com o branch e suas versões
```

- **Vendo as alteracões antes de commitar**
```
git diff #Mostra as atualizações feitas antes de commitar
git diff --name-only #Dizer apenas o nome do arquivo a ser modificado
git commit -am #Pode ser feito quando já mexeu nesse arquivo, quando já commitou antes
git show #Mostra as atualizações feitas
```

- **Desfazendo alterações**
```
git checkout Readme.md(ou .) #Vai retornar o arquivo antes da edição
git reset HEAD #Quero remover o stage(etapa) do meu arquivo do local que estou
git reset --soft #Desfaz o commit, mas as alterações continuam(no git add{verde})
git reset --mixed #Desfaz o commit e o git add(vermelho)
git reset --hard #Apaga tudo, commit e alterações
```
**Sempre tem que escolher o penúltimo commit*

- **Enviando o seu projeto para um repositório remoto (GITHUB)**
```
git remote #Diz se já existe algum repositório origin
git remote -V #Mais informações, endereço dele
git push #Envia os arquivos, modificações para o repositório determinando
git push -u origin master #Envia para a o repositório origin na branch master
```

- **Clonando repositórios remotos**

Copie o endereço SSH ou https do repositório (disponível no github) e no terminal digite:
```
git clone https://github.com/nomeDoUsuario/nomeDoRepositorio.git nomeDaPastaDesejada
```

- **Criando Branchs**

É um ponteiro móvel que leva a um commit
```
git checkout -b nomeDaBranchDesejada #-b é o comando responsável por criar uma branch e mudar pra ela
git branch #Mostra todas as branchs exixtentes e qual branch está no momento
```

- **Trocando de branch**
```
git checkout master #Vai para a branch master
git checkout nomeDaBranchDesejada #Vai para a branch "nomeDaBranchDesejada" apenas se ela existir
```

- **Deletando uma branch**
```
git branch -D nomeDaBranchDesejada
```

- **Entendendo o merge e rebase**

Os comandos **merge** e **rebase** servem para unir branchs, mas cada um funciona de uma forma diferente:

 > **Merge**
Une todas branchs em uma só na ordem certa.

> **Rebase**
Une todas branchs na ordem certa quando um contribuinte está trabalhando e enviando de outro local.


- **Guardando pra depois**
Quando você tem uma modificação que ainda não pode ser commitada e quer guardar para chamar depois quando necessário:
```
git stash #Fica em estado de WIP - Work In Progress
git stash list #Lista todos os arquivos em stashs
git stash apply #Traz um arquivo que está no stash de volta
git stash clear #Limpa todas as modificações guardadas no stash
```

- **Versionando com Tags**
Faz uma nova versão do seu projeto relacionando com os últimos commits
```
git tag #Mostra todas as tags
git tag -a 1.0.0 -m "Versão 1.0.0" #Cria uma nova tag onde -a especifica o numero da versão e -m especifica a mensagem
git push origin master --tags #envia a nova tag para o repositorio remoto
```

- **Revertendo um commit**
Desfaz as alterações que foram feitas em um commit, mas mantém ele no histórico
```
git revert 123abc #onde 123abc 'é o número do commit
```

- **Apagando tags e branches do repositório remoto**
```
git tag -d 1.0.0
git push origin master —tags
git push origin :1.0.0
```
```
git branch -d nomeDaBranchDesejada
git push origin :nomeDaBranchDesejada
```

- **Criando atalhos**
```
git config --global alias.s status #Cria um atalho para o git status
git s #agora podemos digitar apenas git s em vez de git status
```

- **Dicas extras**
 - Para limpar a tela digite clear a aperta enter
 - Para sair do VIM aperta a tecla esc, digita ":wq" e aperta enter
