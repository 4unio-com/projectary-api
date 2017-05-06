Atualiza��o de 25-04-2017 19:48

-A vagrant file ir� criar uma m�quina virtual com mysql e nodejs
-Instalar o Vagrant de https://www.vagrantup.com/downloads.html
-Instalar o Cygwin e nos plugins, instalar o openssh (procurar em net)
-Instalar a Virtualbox (a m�quina virtual ir� ser criada na Virtualbox, mas n�o � necessario abrir a Virtualbox)
-ir a linha de comandos e aceder a pasta onde est� a Vagrantfile (Ex. cd\PSI\Trabalho)
-Convem que esta pasta tenha os repositorios do GIT porque a m�quina virtual mapeia a pasta onde est� a VagrantFile tornando-a acessivel
 a partir do sistema operativo Host e do Guest.
- P.S. SE EXISTIR ALGUMA VAGRANT MACHINE CRIADA, UTILIZAR O COMANDO "vagrant destroy"
 -executar o comando "vagrant up" dentro da pasta da VagrantFile, ir� sacar a maquina e configur�-la de acordo com o ficheiro
-para aceder por ssh, fazer "vagrant ssh" e ter� acesso � shell da m�quina (� necess�rio o cygwin instalado, com o putty n�o d�)
-em shell do ubuntu, a pasta partilhada com o SO do host est� em /vagrant (nao confundir com /home/vagrant). Esta pasta � a mesma onde est�
 a VagrantFile e tudo o que for aqui criado est� sincronizado entre a m�quina virtual e a pasta no host
-para sair da shell fazer "exit" na shell da m�quina virtual
-para parar a m�quina virtual, depois de ter sa�do da shell para a linha de comandos do Sistema operativo host, fazer "vagrant halt"
-se quiser "destruir" a m�quina virtual (por exemplo pra libertar espa�o), basta fazer "vagrant destroy". A VagrantFile continua na pasta e
 todo o processo pode ser repetido, no entanto todos os dados criados na maquina virtual s�o eliminados quando se faz "vagrant destroy"
-Se quiser remover definitivamente a m�quina virtual, fazer "vagrant box remove ubuntu/xenial64" (vagrant box remove nome_da_maquina)


- Mysql Instalado
- node js instalado
- alteradas credenciais do root do mysql para a password '123qwe'
- alterados os hosts com permiss�o para aceder ao mysql para todos (%)
- alterado o bind-address do mysql para 0.0.0.0 e permitir liga��o a partir de outros hosts
- portas redirecionadas : 8080 -> 8080 (backend api), 3306 -> 33060 (mysql)
- portas redirecionadas : 3000 -> 3000 e 3001 -> 3001 (frontend)
- existe uma linha comentada de n�o utiliza��o de links simbolicos para quem tiver problemas em 
  linha de comandos de windows (de acordo com o Andr� apenas em modo normal, em modo de Admin n�o d� erro)

IMPORTANTE : Alguns colegas est�o a ter problemas com a instala��o autom�tica do script da Vagrantfile.
Em alguns casos foi detetado que tal se devia a terem a pasta do projecto numa path demasiado longa ou com
caracteres especiais. Devem ter a pasta do projecto o mais junto da rais e numa pasta com o nome limpo, 
exemplo : c:\PSI 
e ter os repositorios clonados dentro dessa pasta

para executar o servidor da aplica��o, entrar na vagrant machine com "vagrant ssh" e fazer :
cd /vagrant/projectary-api
npm run frontend
ou
yarn run frontend

e no host aceder a http://127.0.0.1:8080