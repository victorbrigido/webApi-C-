# webApi-C#

# Sistema de Cadastro de Alunos

Este projeto é um sistema de cadastro de alunos desenvolvido utilizando ASP.NET Core. O objetivo é fornecer uma API RESTful simples para adicionar e listar alunos, demonstrando a utilização do Entity Framework Core com SQLite.

## Tecnologias Utilizadas

- **Back-end**: ASP.NET Core com Entity Framework Core
- **Banco de Dados**: SQLite
- **Ferramentas**: Postman para testar a API

## Funcionalidades

- Cadastro de alunos com os campos: Nome, Idade e Curso.
- Listagem de alunos cadastrados através de uma API RESTful.

## Estrutura do Projeto

- **/WebApi**: Projeto da API, incluindo controllers e a configuração do Entity Framework.
- **/Models**: Definições de modelos de dados (ex. Aluno).
- **/Controllers**: Lógica de controle da aplicação.

## Como Executar o Projeto

### Pré-requisitos

- [.NET SDK](https://dotnet.microsoft.com/download) instalado.
- SQLite instalado (opcional, dependendo do seu ambiente).

### Configurando a API

1. Navegue até a pasta do projeto da API:
   ```bash
   cd WebApi

2. Execute o comando para criar o banco de dados e aplicar as migracoes:
   ```bash
   dotnet ef database update

3. Inicie o servidor API:
   ```bash
   dotnet run


  A API estará disponível em: http://localhost:5000

Testando a API

Você pode usar o Postman para testar as rotas da API:

GET http://localhost:5000/api/alunos: Lista todos os alunos.

POST http://localhost:5000/api/alunos: Cria um novo aluno (corpo em JSON).


Exemplo de Corpo da Requisição POST

json
{
  "nome": "João Silva",
  "idade": 20,
  "curso": "Engenharia"
}
