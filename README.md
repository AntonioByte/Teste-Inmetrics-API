# Teste-Inmetrics-API

## Descrição

Projeto de testes automatizados para API do Trello utilizando Cypress com Cucumber/Gherkin. O projeto inclui testes para consultar ações da API e validar respostas.

## Pré-requisitos

- Node.js **18.x** ou superior
- npm (gerenciador de pacotes do Node)
- Google Chrome ou outro navegador compatível

## Instalação do Projeto

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/AntonioByte/Teste-Inmetrics-API.git
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

## Estrutura dos Testes

- Os arquivos `.feature` (cenários Gherkin) estão em:
  - `cypress/features/`
- Os arquivos de step definitions (implementação dos passos) estão em:
  - `cypress/support/step_definitions/`
- Configurações do Cypress:
  - `cypress.config.js`

## Como Executar os Testes

### 1. Abrir o Cypress em modo interativo (GUI):
```bash
npm run cypress:open
```
- Escolha o projeto E2E e selecione o arquivo `.feature` desejado para rodar o teste.

### 2. Executar os testes em modo headless (terminal):
```bash
npm run cypress:run
```
- Os resultados aparecerão no terminal e, se configurado, serão gerados vídeos e screenshots.

## Testes Disponíveis

### Consulta de Ação no Trello
- **Arquivo:** `cypress/features/consultar-nome-lista.feature`
- **Descrição:** Teste que faz uma requisição GET para a API do Trello e valida:
  - Status code da resposta
  - Exibe o campo "name" da estrutura "list" no console

## Tecnologias Utilizadas

- **Cypress:** Framework de testes automatizados
- **@badeball/cypress-cucumber-preprocessor:** Plugin para suporte ao Gherkin/Cucumber
- **@bahmutov/cypress-esbuild-preprocessor:** Preprocessor para bundling
- **@cucumber/cucumber:** Framework BDD

## Observações

- Os testes utilizam o plugin **@badeball/cypress-cucumber-preprocessor** para suporte ao Gherkin/Cucumber.
- Certifique-se de que as dependências estejam instaladas corretamente antes de rodar os testes.
- Caso encontre problemas de cache, execute:
  ```bash
  npx cypress cache clear
  ```
- Os testes estão configurados para usar expressões regulares nos step definitions.
- O projeto suporta Gherkin em português com a configuração `# language: pt` nos arquivos `.feature`.

## Estrutura de Dependências

```json
{
  "devDependencies": {
    "@badeball/cypress-cucumber-preprocessor": "^22.1.0",
    "@bahmutov/cypress-esbuild-preprocessor": "^2.2.5",
    "@cucumber/cucumber": "^11.0.0",
    "@cypress/browserify-preprocessor": "^3.0.2",
    "cypress": "^14.4.1"
  }
}
```