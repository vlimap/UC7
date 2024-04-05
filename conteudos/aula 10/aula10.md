# Aula 10: React Avançado - Parte 1

## Objetivos da Aula

- Entender o conceito de estado (state) em componentes React.
- Aprender sobre os métodos do ciclo de vida de componentes de classe.

## Conteúdo Programático

### 1. State em Componentes React

- **O que é State:**
  - State é um objeto que armazena informações sobre o componente que podem mudar ao longo do tempo.
- **Uso de State em Componentes de Classe:**
  - Inicialização do state no construtor.
  - Exemplo de componente com state:
    ```javascript
    class Counter extends React.Component {
      constructor(props) {
        super(props);
        this.state = { count: 0 };
      }

      render() {
        return (
          <div>
            <p>Count: {this.state.count}</p>
            <button onClick={() => this.setState({ count: this.state.count + 1 })}>
              Increment
            </button>
          </div>
        );
      }
    }
    ```

### 2. Métodos do Ciclo de Vida

- **Introdução aos Métodos do Ciclo de Vida:**
  - `componentDidMount`, `componentDidUpdate`, `componentWillUnmount` são alguns dos métodos do ciclo de vida de componentes de classe.
- **Exemplos de Uso:**
  - `componentDidMount`: Executar uma ação após o componente ser montado.
  - `componentDidUpdate`: Executar uma ação após a atualização do componente.
  - `componentWillUnmount`: Executar uma limpeza antes de o componente ser desmontado.

## Atividades Práticas

- Criar um componente de classe que utiliza state para gerenciar dados internos.
- Implementar métodos do ciclo de vida para adicionar comportamentos específicos durante a montagem, atualização e desmontagem do componente.

## Recursos Adicionais

- [Documentação oficial do React - State e Ciclo de Vida](https://reactjs.org/docs/state-and-lifecycle.html)
- [React Lifecycle Methods Diagram](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)

## Avaliação

- Compreensão do conceito de state e sua importância em componentes React.
- Habilidade em utilizar métodos do ciclo de vida para controlar o comportamento dos componentes.
