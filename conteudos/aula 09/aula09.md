# Aula 09: Introdução ao React

## Objetivos da Aula

- Entender os conceitos básicos do React.
- Aprender sobre componentes, JSX e props no React.

## Conteúdo Programático

### 1. Conceitos Básicos do React

- **O que é React:**
  - Uma biblioteca JavaScript para construir interfaces de usuário.
  - Componentes como blocos de construção de interfaces.
- **Vantagens do React:**
  - Reutilização de componentes.
  - Virtual DOM para otimização do desempenho.
  - Ecossistema rico e comunidade ativa.

### 2. Componentes e JSX

- **Componentes:**
  - Definição de componente funcional e de classe.
  - Exemplo de um componente funcional:
    ```javascript
    function Welcome(props) {
      return <h1>Hello, {props.name}</h1>;
    }
    ```
  - Exemplo de um componente de classe:
    ```javascript
    class Welcome extends React.Component {
      render() {
        return <h1>Hello, {this.props.name}</h1>;
      }
    }
    ```
- **JSX:**
  - Sintaxe semelhante ao HTML para escrever elementos React.
  - Exemplo de JSX:
    ```javascript
    const element = <h1>Hello, world!</h1>;
    ```

### 3. Props

- **Introdução a Props:**
  - Props são propriedades passadas para componentes para configurá-los.
  - Exemplo de uso de props:
    ```javascript
    const welcomeElement = <Welcome name="Alice" />;
    ```

## Atividades Práticas

- Criar um novo projeto React usando Create React App.
- Desenvolver um componente simples que recebe props e exibe um texto.
- Praticar a escrita de JSX para criar elementos React.

## Recursos Adicionais

- [Documentação oficial do React](https://reactjs.org/docs/getting-started.html)
- [Tutorial oficial do React](https://reactjs.org/tutorial/tutorial.html)

## Avaliação

- Compreensão dos conceitos básicos do React, como componentes, JSX e props.
- Capacidade de criar e utilizar componentes React em um projeto.
