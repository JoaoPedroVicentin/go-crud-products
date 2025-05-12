
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
http://localhost:PORT/swagger/index.html
```

> Substitua `PORT` pela porta que a aplicação está rodando.

---

## 🛠️ Tecnologias Utilizadas

- [Go (Golang)](https://golang.org/)
- [Chi](https://github.com/go-chi/chi) – Micro framework HTTP router
- [JWTAuth](https://github.com/go-chi/jwtauth) – Middleware para autenticação JWT
- [GORM](https://gorm.io/) – ORM para Go
- [SQLite](https://www.sqlite.org/) – Banco de dados leve utilizado com GORM
- [Viper](https://github.com/spf13/viper) – Gerenciador de configurações e variáveis de ambiente
- [UUID](https://github.com/google/uuid) – Geração de identificadores únicos
- [Testify](https://github.com/stretchr/testify) – Biblioteca de utilitários para testes
- [Swaggo](https://github.com/swaggo/swag) – Gerador de documentação Swagger para Go
- [HTTP-Swagger](https://github.com/swaggo/http-swagger) – Servidor Swagger UI para visualização da documentação

---

## 📁 Variáveis de Ambiente

As variáveis de ambiente devem ser configuradas no arquivo:

```
cmd/server/.env
```

### Exemplo de `.env`:

```env
# Tipo de driver do banco de dados (ex: sqlite, postgres, mysql)
DB_DRIVER=

# Endereço do host do banco de dados
DB_HOST=

# Porta do banco de dados
DB_PORT=

# Usuário para acessar o banco de dados
DB_USER=

# Senha do usuário do banco de dados
DB_PASSWORD=

# Nome do banco de dados
DB_NAME=

# Porta onde o servidor web da aplicação será iniciado
WEB_SERVER_PORT=

# Chave secreta para geração e verificação de tokens JWT
JWT_SECRET=

# Tempo de expiração do token JWT
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
cd cmd/server
swag init -g main.go
```

### 5. Inicie o servidor

```bash
cd cmd/server
go run main.go
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