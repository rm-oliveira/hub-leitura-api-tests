# Hub de Leitura - API Tests

Este repositório contém testes automatizados de **API** desenvolvidos com **Cypress** para o sistema **Hub de Leitura**, com foco na validação de endpoints, contratos, respostas e regras de negócio.

O projeto foi desenvolvido durante o curso de Qualidade de Software da EBAC, aplicando boas práticas de automação de testes de API.

## Sistema Testado

Os testes deste projeto são executados sobre a **API do Hub de Leitura**, disponibilizada pela EBAC para fins educacionais.

Repositório da API (documentação e servidor):

https://github.com/EBAC-QE/hub-de-leitura-api

⚠️ Antes de rodar os testes, certifique-se de que a **API esteja rodando localmente** conforme as instruções do README oficial do repositório acima.

## Execução dos testes (UI)

### Pré-requisitos

- Node.js (versão LTS)
- npm
- Editor de código (Visual Studio Code recomendado)
- **API** do **Hub de Leitura** rodando localmente

### Instalação do projeto de testes

Clone este repositório e instale as dependências:
```bash
git clone https://github.com/rm-oliveira/hub-leitura-api-tests.git

cd hub-leitura-api-tests

npm install
````

### Executando os testes

Abrir o Cypress em modo interativo:
```bash
npx cypress open
```
Executar os testes em modo headless:
```bash
npx cypress run
````
### Estrutura dos testes

Os testes utilizam autenticação via token e comandos customizados do Cypress para criação, atualização e exclusão dinâmica de dados, garantindo maior reutilização e confiabilidade dos cenários.

Os testes de API estão organizados na pasta:
```bash
cypress/e2e
```

As validações são realizadas por meio de requisições HTTP como:

- GET
- POST
- PUT
- DELETE

Com foco na validação de:

- Status code
- Corpo da resposta
- Contratos da API
- Regras de negócio
- Mensagens de erro

### Configuração da aplicação

A URL da aplicação testada pode ser ajustada no arquivo cypress.config.js.

http://localhost:3000/api/

## Tecnologias utilizadas

- Cypress
- JavaScript
- Node.js
- Git & GitHub