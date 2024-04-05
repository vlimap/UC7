# Aula 12: Estilização em React - Parte 1

## Objetivos da Aula

- Aprender a utilizar CSS Modules e Styled Components para estilizar componentes React.
- Entender as vantagens de cada abordagem de estilização.

## Conteúdo Programático

### 1. CSS Modules

- **Introdução ao CSS Modules:**
  - Sistema que permite a importação de estilos CSS como módulos JavaScript.
  - Isolamento de estilos para evitar conflitos entre componentes.
- **Uso de CSS Modules:**
  - Criação de arquivos CSS específicos para cada componente.
  - Importação e aplicação de estilos nos componentes React.
  - Exemplo:
    ```javascript
    import React from 'react';
    import styles from './Button.module.css';

    function Button() {
      return <button className={styles.button}>Click me</button>;
    }
    ```

### 2. Styled Components

- **Introdução aos Styled Components:**
  - Biblioteca que permite escrever CSS diretamente dentro de componentes JavaScript.
  - Uso de template literals para definir estilos.
- **Uso de Styled Components:**
  - Criação de componentes estilizados com sintaxe semelhante ao CSS.
  - Exemplo:
    ```javascript
    import React from 'react';
    import styled from 'styled-components';

    const Button = styled.button`
      background-color: blue;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
    `;

    function App() {
      return <Button>Click me</Button>;
    }
    ```

## Atividades Práticas

- Criar componentes React e aplicar estilos usando CSS Modules.
- Utilizar Styled Components para estilizar componentes de forma dinâmica.

## Recursos Adicionais

- [Documentação oficial do CSS Modules](https://github.com/css-modules/css-modules)
- [Documentação oficial dos Styled Components](https://styled-components.com/docs)

## Avaliação

- Capacidade de aplicar estilos de forma modular e isolada usando CSS Modules.
- Habilidade em criar componentes estilizados dinamicamente com Styled Components.
