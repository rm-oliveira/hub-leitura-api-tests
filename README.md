# Hub de Leitura - API Tests

![CI Status](https://github.com/rm-oliveira/hub-leitura-api-tests/actions/workflows/api-tests.yml/badge.svg)

Este repositório contém testes automatizados de **API** desenvolvidos com **Cypress**, com foco na validação de endpoints, contratos, autenticação e regras de negócio da API do sistema **Hub de Leitura**.

O projeto foi desenvolvido durante o curso de **Qualidade de Software da EBAC**, aplicando boas práticas de automação e integração contínua.

## Sistema Testado

Os testes são executados sobre a **API do Hub de Leitura**, originalmente disponibilizada pela EBAC para fins educacionais.

Repositório da aplicação (fork utilizado neste projeto):

https://github.com/rm-oliveira/hub-de-leitura-api

Projeto original da EBAC:

https://github.com/EBAC-QE/hub-de-leitura-api

⚠️ Para execução local, certifique-se de que a API esteja rodando conforme as instruções do repositório da aplicação (porta 3000).

## Integração Contínua (CI)

Este projeto possui pipeline automatizada utilizando **GitHub Actions**, que:

- Clona o servidor da aplicação
- Instala as dependências
- Sobe o ambiente automaticamente
- Aguarda a disponibilidade da aplicação
- Executa os testes de API em modo headless

Os testes são executados automaticamente a cada push na branch `main`.

## Execução dos testes (Local)

### Pré-requisitos

- Node.js (versão LTS)
- npm
- API do Hub de Leitura rodando localmente

### Instalação 

```bash
git clone https://github.com/rm-oliveira/hub-leitura-api-tests.git

cd hub-leitura-api-tests

npm install
````

### Executando os testes

Modo interativo:
```bash
npx cypress open
```
Modo headless:
```bash
npm test
````

### Estrutura dos testes

Os testes utilizam:

- Autenticação via token

- Comandos customizados do Cypress

- Criação, atualização e exclusão dinâmica de dados

Essa abordagem garante:

- Independência de ambiente

- Maior confiabilidade dos cenários

- Execução estável em CI

Os testes estão organizados em:
```bash
cypress/e2e
```

As requisições HTTP cobertas incluem:

- GET
- POST
- PUT
- DELETE

Com validações de:

- Status code
- Corpo da resposta
- Estrutura/contrato
- Regras de negócio
- Mensagens de erro

### Configuração da aplicação

A URL base da aplicação pode ser ajustada no arquivo:
```bash
cypress.config.js
````

URL padrão utilizada:
```bash
http://localhost:3000/api/
```

## Tecnologias utilizadas

- Cypress
- JavaScript
- Node.js
- Git & GitHub
- GitHub Actions (CI)