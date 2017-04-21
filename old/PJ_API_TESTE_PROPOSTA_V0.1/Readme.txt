//API Teste v.0.1
//Disclaimer: experimental e nada definitivo apenas->demonstrar ponto de vista que funciona

//Notas: Base de dados longe de ser prefeita no entanto funciona aceita-se sugest�es
//	API martelada no entanto intuito->demonstrar ponto de vista e que funciona
//	Estado:
//	API Martelada: 80%
//	BD Martelada: 80%

//TODO LIST:

//BD:
//
//Deixa de fazer procedimentos
//Fazer consultas para obter as listagens de todos os dados
//Rever a base de dados, verificar relacionamentos e campos(verificar se os campos neces�rios est�o
//presentes ou est�o a mais ou em falta) verificar se falta alguma tabela ou propor melhorias.
//Verificar o tipo de dados dos campos da bd
//Falta definir as chaves forasteiras na bd
//Verificar a exist�ncia de consultas mais "optimizadas" para as opera��es neces�rias
//Ajudar a API com o mec�nismo de transac��es

//An�lise de requisitos:
//
//Definir o estados poss�veis do projeto e da application e do registo do utilizador
//exemplo state = 1; aceite 
//Verificar a necessidade de aprovar o registo de um professor
//Ajudar a BD a rever as tabelas

//API:
//
//Tratar da autentica��o (finalizar)
//C�digo ass�ncrono mal desenhado usar biblioteca async - waterfall, series, map, ...
//Registo de dados multiplos funcionam mal excepto contactos que funciona 
//provavel = codigo async mal desenhado
//Rever o c�digo fazer um handling de error bem feito
//Alterar o c�digo martelo para c�digo bem estruturado e definido
//Proteger os dados quanto poss�vel do lado da api evitar o envio de dados errados para a bd
//Verificar a necessidade de aprovar o registo de um professor(falta endpoint na api);
//Fazer a api foolproof
//Verificar porque as transac��es n�o funcionam e corrigir 
//Implementar o sistema de roles
//Colocar as fun��es num m�dulo � parte as mais usadas em v�rios controllers
//Arranjar um mec�nismo para retirar a base de dados do request e colocar num m�dulo � parte
//Verificar o release das liga��es � db algumas n�o s�o libertadas quando deviam

//Testes: 
//Criar estudante
//POST: http://127.0.0.1:8080/api/student
{
	"username":"xmanel",
	"password":"32r2rfwefn",
	"email": "aa33r3ae@ataa.com",
	"usernumber":"923299",
	"fullname":"Ma33nuel X",
	"courses": [		
		{"course":1, "enryear": "2019"}
	],
	"contacts": [
		{"type": "44444", "contact": "phone"},
		{"contact": "44534234","type": "phone"}
	],
	"interests":"Redes e Comunica��o de Dados",
	"visibility":"2"
}


//Criar professor
//POST: http://127.0.0.1:8080/api/teacher
{
	"username":"jaquin122",
	"password":"32r2rfwefn",
	"email": "atado@ata.com",
	"fullname":"Super X",
	"contacts": [
		{"type": "44444", "contact": "phone"},
		{"contact": "44534234","type": "phone"}
	],
	"link":"http://127.0.0.1",
	"du": 1,
	"areas": "�rea de Redes e Comunica��o de Dados    �rea de Gest�o de Internet e Correio Electr�nico    �rea de Aplica��es Gerais e Apoio a Utilizadores    �rea de Aplica��es Administrativas e Apoio a Utilizadores    �rea de Gest�o de Salas de Inform�tica",
	"visibility":"2"
}

//Criar projeto
//POST: http://127.0.0.1:8080/api/project
{
	"title":"Project X",
	"summary":"Secreto",
	"nofstudents": 5,
	"objectives":"Desenvolver o Super X projeto ultra secreto",
	"prereqs":"Conhecimento de espionagem industrial",
	"course": 1,
	"start":"2020-01-01",
	"end":"2030-01-01",
	"lecyear": "2020/2021",
	"mentors":"c1e267c2-b835-4295-8049-ea832f0ba3e3"
}

//Criar projeto com proponentes
//POST: http://127.0.0.1:8080/api/project
{
	"title":"Project Y",
	"summary":"Secreto",
	"nofstudents": 5,
	"objectives":"Desenvolver o Super X projeto ultra secreto",
	"prereqs":"Conhecimento de espionagem industrial",
	"course": 1,
	"start":"2020-01-01",
	"end":"2030-01-01",
	"lecyear": "2020/2021",
	"mentors":["c1e267c2-b835-4295-8049-ea832f0ba3e3","c1e267c2-b835-4295-8049-ea832f0ba3e4","c1e267c2-b835-4295-8049-ea832f0ba3e5"],
	"proponents":["1abfc60d-1e7c-459e-85ff-ba27c961745b","1abfc60d-1e7c-459e-85ff-ba27c961745c","1abfc60d-1e7c-459e-85ff-ba27c961745d"]
}

//Candidatar a projetos
//POST: http://127.0.0.1:8080/api/application
{
	"place":"Tomar",
	"course":2,
	"lecyear":"2020/2021",
	"group":[
		{"student":"1abfc60d-1e7c-459e-85ff-ba27c961745b","ects":"1","average":"14.0"}
	],
	"application":[
		{"project":"1a435d96-e13c-42b0-ac28-73a11c3105cd","preference":"1"}
	]
}