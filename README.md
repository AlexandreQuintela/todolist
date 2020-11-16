# Esse projeto foi realizado para conhecimento do Framework .Net core 5.0
Foi criada uma API Web com .Net Core que pode gerenciar "tarefas pendestes" armazenando em um banco de dados.

## Ferramentas
O projeto foi realizado utilizando o ASP .NET core 5.0 utilizando o editor VSCode.

### Pacotes  Nuget Utilizados:
```
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.InMemory
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design
dotnet add package Microsoft.EntityFrameworkCore.Design
dotnet tool install --global dotnet-aspnet-codegenerator
dotnet tool update -g Dotnet-aspnet-codegenerator
```


## Como compilar e Executar
* Para compilar o projeto utilize o comando no terminal:
```
dotnet build
```
* Para executar o projeto utilize o comando no terminal:
```
dotnet run
```
* Teste o TodoList com o Insomnia 

* Crie uma solicitação.
* Defina o método HTTP como POST.
* Defina o URI como https://localhost:5001/api/TodoItems.
* Selecione a guia Corpo.
* Selecione o botão de opção bruto.
* Defina o tipo como JSON (aplicativo/json).
* No corpo da solicitação, insira JSON para um item pendente:
```
{
  "name":"Projeto Todo",
  "isComplete":true
}
```
Selecione Enviar. 

### Visão geral da API
|API                        |Descrição                                 |Corpo da solicitação      |Corpo da resposta                   |
|---------------------------|------------------------------------------|--------------------------|------------------------------------|
|GET /api/TodoItems         |Obter todos os itens de tarefas pendentes |Nenhum                    |Matriz de itens de tarefas pendentes|
|GET /api/TodoItems/{id}    |Obter um item por ID                      |Nenhum                    |Item de tarefas pendentes           |
|POST /api/TodoItems        |Adicionar um novo item                    |Item de tarefas pendentes |Item de tarefas pendentes           |
|PUT /api/TodoItems/{id}    |Atualizar um item existente               |Item de tarefas pendentes |Nenhum                              |
|DELETE /api/TodoItems/{id} |Excluir um item                           |Nenhum                    |Nenhum                              |
