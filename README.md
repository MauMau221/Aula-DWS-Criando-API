# 📘 API - Controle de Oficina

Esta API foi desenvolvida para gerenciar o fluxo de trabalho de uma oficina mecânica, incluindo **Ordens de Serviço, Clientes, Estoque, Agenda, Orçamentos, Financeiro e Garagem**.  
O objetivo é fornecer endpoints simples e padronizados para integração com sistemas web ou mobile.

---

## 🚀 Funcionalidades Principais
- **Ordens de Serviço (O.S)**
- **Estoque**
- **Clientes**
- **Agenda**
- **Orçamentos**
- **Financeiro**
- **Garagem (controle de veículos)**

---

## 📂 Recursos e Endpoints

### 🔧 Ordens de Serviço (O.S)
- `GET /os` → Lista todas as ordens de serviço  
- `GET /os/{id}` → Detalhes de uma ordem de serviço por ID  
- `POST /os` → Cria uma nova ordem de serviço  
- `PUT /os/{id}` → Atualiza uma ordem de serviço por ID  
- `DELETE /os/{id}` → Remove uma ordem de serviço por ID  

---

### 📦 Estoque
- `GET /estoque` → Lista todos os itens do estoque  
- `GET /estoque/{id}` → Detalhes de um item do estoque por ID  
- `POST /estoque` → Cria um novo item no estoque  
- `PUT /estoque/{id}` → Atualiza um item do estoque por ID  
- `DELETE /estoque/{id}` → Remove um item do estoque por ID  

---

### 👥 Clientes
- `GET /clientes` → Lista todos os clientes  
- `GET /clientes/{id}` → Detalhes de um cliente por ID  
- `POST /clientes` → Cria um novo cliente  
- `PUT /clientes/{id}` → Atualiza um cliente por ID  
- `DELETE /clientes/{id}` → Remove um cliente por ID  

---

### 📅 Agenda
- `GET /agenda` → Lista todos os agendamentos  
- `GET /agenda/{id}` → Detalhes de um agendamento por ID  
- `POST /agenda` → Cria um novo agendamento  
- `PUT /agenda/{id}` → Atualiza um agendamento por ID  
- `DELETE /agenda/{id}` → Remove um agendamento por ID  

---

### 💰 Orçamentos
- `GET /orcamentos` → Lista todos os orçamentos  
- `GET /orcamentos/{id}` → Detalhes de um orçamento por ID  
- `POST /orcamentos` → Cria um novo orçamento  
- `PUT /orcamentos/{id}` → Atualiza um orçamento por ID  
- `DELETE /orcamentos/{id}` → Remove um orçamento por ID  

---

### 💵 Financeiro
- `GET /financeiro` → Lista todos os lançamentos financeiros  
- `GET /financeiro/{id}` → Detalhes de um lançamento por ID  
- `POST /financeiro` → Cria um novo lançamento financeiro  
- `PUT /financeiro/{id}` → Atualiza um lançamento financeiro por ID  
- `DELETE /financeiro/{id}` → Remove um lançamento financeiro por ID  

---

### 🚗 Garagem
- `GET /garagem` → Lista todos os veículos na garagem  
- `GET /garagem/{id}` → Detalhes de um veículo por ID  
- `POST /garagem` → Registra um novo veículo na garagem  
- `PUT /garagem/{id}` → Atualiza informações de um veículo  
- `DELETE /garagem/{id}` → Remove um veículo da garagem  

---

## ✅ Regras e Validações
- Todos os campos obrigatórios devem ser validados no **backend**.  
- O **ID** deve ser único e numérico.  
- **CPF e CNPJ** devem ser únicos e validados.  
- **Datas** devem seguir o formato ISO 8601 (`YYYY-MM-DD`).  
- **Valores monetários** devem ser positivos.  

---

## 🔐 Autenticação
A API utiliza **JWT (JSON Web Token)** para autenticação.  

- O usuário deve realizar **login** para receber um token.  
- Esse token deve ser incluído no cabeçalho da requisição:  

```http
Authorization: Bearer {token}
