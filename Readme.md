#Git-course

Este é um repositorio teste para ensinar como o git funciona.

Saiba mais no link: [willianjusten.com.br](http://willianjusten.com.br)

Gostou do curso? Quer mais? Ajude com uma doação, até um café é válido =)

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/websrc?cmd=_s-xclick&hosted_button_id=UTMFZUHX6EUGE)

Outros cursos em : [Willian Justen Cursos](http://willianjusten.teachable.com)

-------------------------
Comands

#Configurando nome de usuário, email e editor no git

git config --global user.name "Mariana Brito"

git config --global user.email "mariana.bsouza@hotmail.com"

git config --global core.editor sub


#Mostrando user ou email

git config user.user

git config user.name


#Limpar tela

Digite clear e aperte enter


#Lista de várias informações do meu git

git config --list


#Criando páginas/pasta dentro do terminal

mkdir + nome da pasta


#Entrando na pasta

cd + nome da pasta


#Saindo da pasta

cd ..

#Iniciando repositório

git init


#Lista de arquivos

ls


#Como está o repositório no momento

git status


#Atalho Sublime

subl


#Para commitar

git commit -m "--"
(-m uma mensagem do que fez)

git commit -am “—“
(já faz o add de tudo)

#Lugar atual

master ou outra branch

*Para commitar precisa de add .


#Histórico de coisas feitas

git log
git log --decorate = de qual branch para qual branch, qual tag gerada
git log --author="Mariana" = Filtrar por author
git shortlog = ordem alfabética dos ocntrinuintes
git log --graph = mostra o que acontece com o branch e suas versões


#Diff

git diff = mostra as atualizações feitas antes de commitar

git diff --name-only = dizer apenas o nome do arquivo a ser modificado

git commit -am = pode ser feito quando já mexeu nesse arquivo, quando já commitou antes

git show = mostra as atualizações feitas


#Resetar erros

git checkout Readme.md(ou .) = vai retornar o arquivo antes da edição

git reset HEAD = quero remover o stage(etapa) do meu arquivo do local que estou

git reset --soft = desfaz o commit, mas as alterações continuam(no git add{verde})

git reset --mixed = defaz o commit e o git add(vermelho)

git reset --hard = paga tudo, commit e alterações

*sempre tem que escolher o penúltimo commit


#Criando repositório remoto(GITHUB)

git remote = diz que já existe repositório origin

git remote -V = mais informações, endereço dele

git push = ele envia os arquivos, modificações para o repositório determinando

git push -u origin master = envia para a o repositório determinado
(-u = para trackear para não ter que digitar tudo novamente)
(origin = vai para)
(master = vem)


#Clonando repositórios remotos

copiar o endereço SSH ou https lá do github
digitar git clone e colar o endreço e e renomear o arquivo com outro nome e colocar clone


#Ramificação(Branch)

é um ponteiro móvel que leva a um commit


#Criando um Branch

git checkout -b testing
(-b = dizendo que está criando uma branch)
(testing = nome da branch)

git branch = branchs existentes e qual branch está no momento

#Movendo e deletando branchs

git checkout = git checkout testing ou master = vai pral qual branch quer
(testing e master = nome das branchs)

#Apagando

git branch -D testing


#Entendendo o merge e rebase

serve para unir branchs

#Merge
uni todas branchs em uma só na ordem certa

#Rebase
uni todas branchs na ordem certa quando um contribuinte está trabalhando e enviando de outro local


#Como sair do vim

aperta a tecla "esc" e digita ": wq"


#Stash

git stash = guardar modificações que ainda não foram commitadas numa pasta/arquivo que eu possa chamar depois quando necessário

fica em estado de WIP

#Trazendo de volta o arquivo

git stash apply

git stash list = mostra a lista de todos os stashs que estou fazendo

git stash clear = limpa tudo e todas modificações e stash guardados

#Atalhos

git status = git s = git config --global alias.s status


#Versionando com Tags

git tag -a q.0.0 -m "Readme.md"
(1.0.0 = versão)
(-a = com algum dado)

#Subindo

git push origin master --tags

#Listando todas as tags

git tag

#Revertendo

git revert
(git revert + número do commit)
(mas mantém o histórico do commit)


#Apagando tags e branches remotos

-tags
git tag -d 1.0.1
depois precisa subir
git push origin master —tags(mas ainda não apagou no repositório remoto)
apagando no remoto
git push origin :1.0.0

branch
mesma forma que a tag
git push origin :test