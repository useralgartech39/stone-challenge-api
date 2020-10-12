# Stone DevOps | SRE Challenge
Paulo Vitor Costa Lima

# O desafio
⦁	A API foi desenvolvida utilizando a linguagem de propagação Python e sua aplicação se encontra no script denominado main.py, no repositório do Git compartilhado. 

⦁	Foi disponilizado um arquivo nomeado por Dockerfile, que se encontra no repositório do Git, para que possam subir a API localmente, conforme solicitado.

⦁	Foi criado um pipeline de integração contínua utilizando o GitHub Actions, onde pode ser visualizado pelo workflows contido no repositório do Git em destaque.

⦁	A aplicação foi implementada no Paas Heroku, onde pode ser acessada pela url: https://stone-challenge-api.herokuapp.com/ , de maneira que foi configurado também o deploy automático, assim que passar pela Integração Contínua implementada no GitHub actions, conforme falado no passo anterior.

# API - Dockerfile
⦁	Conforme solicitado foi incluido no diretório um Dockerfile para que a API possa ser implementada localmente. Segue os passos para execução:
	No diretório onde se encontra o Dockerfile executar o comando: 
	> docker build -t myimage .
	> docker run -d --name mycontainer -p 5000:5000 myimage 
	
⦁	A aplicação poderá ser testada localmente pelos seguintes caminhos:
1.	Rota Raiz - Método GET
http://localhost:5000/ 
2.	Rota para retornar todos os usuários cadastrados - Método GET
http://localhost:5000/usuarios 
3.	Rota para inserir um usuário - Método POST
http://localhost:5000/usuarios/inserir_usuario  
Exemplo de como inserir:
 {"nome":"Carlos","sobrenome":"da Silva","CPF":"023.543.555-87","email":"teste@hotmail.com","data":"15/11/2020"}
4.	Rota para buscar um usuário através de CPF - Método GET
http://localhost:5000/usuarios/{CPF_usuario} 
5.	FastAPI docs
http://localhost:5000/docs

# API - Heroku
⦁	Foi implementada uma API em python utilizando o FastAPI, onde armazenamos os dados de um usuário como: nome, sobrenome, CPF, email e data de nascimento. A aplicação foi hospedada na plataforma do Heroku, utilizando Integração Contínua com o GitHub Actions e o Deploy Automático configurado no próprio Heroku.

⦁	Para isso foram criadas três rotas, conforme solicitado. Segue as urls para cada rota:

1.	Rota Raiz - Método GET
https://stone-challenge-api.herokuapp.com/
2.	Rota para retornar todos os usuários cadastrados - Método GET
https://stone-challenge-api.herokuapp.com/usuarios
3.	Rota para inserir um usuário - Método POST
https://stone-challenge-api.herokuapp.com/usuarios/inserir_usuario
Exemplo de como inserir:
 {"nome":"Carlos","sobrenome":"da Silva","CPF":"023.543.555-87","email":"teste@hotmail.com","data":"15/11/2020"}
4.	Rota para buscar um usuário através de CPF - Método GET
https://stone-challenge-api.herokuapp.com/usuarios/{CPF_usuario}
5.	FastAPI docs
https://stone-challenge-api.herokuapp.com/docs



