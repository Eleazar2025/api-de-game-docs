# API de Games
Esta API será utilizada para a aplicação de games

## EndPoints
### GET /games
#### Esta rota (endpoint) é responsavel por retornar todos os games registrados no banco de dados (bd).

##### Parâmetros recebidos por este endpoint: 
nenhum 

### Possíveis respostas deste endpoint:
#### OK 200
Caso esta resposta aconteça você receberá a listagem de todos os games
Exemplo de resposta:
```js
[
  {
    "id": 23,
    "title": "Call of the duty MW",
    "year": 2019,
    "price": 60
  },
    "id": 65,
    "title": "Sea of thieves",
    "year": 2018,
    "price": 40
  },
  {
    "id": 2,
    "title": "Minercraft",
    "year": 2019,
    "price": 60
  }
]
```
#### NOK 401
Falha na autenticação
caso ocorra esta resposta é sinal de que ocorreu alguma falaha durante o processo de autenticação da requisição. Falta de token ou token expirado.

Exemplo de resposta:
```
  "err": Token Inválido
```

# Comentando o processo de Login

### POST /auth
#### Esta rota (endpoint) é responsavel por retornar todos os games registrados no banco de dados (bd).

### Parâmetros recebidos por este endpoint: 
email : Email cadastrado no sistema

password: Senha do usuário cadastrado no sistema

### Possíveis respostas deste endpoint:
#### OK 200

```
  {
    "token":
    "fghjsfgfdgdfjgfhgldhfglhgjdfpgndflkgjd/fg/dflg/çdfjg/dfgljdf/gjd/sgj/çdjhçrykhtykjpukjpYUj~khSrkhrskhçkf/çhlsf/ç"
  }
```


#### 401
Caso esta resposta aconteça significa que alguma falha ocorreu durante o processo de autenticação da requisição. Motivos : Senha incorreta ou email incorreto.

#### NOK 401
Falha na autenticação
caso ocorra esta resposta é sinal de que ocorreu alguma falaha durante o processo de autenticação da requisição. Falta de token ou token expirado.

Exemplo de resposta:
```
  "err":Credenciais inválidas"
```


