# API de Games
Esta API foi confeccionada em estudo de API na linguagem Node js.
## Endpoints
### GET /games
Esse endpoint é responsável por retornar a listagens de todos os games cadastrados no banco de dados.
#### Parâmetros
Nehum
#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber a listagem de todos os games.
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durane o processo de autenticação de requisição. Motivos: Token inválido, token inspirado.
