# MERN Blog

Este é um projeto de blog simples desenvolvido com a stack MERN (MongoDB, Express, React, Node.js). Ele permite que os usuários registrem, façam login, criem, atualizem e visualizem posts.

## Funcionalidades

- Registro de Usuário
- Login de Usuário
- Logout
- Criação de Posts
- Atualização de Posts
- Visualização de Posts
- Upload de Arquivos para os Posts

## Tecnologias Utilizadas

- MongoDB
- Express
- React
- Node.js
- JWT para autenticação
- Bcrypt para hash de senhas
- Multer para upload de arquivos

## Instalação

### Pré-requisitos

- Node.js
- MongoDB

### Passo a Passo

1. Clone o repositório:

    ```sh
    git clone https://github.com/username/mern-blog.git
    cd mern-blog
    ```

2. Instale as dependências no diretório raiz e no diretório `client`:

    ```sh
    npm install
    cd client
    npm install
    cd ..
    ```

3. Configure as variáveis de ambiente. Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

    ```env
    MONGO_URL=mongodb+srv://<username>:<password>@cluster0.mongodb.net/
    JWT_SECRET=your_jwt_secret
    ```

4. Inicie o servidor backend:

    ```sh
    cd api
    nodemon index.js
    ```

5. Inicie o cliente React:

    ```sh
    cd client
    npm start
    ```

6. Acesse o aplicativo em `http://localhost:3000`.

## Endpoints

### Autenticação

- `POST /register` - Registro de um novo usuário
- `POST /login` - Login de usuário
- `POST /logout` - Logout de usuário
- `GET /profile` - Obtém o perfil do usuário logado

### Posts

- `GET /post` - Obtém todos os posts
- `GET /post/:id` - Obtém um post específico por ID
- `POST /post` - Cria um novo post (com upload de arquivo)
- `PUT /post` - Atualiza um post existente (com upload de arquivo)

## Estrutura do Projeto
mern-blog/
├── client/ # Aplicação React
├── models/ # Modelos Mongoose
│ ├── User.js
│ └── Post.js
├── uploads/ # Diretório de uploads de arquivos
├── .gitignore
├── index.js # Servidor Express
├── package.json
├── README.md
└── .env # Arquivo de variáveis de ambiente


## Exemplos de Uso

### Registro de Usuário

```sh
curl -X POST http://localhost:4000/register -H "Content-Type: application/json" -d '{"username":"example","password":"password"}'
```

## Contribuição
Faça um fork do projeto
Crie uma branch para sua feature (git checkout -b feature/fooBar)
Commit suas mudanças (git commit -am 'Add some fooBar')
Push para a branch (git push origin feature/fooBar)
Crie um novo Pull Request
Licença
Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para mais detalhes.

## Contato
João Pedro Silva - joaopedrobueno2910@gmail.com
Link do projeto: https://github.com/jp-bueno/mern-blog
