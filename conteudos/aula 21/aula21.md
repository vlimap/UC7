# Aula 21: Testes no Desenvolvimento Web

## Objetivos da Aula

- Compreender os conceitos fundamentais de testes no desenvolvimento web.
- Aprender a utilizar ferramentas de teste como Jest e React Testing Library para testar aplicações React.

## Conteúdo Programático

### 1. Conceitos de Testes

- **Importância dos Testes:**
  - Garantir a qualidade do software e evitar regressões.
- **Tipos de Testes:**
  - Testes unitários, testes de integração, testes de ponta a ponta (E2E).

### 2. Ferramentas de Testes

- **Jest:**
  - Framework de teste para JavaScript com foco em simplicidade.
  - Exemplo de teste unitário com Jest:
    ```javascript
    // sum.js
    function sum(a, b) {
      return a + b;
    }
    module.exports = sum;

    // sum.test.js
    const sum = require('./sum');

    test('adds 1 + 2 to equal 3', () => {
      expect(sum(1, 2)).toBe(3);
    });
    ```
- **React Testing Library:**
  - Conjunto de utilitários para testar componentes React de forma mais idiomática.
  - Exemplo de teste de componente com React Testing Library:
    ```javascript
    import { render, screen } from '@testing-library/react';
    import Button from './Button';

    test('renders a button with text "Click me"', () => {
      render(<Button />);
      const buttonElement = screen.getByText(/click me/i);
      expect(buttonElement).toBeInTheDocument();
    });
    ```

## Atividades Práticas

- Escrever testes unitários para funções JavaScript simples usando Jest.
- Criar testes para componentes React utilizando a React Testing Library.
- Executar testes e interpretar os resultados.

## Recursos Adicionais

- [Documentação oficial do Jest](https://jestjs.io/docs/getting-started)
- [React Testing Library - Documentação](https://testing-library.com/docs/react-testing-library/intro)

## Avaliação

- Habilidade em escrever e executar testes unitários para funções JavaScript.
- Capacidade de testar componentes React com a React Testing Library.
- Compreensão dos conceitos fundamentais de testes no desenvolvimento web.
