# Gerenciador de Tarefas - API REST com Spring Boot

Este repositório contém o backend de um sistema completo de gerenciamento de tarefas. A aplicação foi desenvolvida como uma API RESTful, utilizando **Java e Spring Boot**, para centralizar toda a lógica de negócio e a comunicação com o banco de dados.

---

### ✨ Arquitetura e Ecossistema do Projeto

A solução completa é modularizada em três projetos independentes que se comunicam através desta API, promovendo um baixo acoplamento entre as partes.

-   **Backend (Este Repositório):** O coração da aplicação. Uma API REST que gerencia as operações de Criar, Ler, Atualizar e Excluir (CRUD) tarefas. Para simplificar o ambiente de desenvolvimento, utiliza o banco de dados em memória **H2**.

-   **Frontend Web (Angular):** Uma interface web moderna e reativa que consome os dados desta API, proporcionando uma experiência de usuário fluida no navegador.
    -   **Repositório:** `https://github.com/DouglasCaron/lista-tarefas-web`

-   **Frontend Desktop (JavaFX):** Um cliente desktop robusto e nativo, também integrado a esta API, para gerenciamento de tarefas diretamente do seu computador.
    -   **Repositório:** `https://github.com/DouglasCaron/lista-tarefas-desktop`

### 🚀 Funcionalidades Principais

-   **Operações CRUD completas** para gerenciamento de tarefas.
-   **API RESTful bem definida** para fácil integração com diferentes clientes.
-   **Persistência de dados em memória (H2)**, ideal para desenvolvimento e testes rápidos.
-   **Arquitetura desacoplada** que permite o desenvolvimento e a implantação independentes do backend e dos frontends.

### 🛠️ Tecnologias Utilizadas

-   Java 21
-   Spring Boot 3
-   Spring Data JPA
-   Maven (Gerenciador de Dependências)
-   H2 Database (Banco de Dados em Memória)

### 🔧 Configuração e Execução

Para executar a API em seu ambiente local, siga os passos abaixo:

1.  **Pré-requisitos:** É necessário ter o **Java JDK 21** (ou superior) instalado e configurado em seu sistema.
2.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/DouglasCaron/lista-tarefas-api.git](https://github.com/DouglasCaron/lista-tarefas-api.git)
    ```
3.  **Abra o projeto** em sua IDE de preferência (IntelliJ IDEA, VS Code, Eclipse, etc.).
4.  **Execute a aplicação:** Inicie o servidor a partir da classe principal `ListaTarefasApiApplication.java`.
    -   *Dica para VS Code:* Com a extensão `Spring Boot Dashboard`, basta localizar `lista-tarefa-api` na aba da extensão e clicar em "start".
5.  **Verificação:** Após a inicialização, a API estará disponível e pronta para receber requisições em `http://localhost:8080`.

### 🔌 Endpoints da API

A tabela abaixo detalha os endpoints disponíveis para interagir com o recurso de tarefas.

| Método | URL                 | Descrição                                         |
| :----- | :------------------ | :------------------------------------------------ |
| `GET`  | `/api/tarefas`      | Retorna a lista completa de todas as tarefas.     |
| `POST` | `/api/tarefas`      | Cria uma nova tarefa com base nos dados enviados. |
| `PUT`  | `/api/tarefas/{id}` | Atualiza uma tarefa existente pelo seu `id`.      |
| `DELETE`| `/api/tarefas/{id}` | Remove uma tarefa do sistema pelo seu `id`.       |

---

*Este backend é a base para os clientes Web e Desktop. Sinta-se à vontade para explorá-los e ver a integração em ação!*
