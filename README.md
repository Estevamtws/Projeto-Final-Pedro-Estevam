# Projeto-Final-Pedro-Estevam
Projeto final da matéria de Desenvolvimento de Sistemas

---

# 🥖 Sistema de Gestão para Franquia de Padaria

## 📌 Visão Geral

Este projeto consiste no desenvolvimento de um sistema completo para **gestão de uma franquia de padaria**, com foco em controle operacional, vendas, estoque, clientes e relatórios.

A aplicação será construída seguindo boas práticas de engenharia de software, incluindo **arquitetura limpa, testes automatizados e documentação completa**.

---

## 🎯 Objetivos do Projeto

* Centralizar a gestão de múltiplas unidades da franquia
* Controlar vendas, produtos e estoque
* Gerenciar clientes e histórico de compras
* Fornecer APIs seguras para integração com frontend
* Garantir escalabilidade e manutenção facilitada

---

## 📊 1. BRD – Business Requirements Document

### 📌 Regras de Negócio

* Cada franquia pode possuir múltiplas unidades
* Produtos possuem categorias (pães, doces, bebidas, etc.)
* O estoque deve ser atualizado automaticamente após vendas
* Um cliente pode realizar múltiplas compras
* Funcionários possuem níveis de acesso (admin, operador)
* O sistema deve registrar histórico de vendas
* Cada unidade possui seu próprio controle de estoque

---

## 📑 2. SRS – Software Requirements Specification

### ✅ Requisitos Funcionais

* Cadastro de usuários (login/autenticação)
* CRUD de:

  * Produtos
  * Categorias
  * Clientes
  * Pedidos/Vendas
  * Funcionários
* Controle de estoque
* Registro de vendas
* Consulta de relatórios
* Autenticação segura (JWT)

---

### ⚙️ Requisitos Não Funcionais

* API RESTful
* Segurança com criptografia de senha
* Performance adequada para múltiplos usuários
* Código modular e escalável
* Uso de Docker para banco de dados
* Documentação via Swagger
* Testes automatizados

---

## 🗂️ 3. Planejamento e Cronograma

| Etapa | Descrição                        | Prazo  |
| ----- | -------------------------------- | ------ |
| 1     | Levantamento de requisitos       | 2 dias |
| 2     | Modelagem (diagramas)            | 3 dias |
| 3     | Setup do projeto (.NET + Docker) | 1 dia  |
| 4     | Desenvolvimento da API           | 7 dias |
| 5     | Implementação de autenticação    | 2 dias |
| 6     | Testes automatizados             | 2 dias |
| 7     | Documentação e ajustes finais    | 2 dias |

---

## 🧠 4. Diagramas

### 📌 Diagrama de Casos de Uso

* Login
* Gerenciar produtos
* Realizar venda
* Gerenciar estoque
* Consultar relatórios

### 📌 Diagrama de Classes

* User
* Product
* Category
* Order
* OrderItem
* Customer
* Employee

### 📌 Diagrama ER (Banco de Dados)

* Relacionamento entre:

  * Produtos ↔ Categorias
  * Pedidos ↔ Clientes
  * Pedidos ↔ Itens

### 📌 Diagrama de Sequência

* Fluxo de venda:

  * Login → Seleção de produtos → Finalização → Atualização de estoque

---

## 🔐 5. API de Autenticação

* Implementação com JWT
* Hash de senha com BCrypt
* Controle de acesso por roles

---

## 🔄 6. APIs CRUD

Entidades principais:

* Users
* Products
* Categories
* Orders
* Customers
* Employees

Operações:

* Create
* Read
* Update
* Delete

---

## 📘 7. Documentação (Swagger)

* Documentação completa das rotas
* Teste direto via navegador
* Descrição de parâmetros e respostas

---

## ⚙️ 8. Tecnologias Utilizadas

* **Backend:** C# com .NET
* **Banco de Dados:** SQL Server / PostgreSQL
* **ORM:** Entity Framework Core
* **Containerização:** Docker
* **Autenticação:** JWT
* **Testes:** xUnit / NUnit

---

## 🧪 9. Testes Automatizados

Exemplos:

* Teste de criação de produto
* Teste de autenticação
* Teste de venda
* Teste de atualização de estoque
* Teste de validação de dados

---

## 🧱 10. Arquitetura

Projeto estruturado seguindo **Clean Architecture**:

* **Domain** → Entidades e regras de negócio
* **Application** → Casos de uso
* **Infrastructure** → Banco de dados e serviços externos
* **API** → Controllers e endpoints

---

## 🧼 11. Clean Code

* Nomes descritivos
* Funções curtas
* Separação de responsabilidades
* Baixo acoplamento
* Alta coesão

---

## ❗ 12. Tratamento de Erros

* Middleware global de exceções
* Retorno padronizado de erros
* Logs estruturados

---

## 🚀 13. Como Executar o Projeto

```bash
# Clonar repositório
git clone <repo>

# Entrar na pasta
cd projeto-padaria

# Subir containers
docker-compose up -d

# Rodar aplicação
dotnet run
```

---

## 🔑 14. Acesso à API

* Swagger: `https://localhost:xxxx/swagger`
* Login: `/api/auth/login`

---

## 📌 15. Melhorias Futuras

* Integração com sistema de pagamento
* Dashboard com gráficos
* Multi-tenant (várias franquias isoladas)
* Integração com aplicativos mobile

---

## 👨‍💻 Autores

Pedro Henrique Rodrigues Costa
Pedro Henrique Almeida Estevam

---

## ⚠️ Análise crítica (importante)

Seu projeto está bem estruturado, mas alguns pontos podem elevar muito o nível:

**Pontos fortes:**

* Uso de Clean Architecture
* Uso de Docker
* Testes automatizados
* Separação clara de responsabilidades

**Riscos:**

* Complexidade excessiva para prazo curto
* Autenticação mal implementada pode comprometer tudo
* Falta de logs pode dificultar debugging

**Melhorias estratégicas:**

* Implementar logs (Serilog)
* Versionar API (`/v1/`)
* Adicionar validação com FluentValidation
* Usar DTOs para evitar exposição de entidades

