Link de ajuda:
https://github.com/luong-komorebi/Markdown-Tutorial/blob/master/README_pt-BR.md
https://stackedit.io/app#

# Sistema de Cadastro e Busca de Usuários - API

Este projeto consiste em uma API para cadastro e busca de usuários utilizando uma linguagem de programação (por exemplo, Python) e um banco de dados (por exemplo, MySQL).

## Requisitos

- Linguagem de programação (ex: Python)
- Banco de dados (ex: MySQL)
- Framework de desenvolvimento de APIs (ex: Flask, Django)
- Bibliotecas Python para conexão com o banco de dados (ex: SQLAlchemy, psycopg2 para PostgreSQL, etc.)

## Instalação

1. Clone o repositório do projeto:

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```

2. Instale as dependências necessárias:
```bash
pip install -r requirements.txt
```
3. Execute o servidor da API:
```bash
python app.py
```

## Endpoints
### Adicionar Usuário

-   **URL:** `/api/adicionar_usuario`
-   **Método:** POST
-   **Payload JSON:**
   
    json code:
     ```bash
    `{
      "nome": "Nome do Usuário",
      "email": "usuario@example.com",
      "idade": 30
    }` 
    ```
-   **Resposta de Sucesso:** Código HTTP 201 (Created) e mensagem "Usuário adicionado com sucesso!".
-   **Resposta de Erro:** Código HTTP 400 (Bad Request) e mensagem de erro.

### Buscar Usuário por Email

-   **URL:** `/api/buscar_usuario`
-   **Método:** GET
-   **Parâmetros de Query:**
    -   `email`: Email do usuário a ser buscado.
-   **Resposta de Sucesso:** Código HTTP 200 (OK) e JSON com as informações do usuário.
    
    json code:
    ```bash
    {
      "nome": "Nome do Usuário",
      "email": "usuario@example.com",
      "idade": 30
    } 
    ```
-   **Resposta de Erro:** Código HTTP 404 (Not Found) e mensagem "Usuário não encontrado.".
## Exemplos de Uso

### Adicionar Usuário

code:
```bash
`curl -X POST http://localhost:5000/api/adicionar_usuario -H "Content-Type: application/json" -d '{"nome": "Novo Usuário", "email": "novo@example.com", "idade": 25}'` 
 ```
### Buscar Usuário por Email

code:
```bash
`curl -X GET http://localhost:5000/api/buscar_usuario?email=usuario@example.com`
 ```





