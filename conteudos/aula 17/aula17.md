# Aula 17: Conexão com API - Parte 2

## Objetivos da Aula

- Aprofundar o conhecimento sobre consumo de APIs REST em aplicações React.
- Aprender a utilizar a biblioteca Axios para realizar requisições HTTP de forma simplificada.

## Conteúdo Programático

### 1. Revisão sobre APIs REST

- **Importância das APIs REST:**
  - Facilitam a comunicação entre o frontend e o backend, permitindo o acesso a dados e funcionalidades de servidores.

### 2. Uso da Biblioteca Axios

- **Introdução ao Axios:**
  - Biblioteca JavaScript popular para fazer requisições HTTP, baseada em promessas.
- **Vantagens do Axios sobre a Fetch API:**
  - Sintaxe mais simples e direta.
  - Possibilidade de configurar automaticamente parâmetros de requisição, como headers e timeout.
- **Exemplo de Uso do Axios com a API ViaCEP:**
  - Buscar informações de um CEP e exibir em um componente React:
    ```javascript
    import React, { useEffect, useState } from 'react';
    import axios from 'axios';

    function CepInfo({ cep }) {
      const [endereco, setEndereco] = useState(null);

      useEffect(() => {
        if (cep.length === 8) {
          axios.get(`https://viacep.com.br/ws/${cep}/json/`)
            .then(response => {
              if (!response.data.erro) {
                setEndereco(response.data);
              } else {
                setEndereco(null);
              }
            })
            .catch(error => console.error(error));
        }
      }, [cep]);

      return (
        <div>
          {endereco ? (
            <div>
              <p>Logradouro: {endereco.logradouro}</p>
              <p>Bairro: {endereco.bairro}</p>
              <p>Cidade: {endereco.localidade}</p>
              <p>Estado: {endereco.uf}</p>
            </div>
          ) : (
            <p>CEP inválido ou não encontrado.</p>
          )}
        </div>
      );
    }

    function App() {
      return <CepInfo cep="01001000" />;
    }

    export default App;
    ```

## Atividades Práticas

- Refatorar o componente React criado na Aula 16 para utilizar a biblioteca Axios em vez da Fetch API.
- Explorar outras funcionalidades do Axios, como a configuração de interceptadores de requisição e resposta.

## Recursos Adicionais

- [Documentação oficial do Axios](https://axios-http.com/docs/intro)
- [Axios vs Fetch: Comparação e Exemplos](https://blog.logrocket.com/axios-vs-fetch-best-http-requests/)

## Avaliação

- Habilidade em utilizar a biblioteca Axios para simplificar requisições HTTP em uma aplicação React.
- Capacidade de integrar e consumir dados de APIs REST em componentes React de forma eficiente.
