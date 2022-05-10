#GIT.

Quando perguntado sobre o porquê do nome, Linus Torvalds satirizou sobre o termo "Git", uma gíria em inglês britânico para cabeça dura, pessoas que acham que sempre têm razão, argumentativas, podendo ser também pessoa desagradável ou estúpida.

"Silence for Sucess"



### Link para download

[Git - Downloads (git-scm.com)](https://git-scm.com/downloads)

###Blobs (objetos)
Contém metadados do GIT que são o tipo do objeto, o tamanho da string, o tamanho do arquivo... Esses objetos não posuem nomes, datações ou outros metadados.

###Tree (árvores)
Elas armazenam blobs, o blob sendo o bloco básico de composição. É o equivalente a um diretório, ele contém um lista de nomes de arquivos, cada um com bits que informam o tipo e o nome do blob, da árvore, ligação simbólica ou conteúdo de diretório que pertence a este nome. Este objeto descreve o estado da árvore de diretório.

###Commit (entrega)
Agora temos o objeto mais importante de todos que é o commit, o commit e o objeto que vai juntar tudo, que vai dar sentido pra alteração que você está fazendo. O commit liga árvores de objetos junto com um histórico. Ele contém o nome de uma árvore de objetos (da raiz de diretórios), datação, uma mensagem de log, e os nomes de zero ou mais objetos-pai de commit. 'O commit é unico para cada autor."

###Untracked 
O GIT não tem conhecimento deles, não rastreados.

###Tracked
O GIT tem conhecimento dele, sempre atraves do comando $git add ...

###GIT status:

1- Unmodified (não modificado)
2- Modified (modificado)
3- Staged (Preparado)
4- Commited (consolidado)

###Repositório
É onde seu código vive, pode ser visto como um projeto dentro do GIT, ou seja, cada repositório tem suas próprias depêndencias.

###Branch
É o conceito central do GIT. Todo repositório inicia com uma branch (tronco) chamada main (master). A partir desse entroncamento principal outras branches são criadas para dar vida a outras funcionalidades e alterações no código.

##Principais comandos do GIT.

###GIT config
Este comando é utilizado para configurar o nome do autor e endereço de e-mail que serão usados nos seus commits, importante ressaltar que é o nickname e o e-mail usado no GITHUB.
$git config --global user.name (nome ou nickname)
$git config --global user.email (nome@provedor.com)

###GIT Init
Comando utilizado para criar novos repositórios.
$git init

###GIT Clone
Cria uma cópia local de um repositório remoto.
$git clone {link repositório}

###GIT add
Adiciona um ou mais arquivos modificados localmente à área de stage para serem incluidos no commit.
$git add {nome do arqivo}
$git add * (todo o conteúdo)

###GIT commit
Confirma as mudaças localmente. (Não altera o servidor remoto)
$git commit -m "mensagem do commit"

###GIT push
Envia as alterações feitas em uma branch específica ou em todas as branches (parametro --all) para o servidor remoto.
$git push {nome do arquivo} {branch}
$git push --all

###GIT status
Mostra o estado da sua branch atual, lista os arquivos que você já alterou e aqueles que precisam ser adicionados a um commit.
$git status

###GIT branch
Comando utilizado para gerenciar os branches. Com ele é possivel criar, listar ou deletar branches.
	1. Criar uma nova branch:
$git branch {nome da branch}
	2. Listar branches:
$git branch
	3. Deletar uma branch:
$git branch -d {nome do arquivo}

###GIT checkout
Comando utilizado para troca de branch do seu projeto. Se utilizado o parâmetro -b cria uma nova branch e já troca sua branch atual pela criada.
$git checkout {branch}
$git checkout -b {nova branch}

###GIT merge
Combina as mudanças de uma branch em outras. Esse comando vai trazer todas as alterações de outras branch para sua branch atual.
$git merge {branch origem}

###GIT log
Traz o histórico de alterações da branch atual. Cada parâmetro altera a saída do comando

	1.$git log --decorate
Altera a saída, decorando-a para ficar visualmente mais bem organizada.

	2.$git log --oneline
Um commit por linha

	3.$git log --all
Traz todos os commits de todas as branches

	4.$git log --grafh
Estiliza a saída em formato de grafo

	5.$git log --help
Serve para saber todos os parametros do comando, serve para outros comandos também

###GIT clear
Limpa a tela de trabalho no git bash
$clear






