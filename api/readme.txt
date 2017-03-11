Por favor leiam.

Segue uma base para a cria��o da API, em baixo poder�o encontrar a esturura das diretorias do projeto
Pe�o especial aten��o para que comentem tudo, comentarios em ingl�s s�o a descri��o do c�digo e 
	coment�rios em portugu�s s�o notas para que todos os envolvidos percebam o que est� feito, e falta 
	fazer. Todos os ficheiros .go t�m um cabe�alho "AGENDA", servir� para nos orientarmos, pe�o-vos que 
	sigam o padr�o. Cada um fica respons�vel de apagar os seus coment�rios, caso algu�m ache que um 
	coment�rio n�o faz sentido comunique ao envolvido mas N�O APAGUE sem o consentimento dele.

J� retirei os reposit�rios .git que se encontravam nas bibliotecas da pasta github.com para que baste descarregar ~
	a pasta "api" e correr o execut�vel main.exe, os dados que introduzi na struct para codificar em JSON 
	s�o meramente exemplificativos.

O Projeto encontra-se organizdo da seguinte forma:

	api
	|	readme.txt
	|	bin
	|	|	main.exe
	|	pkg
	|	|	windows_amd64 (compila��o de bibliotecas)
	|	src
	|	|	github.com
	|	|	|	gorilla	(biblioteca necessaria para roteamento)
	|	|	|	go-sql-driver (biblioteca necess�ria para liga��o � base de dados)
	|	|	main
	|	|	|	controller.go (conjunto de handlers associados a uma rota)
	|	|	|	dbconnection.go (fun��es de manipula��o de dados da base de dados)
	|	|	|	main.go (arranque do servi�o)
	|	|	|	model.go (estruturas representantes da das views, necess�rias para serializa��o JSON)
	|	|	|	router.go (defini��o das rotas)

Adotei uma organiza��o o mais aproximado com MVC para facilitar a compreens�o do c�digo, 
e separei em ficheiros para evitar conflitos de commits e assim podermos render melhor o trabalho.

Comandos necess�rios no prompt:
	> go env
	> set GOPATH={absolute_path}\api
	> set GOBIN={absolute_path}\api\bin
	> go install {absolute_path}\api\src\main
	> cd {absolute_path}\api\bin
	> main.exe

comandos necess�rios no git bash (opcional para importar bibliotecas):
	$ export GOPATH={absolute_path}\api
	$ export GOBIN={absolute_path}\api\bin
	$ go get {repository}

Penso que da forma que a diretoria foi organizada ser� de facil compreenss�o a todos e o c�digo 
procurei o mais simples possivel.
Coment�rios deixem em baixo ou no SLACK