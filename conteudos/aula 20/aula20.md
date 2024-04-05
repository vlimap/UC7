# Aula 20: Tratamento de Exceções

## Objetivos da Aula

- Compreender a importância do tratamento de exceções em aplicações React.
- Aprender a utilizar o try-catch e error boundaries para gerenciar erros.

## Conteúdo Programático

### 1. Try-Catch

- **Uso do Try-Catch:**
  - Estrutura para capturar e tratar erros em blocos de código específicos.
  - Exemplo de uso em uma função assíncrona:
    ```javascript
    async function fetchData() {
      try {
        const response = await axios.get('https://api.example.com/data');
        return response.data;
      } catch (error) {
        console.error('Erro ao buscar dados:', error);
      }
    }
    ```

### 2. Error Boundaries

- **Introdução aos Error Boundaries:**
  - Componentes React que capturam erros JavaScript em seus componentes filhos e os tratam, evitando que a aplicação inteira quebre.
- **Implementação de um Error Boundary:**
  - Exemplo de um componente Error Boundary:
    ```javascript
    class ErrorBoundary extends React.Component {
      constructor(props) {
        super(props);
        this.state = { hasError: false };
      }

      static getDerivedStateFromError(error) {
        return { hasError: true };
      }

      componentDidCatch(error, errorInfo) {
        // Log do erro
      }

      render() {
        if (this.state.hasError) {
          return <h1>Algo deu errado.</h1>;
        }
        return this.props.children;
      }
    }

    // Uso do Error Boundary
    <ErrorBoundary>
      <MyComponent />
    </ErrorBoundary>
    ```

### 3. Tratamento de Erros em APIs

- **Gestão de Erros em Requisições HTTP:**
  - Tratamento de erros comuns em chamadas de API, como erros de rede, timeouts e respostas de erro do servidor.
  - Exibição de mensagens de erro amigáveis para o usuário.

## Atividades Práticas

- Implementar o tratamento de exceções em funções que fazem chamadas de API usando try-catch.
- Criar e utilizar um componente Error Boundary para gerenciar erros em componentes React.
- Desenvolver uma estratégia de tratamento de erros para exibir feedback adequado aos usuários em caso de falhas nas requisições de API.

## Recursos Adicionais

- [Documentação oficial do React - Error Boundaries](https://reactjs.org/docs/error-boundaries.html)
- [MDN Web Docs - try...catch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch)

## Avaliação

- Habilidade em aplicar o tratamento de exceções em operações assíncronas e componentes React.
- Capacidade de implementar Error Boundaries para gerenciar erros de forma eficaz.
- Competência em tratar e exibir erros de forma amigável ao usuário em chamadas de API.
