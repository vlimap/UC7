# Aula 19: Autenticação e Autorização

## Objetivos da Aula

- Compreender os conceitos de autenticação e autorização em aplicações web.
- Aprender a implementar um sistema de login e proteger rotas em uma aplicação React integrada com SQL Server.

## Conteúdo Programático

### 1. Conceitos de Autenticação e Autorização

- **Autenticação:**
  - Processo de verificação da identidade de um usuário.
- **Autorização:**
  - Processo de determinar se um usuário autenticado tem permissão para acessar determinados recursos ou rotas.

### 2. Implementação de Login

- **Criação de um Formulário de Login:**
  - Desenvolvimento de um componente React para entrada de credenciais do usuário.
- **Envio de Credenciais para o Backend:**
  - Uso do Axios para enviar as credenciais para um endpoint de autenticação no backend.
- **Autenticação no Backend:**
  - Recebimento das credenciais no backend (Express.js) e validação das mesmas no banco de dados SQL Server.
  - Exemplo de autenticação no backend:
    ```javascript
    app.post('/api/login', async (req, res) => {
      const { username, password } = req.body;
      const user = await sql.query(`SELECT * FROM users WHERE username = '${username}' AND password = '${password}'`);
      if (user.recordset.length > 0) {
        // Credenciais válidas
        res.status(200).send({ message: 'Login bem-sucedido' });
      } else {
        // Credenciais inválidas
        res.status(401).send({ message: 'Usuário ou senha incorretos' });
      }
    });
    ```

### 3. Proteção de Rotas

- **Uso do React Router para Proteção de Rotas:**
  - Criação de um componente de rota privada que verifica se o usuário está autenticado antes de permitir acesso à rota.
- **Exemplo de Rota Privada:**
  - Implementação de um componente `PrivateRoute` para proteger rotas que requerem autenticação:
    ```javascript
    import React from 'react';
    import { Route, Redirect } from 'react-router-dom';

    const PrivateRoute = ({ component: Component, isAuthenticated, ...rest }) => (
      <Route {...rest} render={(props) => (
        isAuthenticated ? <Component {...props} /> : <Redirect to='/login' />
      )} />
    );
    ```

## Atividades Práticas

- Desenvolver um sistema de login que autentica usuários com base em credenciais armazenadas no SQL Server.
- Implementar proteção de rotas na aplicação React, restringindo o acesso a determinadas páginas a usuários autenticados.

## Recursos Adicionais

- [React Router - Proteção de Rotas](https://reactrouter.com/web/example/auth-workflow)
- [Autenticação no Express.js com SQL Server](https://www.npmjs.com/package/mssql#promises)

## Avaliação

- Habilidade em implementar um sistema de autenticação integrado com o SQL Server.
- Capacidade de proteger rotas em uma aplicação React, permitindo acesso apenas a usuários autenticados.
