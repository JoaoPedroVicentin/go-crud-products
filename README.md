
# 🛒 CRUD de Produtos com Autenticação em Go

Este projeto é uma API REST desenvolvida em **Go (Golang)** que oferece um CRUD completo de produtos com autenticação de usuários utilizando **JWT**. A API também possui documentação integrada via **Swagger**.

---

## 🚀 Funcionalidades

- ✅ Cadastro e login de usuários
- ✅ Autenticação via JSON Web Token (JWT)
- ✅ Proteção de rotas: apenas usuários autenticados podem acessar o CRUD de produtos
- ✅ CRUD completo de produtos (Create, Read, Update, Delete)
- ✅ Documentação disponível via Swagger

---

## 📄 Documentação

A documentação Swagger está disponível em:

```
http://localhost:8080/swagger/index.html
```
---

## 🛠️ Tecnologias Utilizadas

- [Go (Golang)](https://golang.org/)
- [JWT](https://jwt.io/)
- [Swaggo](https://github.com/swaggo/swag) – Gerador de documentação Swagger para Go
- [Gin](https://github.com/gin-gonic/gin) – Framework web para Go (se estiver usando)

---

## 📁 Variáveis de Ambiente

As variáveis de ambiente devem ser configuradas no arquivo:

```
cmd/server/.env
```

### Exemplo de `.env`:

```env
DB_DRIVER=
DB_HOST=
DB_PORT=
DB_USER=
DB_PASSWORD=
DB_NAME=

WEB_SERVER_PORT=

JWT_SECRET=
JWT_EXPIRES_IN=
```

> Preencha com os dados corretos do seu banco de dados e das configurações do servidor e autenticação.

---

## 📦 Como rodar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/JoaoPedroVicentin/go-crud-products.git
cd go-crud-products
```

### 2. Instale as dependências

```bash
go mod download
```

### 3. Configure o `.env`

Crie o arquivo `.env` em `cmd/server/` conforme o exemplo acima.

### 4. Gere a documentação Swagger

```bash
go install github.com/swaggo/swag/cmd/swag@latest
swag init
```

### 5. Inicie o servidor

```bash
go run cmd/server/main.go
```

---

## 🔒 Rotas protegidas

As rotas de produtos são protegidas. Para acessá-las, você precisa:

1. Realizar o login
2. Copiar o token JWT retornado
3. Usar esse token no header `Authorization` das requisições protegidas:

```http
Authorization: Bearer SEU_TOKEN
```

---

<div align="center">
<h3>👨‍💻</h3>
    <h3> Criado por João Pedro Vicentin!</h3>
    <div>
        <h3>
            <a href="https://www.linkedin.com/in/joaopedrovicentin/" target="_blank">Linkedin</a>
            <a href='https://github.com/JoaoPedroVicentin' target='_blank'>Github</a>
            <a href="https://contate.me/joao-pedro-lopes-vicentin" target="_blank">Whatsapp</a>
        </h3>
    </div>
</div>