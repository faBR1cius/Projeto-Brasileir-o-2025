# Projeto-Brasileir-o-2025
Projeto Final - Linguagens de Programação para Internet

# Projeto Brasileirão 2025 - Front-end e Back-end

Este repositório contém a implementação completa do sistema desenvolvido para a disciplina de Linguagem de Programação para Internet.  
O projeto é dividido em duas partes: a aplicação Front-end (React) e a API Back-end (Node.js + Express + MongoDB), formando um sistema integrado para gerenciamento dos clubes participantes do Campeonato Brasileiro 2025.

====================================================================
====================================================================

# 1. FRONT-END

O front-end foi desenvolvido utilizando React (Create React App) estruturado em componentes reutilizáveis, páginas, rotas, consumo de API com Axios e estilização com CSS Modules.

---

## 1.1 Tecnologias Utilizadas

- React (Create React App)
- JavaScript ES6+
- React Router DOM
- Axios
- CSS Modules
- HTML / CSS

---

## 1.2 Funcionalidades Implementadas

- Página inicial com listagem dos clubes cadastrados.
- Exibição dos detalhes de cada clube através de um modal.
- Carregamento de imagens internas e externas (URL).
- Formulário para cadastro de clubes.
- Redirecionamento automático após cadastro.
- Integração completa com a API do Back-end.
- Tratamento básico para falhas de imagem (placeholder).
- Responsividade básica.

---

## 1.3 Estrutura do Projeto (Front-end)

frontend/
│
├── public/
│ ├── imagens/
│ │ ├── flamengo.png
│ │ ├── corinthians.png
│ │ └── placeholder.png
│ └── index.html
│
├── src/
│ ├── components/
│ │ └── CartaoClube.jsx
│ │
│ ├── pages/
│ │ ├── Home.jsx
│ │ └── Cadastro.jsx
│ │
│ ├── services/
│ │ └── api.js
│ │
│ ├── styles/
│ │ ├── App.module.css
│ │ ├── Home.module.css
│ │ └── Cadastro.module.css
│ │
│ ├── App.jsx
│ └── index.js
│
└── package.json


---

## 1.4 Instalação e Execução (Front-end)

### Instalar dependências
cd frontend
npm install


### Executar em modo de desenvolvimento
npm start


A aplicação estará disponível em: http://localhost:3000


---

## 1.5 Scripts disponíveis

### `npm start`
Inicia o servidor de desenvolvimento.

### `npm run build`
Gera a versão de produção no diretório `build`.

### `npm test`
Executa testes configurados no CRA (não utilizados neste projeto).

---

## 1.6 Comunicação com a API

Todas as requisições são feitas através do arquivo: src/services/api.js


A API está configurada para rodar na porta: http://localhost:4000


Endpoints utilizados:

GET /clubes
GET /clubes/:id
POST /clubes
DELETE /clubes/:id


---

## 1.7 Padrão de Commits (sugestão)

- feat: implementação de novas funcionalidades  
- fix: correções  
- style: ajustes visuais ou de formatação  
- refactor: reorganização de código  
- docs: alterações no README  
- chore: manutenção geral  

====================================================================
====================================================================

# 2. BACK-END

O back-end foi desenvolvido utilizando Node.js, Express e Mongoose, fornecendo uma API REST que permite criar, listar, consultar e excluir clubes. O banco de dados utilizado é o MongoDB.

---

## 2.1 Tecnologias Utilizadas

- Node.js
- Express
- Mongoose (MongoDB)
- Nodemon
- Dotenv

---

## 2.2 Funcionalidades da API

- Cadastro de clubes
- Listagem geral
- Listagem individual por ID
- Exclusão de clubes
- Seed com clubes iniciais

---

## 2.3 Estrutura do Projeto (Back-end)

backend/
│
├── models/
│ └── Clube.js
│
├── routes/
│ └── clubes.js
│
├── scripts/
│ └── seedClubes.js
│
├── server.js
├── .env
└── package.json


---

## 2.4 Instalação e Execução (Back-end)

### Instalar dependências
cd backend
npm install


### Configurar o arquivo .env

Criar na pasta backend:

MONGO_URI=mongodb://localhost:27017/brasileirao2025
PORT=4000


### Executar o servidor
npm run dev


A API estará disponível em: http://localhost:4000


---

## 2.5 Endpoints da API

### Listar todos os clubes
GET /clubes


### Buscar por ID
GET /clubes/:id


### Cadastrar novo clube
POST /clubes
Body JSON:
{
"nome": "Exemplo",
"descricao": "Descrição do clube",
"imagemUrl": "/imagens/exemplo.png"
}


### Excluir clube
DELETE /clubes/:id


---

## 2.6 Exemplo de Respostas

### Exemplo de clube retornado
{
"_id": "65fbd90193ae32",
"nome": "Flamengo",
"descricao": "Clube de Regatas do Flamengo...",
"imagemUrl": "/imagens/flamengo.png"
}



---

## 2.7 Executando o Seed

Para inserir os clubes iniciais: node scripts/seedClubes.js


---

## 2.8 Organização dos Arquivos

- `server.js`  
  Inicializa o servidor e conecta ao MongoDB.

- `routes/clubes.js`  
  Define as rotas da API.

- `models/Clube.js`  
  Estrutura do documento no banco.

- `scripts/seedClubes.js`  
  Registra clubes iniciais no banco.

---

## 2.9 Padrão de Commits (sugestão)

- feat: rotas novas, melhorias na API  
- fix: correções no servidor ou banco  
- docs: documentação da API  
- refactor: reestruturação de arquivos  
- chore: scripts e manutenção geral  

====================================================================
====================================================================

# 3. Considerações Finais

Este projeto foi desenvolvido seguindo boas práticas de organização entre front-end e back-end, com separação clara de responsabilidades, documentação estruturada e integração completa entre as camadas da aplicação.  
O sistema cumpre os requisitos definidos em aula, incluindo consumo de API, rotas, componentes, CRUD parcial, CSS Modules, axios, estruturação modular e documentação detalhada.
