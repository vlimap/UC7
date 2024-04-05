# Aula 16: Conexão com API - Parte 1

## Objetivos da Aula

- Compreender o conceito de APIs REST e sua importância no desenvolvimento web.
- Aprender a utilizar a Fetch API para realizar requisições HTTP em aplicações React, utilizando a API ViaCEP como exemplo.

## Conteúdo Programático

### 1. Introdução às APIs REST

- **O que é uma API REST:**
  - Interface de Programação de Aplicações que segue os princípios da arquitetura REST (Representational State Transfer).
- **Componentes de uma API REST:**
  - Endpoints, métodos HTTP (GET, POST, PUT, DELETE), status codes.

### 2. Uso da Fetch API com a API ViaCEP

- **Realizando Requisições HTTP:**
  - Uso da Fetch API para fazer requisições GET à API ViaCEP.
  - Tratamento de respostas e erros.
- **Exemplo de Uso da Fetch API com a API ViaCEP:**
  - Buscar informações de um CEP e exibir em um componente React:
    ```javascript
    import React, { useEffect, useState } from 'react';

    function CepInfo({ cep }) {
      const [endereco, setEndereco] = useState(null);

      useEffect(() => {
        if (cep.length === 8) {
          fetch(`https://viacep.com.br/ws/${cep}/json/`)
            .then(response => response.json())
            .then(data => {
              if (!data.erro) {
                setEndereco(data);
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

- Criar um componente React que faz uma requisição GET para a API ViaCEP usando um CEP fornecido e exibe as informações do endereço recebidas.
- Implementar validação do formato do CEP antes de realizar a requisição e tratamento de erros.

## Recursos Adicionais

- [Documentação da API ViaCEP](https://viacep.com.br/)
- [MDN Web Docs - Usando Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)

## Avaliação

- Capacidade de utilizar a Fetch API para realizar requisições HTTP em uma aplicação React.
- Habilidade em consumir dados de uma API REST e exibi-los em componentes React.
