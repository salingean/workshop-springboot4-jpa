# Web Services with Spring Boot and JPA / Hibernate

Projeto desenvolvido utilizando Spring Boot para criação de uma API REST de gerenciamento de usuários, pedidos, produtos e categorias.

## Tecnologias utilizadas

- Java 21
- Spring Boot
- Spring Data JPA
- Hibernate
- Maven
- H2 Database
- REST API

## Objetivo do projeto

O projeto consiste em uma API REST que simula um sistema de e-commerce, contendo:

- Usuários
- Pedidos
- Produtos
- Categorias
- Pagamentos

Além disso, foram aplicados conceitos de:

- CRUD
- Relacionamentos JPA
- Tratamento de exceções
- Arquitetura em camadas
- Banco de dados em memória
- Serialização JSON

## Modelo de domínio

### Entidades principais

- User
- Order
- Product
- Category
- OrderItem
- Payment

## Relacionamentos

- Um usuário possui vários pedidos
- Um pedido possui vários produtos
- Produtos possuem categorias
- Pedido possui pagamento
- Relação many-to-many entre produtos e categorias

## Estrutura do projeto

```bash
src/main/java/com/salingean/course
├── config
├── entities
├── repositories
├── resources
├── services
└── services/exceptions
```

## Endpoints principais

### Users

| Método | Endpoint |
|---|---|
| GET | /users |
| GET | /users/{id} |
| POST | /users |
| PUT | /users/{id} |
| DELETE | /users/{id} |

### Products

| Método | Endpoint |
|---|---|
| GET | /products |
| GET | /products/{id} |

### Orders

| Método | Endpoint |
|---|---|
| GET | /orders |
| GET | /orders/{id} |

### Categories

| Método | Endpoint |
|---|---|
| GET | /categories |
| GET | /categories/{id} |

## Como executar o projeto

### Pré-requisitos

- Java 21+
- Maven

### Clonar repositório

```bash
git clone https://github.com/salingean/workshop-springboot4-jpa.git
```

### Entrar na pasta

```bash
cd workshop-springboot4-jpa
```

### Executar aplicação

```bash
./mvnw spring-boot:run
```

Ou execute diretamente pela IDE.

## Banco H2

O projeto utiliza banco de dados H2 em memória.

### Acessar console H2

```bash
http://localhost:8080/h2-console
```

### Configurações

```bash
JDBC URL: jdbc:h2:mem:testdb
User Name: sa
Password:
```

## Perfil de teste

O projeto utiliza o perfil:

```properties
spring.profiles.active=test
```

Os dados iniciais são carregados automaticamente pela classe:

```bash
TestConfig
```

## Exemplos de JSON

### User

```json
{
  "name": "Maria Brown",
  "email": "maria@gmail.com",
  "phone": "988888888",
  "password": "123456"
}
```

## Aprendizados

Durante o desenvolvimento deste projeto foram praticados:

- Spring Boot
- APIs REST
- JPA/Hibernate
- Relacionamentos entre entidades
- CRUD completo
- Tratamento de exceções
- Organização em camadas
- Persistência de dados

## Autor

Feito por Salin Gean
