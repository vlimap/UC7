# Aula 14: Roteamento em React

## Objetivos da Aula

- Compreender o conceito de roteamento em aplicações React.
- Aprender a utilizar a biblioteca React Router para gerenciar a navegação entre páginas.

## Conteúdo Programático

### 1. Introdução ao Roteamento em React

- **O que é Roteamento:**
  - Sistema que permite a navegação entre diferentes componentes em uma aplicação React, simulando a navegação entre páginas.
- **Por que usar React Router:**
  - Facilita a criação de rotas e a gestão do histórico de navegação.

### 2. Configuração do React Router

- **Instalação do React Router:**
  - `npm install react-router-dom`.
- **Configuração das Rotas:**
  - Uso do componente `BrowserRouter` para envolver a aplicação.
  - Definição das rotas com o componente `Route`.
  - Exemplo:
    ```javascript
    import { BrowserRouter as Router, Route } from 'react-router-dom';

    function App() {
      return (
        <Router>
          <Route path="/" exact component={HomePage} />
          <Route path="/about" component={AboutPage} />
        </Router>
      );
    }
    ```

### 3. Navegação entre Páginas

- **Uso do Componente `Link`:**
  - Criação de links para navegação entre as rotas definidas.
  - Exemplo:
    ```javascript
    import { Link } from 'react-router-dom';

    function NavigationBar() {
      return (
        <nav>
          <Link to="/">Home</Link>
          <Link to="/about">About</Link>
        </nav>
      );
    }
    ```

## Atividades Práticas

- Configurar o React Router em um projeto React.
- Criar um conjunto de rotas para navegar entre diferentes componentes/páginas.
- Implementar uma barra de navegação usando o componente `Link`.

## Recursos Adicionais

- [React Router - Documentação Oficial](https://reactrouter.com/web/guides/quick-start)
- [React Training - React Router Tutorial](https://reactrouter.com/web/example/basic)

## Avaliação

- Capacidade de configurar e utilizar o React Router para gerenciar rotas em uma aplicação React.
- Habilidade em criar links para navegação entre páginas utilizando o componente `Link`.
