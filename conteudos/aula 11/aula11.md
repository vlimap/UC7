# Aula 11: React Avançado - Parte 2

## Objetivos da Aula

- Introduzir o conceito de Hooks em React.
- Aprender a utilizar os Hooks `useState` e `useEffect` para gerenciar estado e efeitos colaterais em componentes funcionais.

## Conteúdo Programático

### 1. Introdução aos Hooks

- **O que são Hooks:**
  - Hooks são funções que permitem a utilização de recursos de estado e ciclo de vida em componentes funcionais.
- **Vantagens dos Hooks:**
  - Simplificação da lógica de componentes.
  - Reutilização de lógica de estado entre componentes.

### 2. Hook `useState`

- **Uso do `useState`:**
  - Gerenciamento de estado em componentes funcionais.
  - Exemplo de uso do `useState`:
    ```javascript
    import React, { useState } from 'react';

    function Counter() {
      const [count, setCount] = useState(0);

      return (
        <div>
          <p>Count: {count}</p>
          <button onClick={() => setCount(count + 1)}>
            Increment
          </button>
        </div>
      );
    }
    ```

### 3. Hook `useEffect`

- **Uso do `useEffect`:**
  - Execução de efeitos colaterais em componentes funcionais.
  - Exemplos de uso do `useEffect`:
    - Executar um efeito ao montar o componente:
      ```javascript
      useEffect(() => {
        // Código a ser executado ao montar o componente
      }, []);
      ```
    - Executar um efeito ao atualizar uma variável de estado específica:
      ```javascript
      useEffect(() => {
        // Código a ser executado ao atualizar a variável de estado `count`
      }, [count]);
      ```

## Atividades Práticas

- Criar um componente funcional que utiliza o hook `useState` para gerenciar o estado.
- Implementar o uso do hook `useEffect` para adicionar comportamentos específicos relacionados a efeitos colaterais.

## Recursos Adicionais

- [Documentação oficial do React - Hooks](https://reactjs.org/docs/hooks-intro.html)
- [React Hooks: Guia Completo](https://blog.rocketseat.com.br/react-hooks/)

## Avaliação

- Compreensão dos conceitos e uso prático dos hooks `useState` e `useEffect`.
- Habilidade em gerenciar estado e efeitos colaterais em componentes funcionais React.
