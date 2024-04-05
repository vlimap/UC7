# Aula 18: Integração React e SQL Server

## Objetivos da Aula

- Compreender como integrar uma aplicação frontend em React com um backend que utiliza o SQL Server.
- Aprender a enviar e receber dados entre o frontend e o backend.

## Conteúdo Programático

### 1. Visão Geral da Integração

- **Conceito de integração entre frontend e backend:**
  - Comunicação entre a interface de usuário (React) e o servidor (backend com SQL Server) para troca de dados e funcionalidades.
- **Arquitetura típica de uma aplicação web:**
  - Frontend fazendo requisições HTTP para o backend, que interage com o banco de dados SQL Server.

### 2. Configuração do Backend com SQL Server

- **Criação de uma API REST no backend:**
  - Uso de frameworks como Express.js para criar endpoints que o frontend pode acessar.
- **Conexão com o SQL Server:**
  - Utilização da biblioteca `mssql` para estabelecer conexão e executar consultas no banco de dados SQL Server.
  - Exemplo de configuração da conexão:
    ```javascript
    const sql = require('mssql');

    const config = {
      user: 'username',
      password: 'password',
      server: 'localhost',
      database: 'database_name',
      options: {
        encrypt: true // Use this if you're on Windows Azure
      }
    };

    sql.connect(config).then(pool => {
      // Query
      return pool.request()
        .query('SELECT * FROM mytable');
    }).then(result => {
      console.dir(result);
    }).catch(err => {
      // Error handling
    });
    ```

### 3. Conexão do Frontend com o Backend

- **Envio de Requisições HTTP:**
  - Uso da Fetch API ou Axios no frontend React para enviar requisições ao backend.
- **Exemplo de Envio e Recebimento de Dados:**
  - Frontend enviando dados de um formulário para o backend, que insere os dados no SQL Server:
    ```javascript
    // Frontend (React)
    function submitForm(data) {
      axios.post('http://backend-api-url/api/data', data)
        .then(response => console.log('Dados enviados com sucesso'))
        .catch(error => console.error('Erro ao enviar dados', error));
    }

    // Backend (Express.js)
    app.post('/api/data', async (req, res) => {
      try {
        const { nome, idade } = req.body;
        // Código para inserir os dados no SQL Server
        res.status(200).send('Dados inseridos com sucesso');
      } catch (error) {
        res.status(500).send('Erro ao inserir dados');
      }
    });
    ```

## Atividades Práticas

- Configurar um backend simples usando Express.js e conectar com o SQL Server.
- Criar um formulário no frontend React e implementar a lógica para enviar os dados do formulário para o backend.
- Implementar o recebimento e exibição de dados do SQL Server no frontend React.

## Recursos Adicionais

- [Express.js - Documentação Oficial](https://expressjs.com/)
- [mssql - Documentação](https://www.npmjs.com/package/mssql)
- [Axios - Documentação Oficial](https://axios-http.com/docs/intro)

## Avaliação

- Capacidade de configurar e integrar um backend em Express.js com o SQL Server.
- Habilidade em enviar e receber dados entre uma aplicação React e um backend SQL Server.
