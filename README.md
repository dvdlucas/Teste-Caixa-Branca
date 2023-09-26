# teste
Pontos Observados Testes de Caixa Branca 
Não existe documentação descrevendo do que se trata esse código, apesar das variáveis e constantes na minha opinião estarem de acordo com o intuito para que o código foi feito,
e possuir uma certa legibilidade e organização pois alguém que entende de programação descobre o que o código faz tranquilamente. 
A arquitetura desse projeto me parece um sistema de autentificação simples sem qualquer tipo de segurança e extremamente vulnerável alem de não ter tratamentos de excessões adequadas.
Primeiro o projeto apresentou um erro indicando que a classe do driver usada nesse código não é a correta.
Identifiquei um erro na linha 15 do meu projeto que o catch responsavel por capturar uma possível excessão não possui nenhum retorno fechando as chaves, 
assim o código fica sem algum tipo de implementação caso o código quebre dentro do bloco Try.
Identifiquei na linha 24 a repetição de instanciação na string sql responsável por executar uma consulta no meu banco de dados que nesse cenário não seria necessário, 
a string sql deveria ser instanciada e preenchida com a instrução sql necessária apenas uma vez, sem a necessidade dessa repetição.
Outro ponto negativo no código que observei foi que a conexão com o banco de dados não é fechada após a consulta, o que é uma obrigação nesse tipo de conexão.
