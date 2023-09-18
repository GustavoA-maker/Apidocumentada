# Documentação da API

* Escolher um local do computador para criar o projeto
* Abir o GitBash nesta pasta

Com o GitBash aberto executar o comando para criar a raiz do projeto: (mkdir: Make diretorio)
```
mkdir NOME_PROJETO
```
Acessar a pasta 
```
cd  NOME_PROJETO
```
Comando para abrir o Vscode 
```
Code . 
```
Cria o arquivo gerenciador de pacotes node
```
npm init -y
```
Criar arquivo .gitignore na raiz do projeto
```
touch .gitignore
```
Criar arquivo .env: arquvi para reservar variaveis do projeto
```
touch .env
```

## Instalar os pacotes do projeto

Instalar pacotes para o projeto
```
npm i express nodemon dotenv
```
* express: será o seridor da api
* nodemon: atualizar os arquivos alterados sem parar o servidor
* dotenv: gerenciador de varíaveis do ambiente

Criar pasta src 
```
mkdir src
```
Criar arquivo server.js na pasta src
```
touch src/server.js
```
Adicionar arquivos e pastas no .gitigore
```
Node_modules
.env
```
Adicionar a porta do servidor no arquivo .env
```
PORT = 3000
```
Configuração básica da API com express
```
// Importar o pacote express
const espress = require('express');

// Instanciar o express na variavel app
const app = express();

// Recuperar o pacote dotenv
const dotenv = require('dotenv').config();

// Importando variavel do arquivo .env
const PORT = process.env.PORT;

// Testando o servidor
app.listen(PORT, () => console.log(`Running at port ${PORT}!`));
```
Criar comando para rodar o servidor no arquivo package.json 
```
"start": "nodemon scr/server.js"
```
Rodar o servidor
```
npm start
```