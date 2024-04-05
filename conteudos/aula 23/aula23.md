# Aula 23: Deploy de Aplicações Web

## Objetivos da Aula

- Compreender os conceitos básicos de deploy de aplicações web.
- Aprender a utilizar o Azure para fazer o deploy da aplicação React com backend Express.js e banco de dados SQL Server.

## Conteúdo Programático

### 1. Conceitos de Deploy

- **O que é Deploy:**
  - Processo de disponibilizar uma aplicação na internet para que possa ser acessada por usuários.
- **Ambientes de Deploy:**
  - Desenvolvimento, teste, produção.

### 2. Deploy no Azure

- **Preparação da Aplicação:**
  - Garantir que a aplicação esteja funcionando corretamente em ambiente local.
  - Configurar variáveis de ambiente para produção, se necessário.

- **Deploy do Backend Express.js:**
  - Criação de um Web App no Azure.
  - Configuração do Web App para uso de Node.js.
  - Deploy do código do backend usando Git, GitHub Actions ou FTP.

- **Deploy do Frontend React:**
  - Build da aplicação React para produção (`npm run build`).
  - Deploy dos arquivos estáticos gerados no mesmo Web App do backend ou em um serviço de armazenamento como o Azure Blob Storage.

- **Configuração do Banco de Dados SQL Server:**
  - Criação de uma instância do SQL Server no Azure.
  - Configuração das credenciais de acesso e regras de firewall.
  - Conexão do backend Express.js ao banco de dados no Azure.

- **Testes Finais:**
  - Verificação do funcionamento da aplicação no ambiente de produção.
  - Testes de carga e performance, se necessário.

## Atividades Práticas

- Realizar o deploy de uma aplicação React com backend Express.js e banco de dados SQL Server no Azure.
- Acessar a aplicação pelo navegador e verificar seu funcionamento em ambiente de produção.

## Recursos Adicionais

- [Documentação oficial do Azure - Web Apps](https://docs.microsoft.com/en-us/azure/app-service/)
- [Documentação oficial do Azure - SQL Database](https://docs.microsoft.com/en-us/azure/azure-sql/)

## Avaliação

- Capacidade de realizar o deploy de uma aplicação web completa no Azure.
- Habilidade em configurar e gerenciar recursos no Azure para hospedagem de aplicações e bancos de dados.
