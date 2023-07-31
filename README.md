# Controlador-Tarefas-API-REST
Este é um projeto de API para um sistema de tarefas desenvolvido em C# utilizando os frameworks .NET Core, Entity Framework e SQL Server.

### Tecnologias Utilizadas

- C#
- .NET Core
- ASP.NET Core
- Entity Framework Core
- Microsoft SQL Server

### Configuração

Antes de executar o projeto, certifique-se de ter instalado o SDK do .NET e um ambiente compatível com o ASP.NET Core. Para configurar o banco de dados, você deve fornecer as informações de conexão no arquivo `appsettings.json`.

### Como Acessar a API

A API pode ser acessada através dos seguintes endpoints:

#### Listar todos os usuários

`GET/api/Usuario`

#### Buscar usuário por ID

`GET/api/Usuario/{id}`

#### Cadastrar novo usuário

`POST/api/Usuario`

#### Atualizar usuário existente

`PUT/api/Usuario/{id}`

#### Excluir usuário

`DELETE/api/Usuario/{id}`

### Modelo de Dados

#### Tarefa

Representa uma tarefa no sistema.

| Campo      | Tipo            | Descrição              |
|------------|-----------------|------------------------|
| Id         | int             | Identificador único    |
| Nome       | string          | Nome da tarefa         |
| Descricao  | string          | Descrição da tarefa    |
| Status     | StatusTarefa    | Status da tarefa       |

#### Usuário

Representa um usuário no sistema.

| Campo      | Tipo            | Descrição              |
|------------|-----------------|------------------------|
| Id         | int             | Identificador único    |
| Nome       | string          | Nome do usuário        |
| Email      | string          | Endereço de e-mail     |

### Repositórios

Os dados dos usuários são armazenados em um banco de dados utilizando o Entity Framework Core. Os repositórios são responsáveis por lidar com as operações de leitura e escrita no banco de dados.

## Mapeamento das Entidades

O mapeamento das entidades para o banco de dados é realizado através das classes `UsuarioMap` e `TarefaMap`.

## Contexto do Banco de Dados

O contexto do banco de dados é definido na classe `SistemaDeTarefasDbContext` e contém as entidades `Usuarios` e `Tarefas`.

## Enumeração de Status de Tarefa

O status de uma tarefa é representado por uma enumeração `StatusTarefa`, que possui os seguintes valores:

- AFazer: A fazer
- EmAndamento: Em andamento
- Concluido: Concluído

## Executando o Projeto
Para executar o projeto, utilize o seguinte comando:

`dotnet run`
