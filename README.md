# Backend do Projeto SaborBr

Este repositório contém o backend do projeto **SaborBr**. Para rodar este backend localmente, siga as instruções abaixo.

## Dependências

Antes de rodar o projeto, instale as dependências necessárias:

### 1. Instalar Node.js e TypeScript

Certifique-se de ter o [Node.js](https://nodejs.org/) e o [TypeScript](https://www.typescriptlang.org/) instalados em seu computador.

## 2. Instalar o Prisma

Este projeto utiliza o Prisma como ORM para interagir com o banco de dados. Execute o seguinte comando para instalar as dependências do Prisma:

```bash
npm install @prisma/client
```
## Configuração do Banco de Dados

O projeto utiliza o MongoDB como banco de dados. Para configurar o banco de dados, siga as etapas abaixo:

### 3. Criar uma Conta no MongoDB Atlas

- Crie uma conta no [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
- Crie um novo cluster na sua conta.
- No painel do Atlas, vá para a seção **Database Access** e crie um usuário com permissões adequadas para o seu banco de dados.
- Em seguida, vá para a seção **Network Access** e adicione seu IP à lista de IPs permitidos.

### 4. Configurar a URL de Conexão do MongoDB

Após criar o cluster e o usuário no MongoDB Atlas, copie a URL de conexão fornecida na interface do MongoDB Atlas.

No arquivo .env do projeto, substitua a URL de conexão do MongoDB pela sua URL de conexão personalizada. A linha no arquivo .env deve se parecer com:

````env
DATABASE_URL="mongodb+srv://<USUARIO>:<SENHA>@cluster0.mongodb.net/<NOME_DO_BANCO>?retryWrites=true&w=majority"
`````

### 5. Rodar as Migrações (se necessário)

Se o projeto utilizar migrações para o banco de dados, execute o seguinte comando para rodar as migrações:

```bash

npx prisma migrate deploy
```

## 6. Rodando o Projeto

Para rodar o servidor localmente, use o comando:

```bash

npm run dev
```

## Vídeo de Referência

Caso precise de mais detalhes, você pode se guiar pelo vídeo de referência:

[Assista ao vídeo no YouTube](https://www.youtube.com/watch?v=XuTfN_84rcU&t=337s)
