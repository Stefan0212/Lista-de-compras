Projeto: Lista de Compras Full-Stack
Este projeto é uma aplicação web completa (CRUD) para gerenciar uma lista de compras, utilizando TypeScript, Node.js, Express e MongoDB no backend, e HTML com Tailwind CSS e JavaScript no frontend.

Estrutura do Projeto
/lista-de-compras-app
|
|--- /backend
|   |--- /src
|   |   |--- /controllers
|   |   |   |--- shopping.controller.ts
|   |   |--- /models
|   |   |   |--- shopping.model.ts
|   |   |--- /routes
|   |   |   |--- shopping.routes.ts
|   |   |--- server.ts
|   |--- package.json
|   |--- tsconfig.json
|
|--- /frontend
|   |--- index.html
|
|--- README.md

Como Executar o Projeto
Pré-requisitos
Node.js e npm instalados.

Uma instância do MongoDB em execução (localmente ou em um serviço como o MongoDB Atlas).

1. Configurar o Backend
Navegue até a pasta do backend:

cd backend

Instale as dependências:

npm install

Configure a Conexão com o MongoDB:

Abra o arquivo backend/src/server.ts.

Encontre a linha const MONGO_URI = 'mongodb://127.0.0.1:27017/shopping-list';.

Altere a string de conexão para a URI do seu banco de dados MongoDB, se for diferente. O nome do banco de dados (shopping-list) será criado automaticamente.

Inicie o servidor backend:

npm start

O servidor estará em execução em http://localhost:5000.

2. Executar o Frontend
Abra o arquivo frontend/index.html diretamente em seu navegador de preferência (como Chrome, Firefox, etc.).

A aplicação frontend se conectará automaticamente ao backend em http://localhost:5000 para buscar, adicionar, editar e excluir itens da sua lista de compras.
