# API - Cadastro de Usuários

API REST desenvolvida com Node.js, Express e Prisma ORM, conectada ao MongoDB Atlas.

## Tecnologias

- Node.js
- Express
- Prisma ORM
- MongoDB Atlas

## Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/API.git

# Entre na pasta
cd API

# Instale as dependências
npm install

# Configure o arquivo .env
cp .env.example .env
# Preencha a variável DATABASE_URL com a sua connection string do MongoDB Atlas
```

## Configuração

Crie um arquivo `.env` na raiz do projeto:

```env
DATABASE_URL="mongodb+srv://usuario:senha@cluster.mongodb.net/nomedobanco?retryWrites=true&w=majority"
```

## Rodando o projeto

```bash
node server.js
```

O servidor vai rodar em `http://localhost:3000`.

## Rotas

| Método | Rota | Descrição |
|--------|------|-----------|
| GET | /usuarios | Lista todos os usuários |
| GET | /usuarios?name=Maria | Filtra usuários por nome |
| GET | /usuarios?age=25 | Filtra usuários por idade |
| GET | /usuarios?email=maria@gmail.com | Filtra usuários por email |
| POST | /usuarios | Cria um novo usuário |
| PUT | /usuarios/:id | Atualiza um usuário |
| DELETE | /usuarios/:id | Deleta um usuário |

## Exemplo de body para POST/PUT

```json
{
  "name": "Maria",
  "email": "maria@gmail.com",
  "age": 25
}
```
