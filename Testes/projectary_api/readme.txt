Por favor leiam.

Segue uma base para a cria��o da API, em baixo poder�o encontrar a esturura das diretorias do projeto.

O Projeto encontra-se organizdo da seguinte forma:

	projectary_api
			|	readme.txt
			|	bin
			|	|	main.exe (execut�vel do servi�o da API)
			|	pkg
			|	|	windows_amd64 (bibliotecas compiladas/direct�rio para compila��o de bibliotecas)
			|	src
			|	|	github.com
			|	|		subpastas cont�m bibliotecas necessarias
			|	|	golang.org
			|	|		subpastas cont�m bibliotecas necessarias
			|	|	gopkg.in				
			|	|	|  subpastas cont�m bibliotecas necessarias
			|	|	|	
			|	|	main
			|	|	|	model (pasta com estruturas representantes do modelo de dados, necess�rias para serializa��o JSON e opera��es BD)
			|	|	|	controllers (pasta com as fun��es associadas �s rotas)
			|	|	|	
			|	|	|	main.go (defini��o de rotas e c�digo do servi�o)
			|	|	|	

Comandos necess�rios no prompt (dica de @diogosantosmendes):
	> go env
	> set GOPATH={caminho_absoluto}\projectary_api
	> set GOBIN={caminho_absoluto}\projectary_api\bin
	> cd {caminho_absoluto}\projectary_api\src\main
	> go install
	> go run main.go ou cd ../../bin && main.exe

//Carece de confirma��o (dica de @diogosantosmendes)
comandos necess�rios no git bash (opcional para importar bibliotecas):
	$ export GOPATH={absolute_path}\projectary_api
	$ export GOBIN={absolute_path}\projectary_api\bin
	$ go get {repository}		
	
//Parte do readme proveniente da inspira��o de @diogosantosmendes	