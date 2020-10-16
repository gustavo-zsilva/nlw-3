# 3 Camadas de abstração de banco de dados

1- Driver Nativo ( sqlite3.query('SELECT * FROM users') )
2- Query Builder ( knex.js )
3- ORM ( Object Relational Mapping ) - Forma de relacionar objetos no JS à Queries no Banco de Dados

Ex:

Banco de Dados --> users
se relaciona com
JS --> Objeto/Classe User

E para cada user no banco de dados
cria-se um objeto/classe User no código JavaScript.

# Como criar a conexão com o banco de dados com Typeorm?

- Primeiro se cria um arquivo de configuração chamado "ormconfig.json" na raíz do projeto.

- As configurações mínimas para este arquivo consiste em especificar a chave "type" com o tipo de banco de dados (sqlite, postgres, mysql) e especificar a chave "database" com o caminho para o arquivo de banco de dados na aplicação.

- Para criar a conexão, crie um arquivo chamado JS ou TS. O de exemplo é "connection.ts", e ele faz a importação da função "createConnection" do módulo typeorm.

- Agora apenas faça uma chamada desta função dentro do arquivo.

# O que são Migrations?

São como um controle de versão do banco de dados;

# Como rodar typeorm com Typescript?

- Crie um novo comando em package.json, ex: "typeorm";
- Adicione o comando "ts-node-dev ./node_modules/typeorm/cli.js" como valor desta chave;
- Rode no terminal o comando "yarn typeorm" ou "npm typeorm", e se o começo dos comandos começar com "cli.js" agora o typeorm entende typescript.