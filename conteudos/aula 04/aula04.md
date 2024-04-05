# Aula 08: Preparar o ambiente com TypeScript, React e SQL Server

## Objetivos da Aula

- Configurar o ambiente de desenvolvimento no Visual Studio Code para trabalhar com TypeScript, React e SQL Server.
- Criar um projeto React com suporte a TypeScript.
- Instalar a biblioteca necessária para conexão com o SQL Server.
- Entender a melhor forma de organizar os diretórios da aplicação.

## Conteúdo Programático

### 1. Configuração do Visual Studio Code

- **Instalação de Extensões Recomendadas:**
  - **ESLint:** Ferramenta de análise de código para identificar padrões problemáticos encontrados no código JavaScript/TypeScript.
  - **Prettier:** Extensão de formatação de código para manter um estilo de codificação consistente.
  - **TypeScript:** Suporte avançado para a linguagem TypeScript, incluindo funcionalidades de autocompletar e detecção de erros em tempo real.

### 2. Criação de um Projeto React com TypeScript

- Utilização do comando `npx create-react-app meu-app --template typescript` para criar um novo projeto React com suporte a TypeScript.
- Explicação da estrutura do projeto e dos arquivos gerados.

### 3. Instalação do mssql

- Execução do comando `npm i mssql` para instalar a biblioteca `mssql`, que permite a conexão e interação com bancos de dados SQL Server a partir de uma aplicação Node.js.

### 4. Organização dos Diretórios da Aplicação

- **Estrutura Sugerida:**
    ```
    meu-app/
    ├── src/
    │   ├── assets/         # Imagens, ícones e outros recursos estáticos
    │   ├── components/     # Componentes React reutilizáveis
    │   ├── pages/          # Componentes React que representam páginas
    │   ├── services/       # Serviços para comunicação com APIs
    │   ├── styles/         # Arquivos de estilos globais e de temas
    │   ├── utils/          # Funções utilitárias e helpers
    │   ├── App.tsx         # Componente principal do React
    │   └── index.tsx       # Ponto de entrada do aplicativo
    ├── public/
    ├── .eslintrc           # Configurações do ESLint
    ├── .prettierrc         # Configurações do Prettier
    ├── package.json
    └── tsconfig.json
    ```

## Atividades Práticas

- Configurar o Visual Studio Code com as extensões recomendadas.
- Criar um novo projeto React com TypeScript e explorar sua estrutura.
- Instalar a biblioteca `mssql` e preparar o ambiente para futuras conexões com o SQL Server.
- Organizar os diretórios do projeto conforme a estrutura sugerida.

## Recursos Adicionais

- [Documentação oficial do ESLint](https://eslint.org/docs/user-guide/getting-started)
- [Documentação oficial do Prettier](https://prettier.io/docs/en/index.html)
- [Documentação oficial do TypeScript](https://www.typescriptlang.org/docs/)
- [npm: mssql package](https://www.npmjs.com/package/mssql)

## Avaliação

- Verificação da correta configuração do ambiente de desenvolvimento.
- Capacidade de criar e entender a estrutura de um projeto React com TypeScript.
- Preparação adequada para futuras conexões com o SQL Server usando a biblioteca `mssql`.
- Organização eficiente dos diretórios da aplicação.
