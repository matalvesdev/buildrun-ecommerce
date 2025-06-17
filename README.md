# 🛒 Sistema de E-commerce

Bem-vindo ao repositório do meu **Sistema de E-commerce**!  
Este projeto foi desenvolvido como parte de uma aula prática com o objetivo de demonstrar como criar e gerenciar usuários, produtos, tags, pedidos e itens de pedidos utilizando tecnologias modernas do ecossistema Java.

---

## 🚀 Sobre o Projeto

Neste projeto, eu aprendi a:

- Configurar um projeto Spring Boot
- Integrar um banco de dados relacional
- Definir entidades JPA e seus relacionamentos
- Criar repositórios e serviços
- Expor APIs RESTful para operações CRUD e manipulação de relacionamentos

Ao final da implementação, fiquei apto a construir e gerenciar sistemas backend robustos com Spring Boot e Spring Data JPA.

---

## 🗂️ Estrutura das Entidades e Relacionamentos

### 📦 Entidades

- **Usuário**
  - Código do Usuário
  - Nome Completo

- **Endereço de Cobrança**
  - Rua
  - Número
  - Complemento
  - Usuário relacionado (one-to-one)

- **Pedido**
  - Número do Pedido
  - Valor Total
  - Data do Pedido
  - Usuário que fez o pedido (many-to-one)

- **Item do Pedido**
  - Pedido relacionado (many-to-one)
  - Produto relacionado (many-to-one)
  - Valor pago pelo usuário no item
  - Quantidade

- **Produto**
  - Código do Produto
  - Nome
  - Preço
  - Tags vinculadas (many-to-many)

- **Tag**
  - Código da Tag
  - Nome

### 🔗 Relações

- Usuário ↔️ Endereço de Cobrança: **1:1**
- Pedido → Usuário: **N:1**
- Pedido → Item do Pedido: **1:N**
- Item do Pedido → Pedido: **N:1**
- Item do Pedido → Produto: **N:1**
- Produto ↔️ Tag: **N:N**

---

## 🛠️ Tecnologias Utilizadas

- Java 17+
- Spring Boot
- Spring Data JPA
- Banco de dados relacional (ex: PostgreSQL, MySQL)
- Maven/Gradle

---

## 📚 O que eu aprendi

Ao concluir este projeto, consegui:

- Compreender como modelar entidades e relacionamentos no JPA
- Implementar operações CRUD em APIs RESTful
- Gerenciar relacionamentos complexos entre entidades
- Aplicar práticas modernas de desenvolvimento backend em Java

---

## 🚧 Como Executar

1. Clone o repositório:
    ```bash
    git clone https://github.com/seu-usuario/seu-repositorio.git
    ```
2. Acesse o diretório do projeto:
    ```bash
    cd seu-repositorio
    ```
3. Configure o banco de dados (application.properties)
4. Execute o projeto:
    ```bash
    ./mvnw spring-boot:run
    ```
    ou
    ```bash
    ./gradlew bootRun
    ```

---

## 📄 Licença

Este projeto está sob a licença MIT.

---

> Projeto desenvolvido para fins de aprendizado e estudo 🚀
