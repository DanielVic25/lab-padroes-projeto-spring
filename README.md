# Projeto Prático: Design Patterns em Java e Spring Boot

Este projeto demonstra a implementação de Padrões de Projeto (Design Patterns) clássicos utilizando o ecossistema Spring Framework. A aplicação consiste em um sistema de gerenciamento de clientes com integração a serviços externos de consulta de CEP.

## 🚀 Tecnologias Utilizadas

* **Java 21**: Linguagem base do projeto.
* **Spring Boot 4.0.2**: Framework para construção da aplicação.
* **Spring Data JPA**: Abstração de repositórios e persistência de dados.
* **Spring Cloud OpenFeign**: Cliente HTTP declarativo para integração com a API do ViaCEP.
* **H2 Database**: Banco de dados em memória para desenvolvimento.
* **SpringDoc OpenAPI (Swagger)**: Documentação interativa da API.
* **Maven**: Automação de compilação e gerenciamento de dependências.

## 🏗️ Padrões de Projeto Implementados

O projeto utiliza as facilidades do Spring para aplicar padrões fundamentais:

* **Singleton**: Gerenciamento de Beans (Services e Repositories) como instâncias únicas pelo container do Spring.
* **Strategy**: Definição de algoritmos de negócio através da interface `ClienteService`, permitindo diferentes implementações.
* **Facade**: A classe `ClienteServiceImpl` abstrai a complexidade das interações entre o banco de dados e o serviço externo (ViaCEP), oferecendo uma interface simplificada ao controlador.

## 🛠️ Estrutura do Projeto

* **Controller**: `ClienteRestController` expõe os endpoints REST.
* **Model**: Entidades `Cliente` e `Endereco` e suas respectivas interfaces de repositório.
* **Service**: Lógica de negócio e cliente Feign para consumo de API externa.

## 🔌 Endpoints Principais

A API gerencia os clientes através dos seguintes endpoints:

* `GET /clientes`: Lista todos os clientes registrados.
* `GET /clientes/{id}`: Busca um cliente por ID.
* `POST /clientes`: Insere um novo cliente com busca automática de endereço via CEP.
* `PUT /clientes/{id}`: Atualiza os dados de um cliente existente.
* `DELETE /clientes/{id}`: Remove um cliente do sistema.

## ⚙️ Como Executar

1.  Certifique-se de possuir o **JDK 21** instalado.
2.  Clone este repositório em sua máquina.
3.  Execute a aplicação via Maven Wrapper:
    ```bash
    ./mvnw spring-boot:run
    ```
4.  Acesse a documentação Swagger para realizar testes manuais nos endpoints.

---

**Nota:** Projeto desenvolvido com foco prático na aplicação de padrões de arquitetura em ambiente Spring Boot.
