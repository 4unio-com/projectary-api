-A vagrant file ir� criar uma m�quina virtual com mysql (mariadb), nodejs e go
-Instalar o Vagrant de https://www.vagrantup.com/downloads.html
-Instalar o Cygwin e nos plugins instalar o openssh (procurar em net)
-Instalar a Virtualbox (a m�quina virtual ir� ser criada na Virtualbox, mas n�o � necessario abrir a Virtualbox)
-ir a linha de comandos e aceder a pasta onde est� a VagrantFile (Ex. cd\PSI\Trabalho)
-Convem que esta pasta tenha os repositorios do GIT porque a m�quina virtual mapeia a pasta onde est� a VagrantFile tornando-a acessivel
 a partir do sistema operativo Host e do Guest.
-executar o comando "vagrant up" dentro da pasta da VagrantFile, ir� sacar a maquina e configur�-la de acordo com o ficheiro
-para aceder por ssh, fazer "vagrant ssh" e ter� acesso � shell da m�quina (� necess�rio o cygwin instalado, com o putty n�o d�)
-em shell do ubuntu, a pasta partilhada com o SO do host est� em /vagrant (nao confundir com /home/vagrant). Esta pasta � a mesma onde est�
 a VagrantFile e tudo o que for aqui criado est� sincronizado entre a m�quina virtual e a pasta no host
-para sair da shell fazer "exit" na shell da m�quina virtual
-para parar a m�quina virtual, depois de ter sa�do da shell para a linha de comandos do Sistema operativo host, fazer "vagrant halt"
-se quiser "destruir" a m�quina virtual (por exemplo pra libertar espa�o), basta fazer "vagrant destroy". A VagrantFile continua na pasta e
 todo o processo pode ser repetido, no entanto todos os dados criados na maquina virtual s�o eliminados quando se faz "vagrant destroy"
-Se quiser remover definitivamente a m�quina virtual, fazer "vagrant box remove ubuntu/xenial64" (vagrant box remove nome_da_maquina)
