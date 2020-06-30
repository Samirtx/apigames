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

Exemplo de resposta:
```
[
    {
        "id": 23,
        "title": "Call of duty MW",
        "year": 2019,
        "price": 60
    },
    {
        "id": 65,
        "title": "Sea of thieves",
        "year": 2018,
        "price": 40
    },
    {
        "id": 2,
        "title": "Minecraft",
        "year": 2012,
        "price": 20
    }
]
```
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durane o processo de autenticação de requisição. Motivos: Token inválido, token inspirado.

Exemplo de resposta:
```
{
    "err": "Token inválido!"
}
```

### GET /auth
Esse endpoint é responsável por fazer o processo de login.
#### Parâmetros
email: E-mail do usuário cadastrado no sistema.

password Senha do usuário cadastrado no sistema com aquele determinado email.

Exemplo:

```
{
    "email": "samir@teste.com",
    "password": "1234"
}
```
#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber o token JWT para conseguir acessar endpoints protegidos na API.

Exemplo de resposta:
```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJzYW1pckB0ZXN0ZS5jb20iLCJpYXQiOjE1OTM1MzUyODcsImV4cCI6MTU5MzcwODA4N30.w3pHe4gVBGveEA9hFH1NBy_yesGe90LgK_rHsNGy_2o"
}
```
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durane o processo de autenticação de requisição. Motivos: senha ou email incorretos.

Exemplo de resposta:
```
 res.json({token: "Credenciais inválidas!"})
```
