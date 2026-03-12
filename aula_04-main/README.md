# Gerenciador de Tarefas (ToDo List)

Aplicação desenvolvida com **Spring Boot + Thymeleaf** para gerenciamento de tarefas com operações de CRUD, filtros por status e contagem automática de tarefas.

## Tecnologias Utilizadas

* Java 21
* Spring Boot 4.0.3
* Thymeleaf
* Maven
* Jakarta Bean Validation

## Funcionalidades

* Criar tarefas
* Editar tarefas
* Excluir tarefas
* Alternar status entre **Pendente** e **Concluída**
* Filtrar tarefas por status
* Contador automático de tarefas
* Validação de formulários
* Interface simples com Thymeleaf

## Como Executar o Projeto

### Pré-requisitos

Antes de executar o projeto é necessário ter instalado:

* **Java 21**
* **Maven**

Ou utilizar o **Maven Wrapper** que já vem no projeto.

### Executando a aplicação

No terminal, dentro da pasta do projeto:

#### Usando Maven Wrapper

```
./mvnw spring-boot:run
```

#### Ou usando Maven instalado

```
mvn spring-boot:run
```

### Acessar no navegador

Após iniciar, a aplicação estará disponível em:

```
http://localhost:8080/tarefas
```

## Endpoints / URLs

| URL                          | Método | Descrição                         |
| ---------------------------- | ------ | --------------------------------- |
| `/tarefas`                   | GET    | Lista todas as tarefas            |
| `/tarefas?filtro=pendentes`  | GET    | Lista apenas tarefas pendentes    |
| `/tarefas?filtro=concluidas` | GET    | Lista apenas tarefas concluídas   |
| `/tarefas/novo`              | GET    | Formulário para criar nova tarefa |
| `/tarefas/editar/{id}`       | GET    | Formulário para editar tarefa     |
| `/tarefas/salvar`            | POST   | Salvar tarefa                     |
| `/tarefas/excluir/{id}`      | POST   | Excluir tarefa                    |
| `/tarefas/status/{id}`       | GET    | Alternar status da tarefa         |

## Exemplo de Uso

Listar todas as tarefas:

```
http://localhost:8080/tarefas
```

Listar apenas tarefas pendentes:

```
http://localhost:8080/tarefas?filtro=pendentes
```

Listar apenas tarefas concluídas:

```
http://localhost:8080/tarefas?filtro=concluidas
```

## Estrutura do Projeto

```
com.biopark.tarefas
│
├── controller
│   └── TarefaController.java
│
├── service
│   └── TarefaService.java
│
├── repository
│   └── TarefaRepository.java
│
├── model
│   └── Tarefa.java
│
└── TarefasAppApplication.java
```

## Funcionalidades Implementadas

✔ CRUD completo de tarefas
✔ Filtro de tarefas por status
✔ Destaque visual do filtro ativo
✔ Contador de tarefas (total, pendentes e concluídas)
✔ 3 tarefas de exemplo pré-cadastradas

## Autor

**Daniel Henrique Todão**
