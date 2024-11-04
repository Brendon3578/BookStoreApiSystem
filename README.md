# 📚 BookStore API System

Este é um sistema de API para gerenciamento de uma livraria, desenvolvido em C# com ASP.NET Core e MongoDB.

## 💻 Descrição

A API permite gerenciar livros, autores e categorias, proporcionando endpoints para operações de CRUD (Create, Read, Update, Delete) e outras funcionalidades essenciais para o controle de uma livraria.

## Tecnologias Utilizadas

- **C#** e **.NET**
- **ASP.NET Core** para desenvolvimento da API
- **MongoDB** como banco de dados
- **Swagger** para documentação da API

## Configuração do Projeto

1. Clone o repositório:

   ```bash
   git clone https://github.com/Brendon3578/BookStoreApiSystem.git
   cd BookStoreApiSystem
   ```

2. Instale as dependências do projeto:

   ```bash
   dotnet restore
   ```

3. Configure as variáveis de ambiente para a string de conexão do MongoDB (veja [Variáveis de Ambiente](#variáveis-de-ambiente)).

4. Inicie a aplicação:

   ```bash
   dotnet run
   ```

5. Acesse a documentação da API no Swagger:

   ```
   http://localhost:5000/swagger
   ```

## Variáveis de Ambiente

Para a API acessar o MongoDB, é necessário configurar a string de conexão via variáveis de ambiente no arquivo `appsettings.json` na pasta do projeto.


```json
{
  "BookStoreDatabase": {
    "ConnectionString": "<string de conexão do mongodb>",
    "DatabaseName": "BookStore",
    "BooksCollectionName": "Books"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}

```

## Endpoints

A API fornece endpoints para gerenciar livros, autores e categorias. Exemplos:

- **GET /api/books**: Lista todos os livros
- **POST /api/books**: Adiciona um novo livro
- **PUT /api/books/{id}**: Atualiza as informações de um livro existente
- **DELETE /api/books/{id}**: Remove um livro

## Uso

Exemplo de uso com `curl` para adicionar um livro:

```bash
curl -X POST http://localhost:5000/api/books \
-H "Content-Type: application/json" \
-d '{
  "title": "Nome do Livro",
  "author": "Autor do Livro",
  "category": "Categoria do Livro",
  "price": 19.99
}'
```

---

<h3 align="center">
    Feito com ☕ por <a href="https://github.com/Brendon3578"> Brendon Gomes</a>
</h3>
