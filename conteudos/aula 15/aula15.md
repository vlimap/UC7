# Aula 15: Gerenciamento de Estado

## Objetivos da Aula

- Compreender o conceito de gerenciamento de estado em aplicações React.
- Aprender a utilizar a Context API e Redux para gerenciar o estado de forma eficiente.

## Conteúdo Programático

### 1. Context API

- **Introdução à Context API:**
  - Mecanismo para compartilhar dados entre componentes sem a necessidade de passar props manualmente em cada nível.
- **Uso da Context API:**
  - Criação de um contexto com `React.createContext`.
  - Uso de `Provider` para passar o estado global.
  - Uso de `Consumer` ou `useContext` hook para acessar o estado.
  - Exemplo:
    ```javascript
    import React, { createContext, useContext, useState } from 'react';

    const ThemeContext = createContext();

    function ThemeProvider({ children }) {
      const [theme, setTheme] = useState('light');
      return (
        <ThemeContext.Provider value={{ theme, setTheme }}>
          {children}
        </ThemeContext.Provider>
      );
    }

    function App() {
      return (
        <ThemeProvider>
          <ChildComponent />
        </ThemeProvider>
      );
    }

    function ChildComponent() {
      const { theme, setTheme } = useContext(ThemeContext);
      return (
        <div>
          Current theme: {theme}
          <button onClick={() => setTheme('dark')}>Change to dark</button>
        </div>
      );
    }
    ```

### 2. Redux

- **Conceitos Básicos do Redux:**
  - Store, Actions, Reducers.
- **Uso do Redux em React:**
  - Configuração da store e uso do `Provider` para disponibilizar o estado.
  - Criação de actions e reducers para manipular o estado.
  - Uso do hook `useSelector` para acessar o estado e `useDispatch` para disparar actions.
  - Exemplo:
    ```javascript
    import { createStore } from 'redux';
    import { Provider, useSelector, useDispatch } from 'react-redux';

    // Reducer
    function counterReducer(state = { count: 0 }, action) {
      switch (action.type) {
        case 'INCREMENT':
          return { count: state.count + 1 };
        default:
          return state;
      }
    }

    // Store
    const store = createStore(counterReducer);

    function App() {
      return (
        <Provider store={store}>
          <Counter />
        </Provider>
      );
    }

    function Counter() {
      const count = useSelector(state => state.count);
      const dispatch = useDispatch();
      return (
        <div>
          Count: {count}
          <button onClick={() => dispatch({ type: 'INCREMENT' })}>Increment</button>
        </div>
      );
    }
    ```

## Atividades Práticas

- Implementar um tema de contexto simples usando a Context API e alternar entre temas claros e escuros.
- Criar uma pequena aplicação React que utiliza Redux para gerenciar o estado de um contador.

## Recursos Adicionais

- [Documentação oficial da Context API](https://reactjs.org/docs/context.html)
- [Documentação oficial do Redux](https://redux.js.org/introduction/getting-started)
- [React Redux - Documentação Oficial](https://react-redux.js.org/introduction/quick-start)

## Avaliação

- Habilidade em utilizar a Context API para gerenciar o estado global de uma aplicação React.
- Capacidade de configurar e utilizar Redux para gerenciar o estado em uma aplicação React de forma eficiente.
