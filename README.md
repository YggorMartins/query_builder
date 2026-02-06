Query Builder - API de Cursos e Módulos
Este projeto é uma API REST desenvolvida para o gerenciamento de cursos e seus respectivos módulos. A aplicação utiliza o Knex.js como query builder para interagir com um banco de dados SQLite, permitindo a criação, leitura, atualização e exclusão de registros de forma eficiente.

🚀 Tecnologias Utilizadas
Node.js: Ambiente de execução.

TypeScript: Linguagem para tipagem estática e melhor manutenção.

Express: Framework web para criação das rotas e gerenciamento de requisições.

Knex.js: Query builder para construção de consultas SQL em JavaScript/TypeScript.

SQLite3: Banco de dados relacional leve.

tsx: Ferramenta para execução direta de TypeScript em ambiente de desenvolvimento.

📋 Funcionalidades
Cursos (/courses)
POST /courses: Cadastra um novo curso.

GET /courses: Lista todos os cursos cadastrados por ordem alfabética.

PUT /courses/:id: Atualiza o nome de um curso existente.

DELETE /courses/:id: Remove um curso pelo ID.

Módulos (/modules)
POST /modules: Cadastra um novo módulo vinculado a um curso.

GET /modules: Lista todos os módulos cadastrados.

GET /courses/:id/modules: Lista todos os módulos de um curso específico utilizando Joins.

🛠️ Como Executar o Projeto
Instale as dependências:

Bash
npm install
Execute as Migrations (para criar as tabelas):

Bash
npm run knex migrate:latest
Execute os Seeds (para popular o banco com dados iniciais):

Bash
npm run knex seed:run
Inicie o servidor em modo de desenvolvimento:

Bash
npm run dev
O servidor iniciará na porta 3333.

🗄️ Estrutura do Banco de Dados
O banco de dados possui as seguintes tabelas principais:

courses: id, name, created_at, updates_at.

course_modules: id, name, course_id (chave estrangeira).

Desenvolvido por Yggor Martins.
