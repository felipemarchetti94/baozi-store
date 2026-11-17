# API REST - Baozi Store

Trabalho de Desenvolvimento Web Back-End (Uninter).
Java 17 + Spring Boot 3 + Spring Data JPA + H2 (opcional: MySQL).

## Como rodar
1. Abra o projeto no IntelliJ / Eclipse / VS Code (importar como projeto Maven).
2. Execute a classe `BaoziStoreApplication` (ou `mvn spring-boot:run`).
3. A API sobe em `http://localhost:8080`.
4. Console do banco H2: `http://localhost:8080/h2-console` (JDBC URL: `jdbc:h2:mem:baozidb`, usuário `sa`, senha vazia).

## Endpoints (clientes, produtos e pedidos)
| Método | URL | Descrição |
|---|---|---|
| POST | /{entidade} | Criar |
| GET | /{entidade} | Listar todos |
| GET | /{entidade}/{id} | Consultar por ID |
| PUT | /{entidade}/{id} | Atualizar (opcional) |
| DELETE | /{entidade}/{id} | Apagar |

## Exemplos de JSON
Cliente: `{"nome": "Felipe5188420"}`
Produto: `{"nome": "Baozi de Carne", "preco": 8.50, "estoque": true}`
Pedido: `{"clienteId": 1, "produtoId": 1, "quantidade": 3}`

## Usar MySQL
Descomente a dependência do MySQL no `pom.xml` e o bloco MySQL no `application.properties` (comentando o bloco do H2).
