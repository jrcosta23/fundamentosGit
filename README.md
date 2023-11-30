# tutorial de Git e Github na prática 

## instalação do Git
* [link com downloads](https://git-scm.com/downloads)

## versionamento local do projeto
* acesse a pasta no qual o projeto está armazenda
* clique com o botão direito do mouse e selecione **open Git bash here**
* `git init`para inicializar o repositório 

  será criada uma pasta chamada `.git`, **não** a apague**
* digite `git add .` para colocar os arquivos do projeto na **área de staging**
<img src="https://i1.wp.com/www.markus-gattol.name/misc/mm/si/content/git_git_add.png">
*  digite `git commit -m "primeira verão do projeto"`para versionar **localmente** o projeto
   digite  `git banch  -M "main"` para renomear a branch  principal de `maste` para `main`

    ##criação de um repositório remoto no Github
  *acesse a conta do Githb e clique em `new` para criar um novo repositório

  coloque um nome para o repositório e preencha as informações do projeto, como a decriação
  * para enviar o commit do repositório local (isto é, em sua máquina) para um repositório
  na plataforma do Github, digite por linha de comando `git remote add origin <link do
  repositório>`

* dessa forma, o repositório local já está vinculado ao repositório remoto do Gihub,
  entrentanto a versão (isto é, o commit) não sobe automaticamente, por isso é necessárop
  digite:**`git push -u origin main`**
* por fim, recarregar a página do Github e verifique se o projeto foi versionado **remotamente**

  ## e quando o projeto for alterado?

  * ao editar um arquivo já versionado ou mesmo criar um novo arquivo não existia na versão
  * anterior, **não** é necessário inicializar novamente o Git por meio do comando `git init`, sendo assim execute os seguindor comandos em ordem:
  
  `git add.`

  `git status` para verificar os arquivos que estejam aguardando na staging area

  `git commit -m "<escreva uma mensagem detalhamdo o que foi alterado>"`

 `git push`

 como é possível notar, também **não** é necessário renomear mais uma vez a branch (pois
 ela já estará renomeada como  cmain`), além disso, o link do repositório remoto já estará
 armazenado, por isso o comando  `git remote add origin <link do repositório>` só é
 utilizado uma única vez

  * no Github será possível verificar todas as versões enviadas clicando em `commits`,de dedo que todas as alterações feita esterão demostradas
  
  o sinal verde `+` represnta o que foi adicionado/modificado no versionamente, enquanto o
  sinal vermelho `-` representa o foi excluido de uma versão para outra 

  ## branch

  * até então, todos os versionamentos ocorreram na **ramificação para (branch `main`)**
  * para criar uma nova branch, isto é, uma nova linha cronológica adicional/altenativa a 
    principal que possa posterionamente se juntar a `main`, digite `git ckeckout -b <nome da nova branch>`, assim o terminal Git sairá da branch `main`, criar uma nova com o nome que desejar e entrará nela, por exemplo: `git ckeckout -b novobotão`
    * com uma nova branch criada, utilize os comandos já explicados;
  
    `git add`

    `git status`

    `git commit -m "<escreva uma mensagem>"`

     no Github, as branch s aparecerão assim:

    <img src="img/imgBranch.png">

    * se necessário retorna para branch `main` pelo terminal do Git, digite  `git ckeckout main
 