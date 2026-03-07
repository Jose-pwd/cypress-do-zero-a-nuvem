# Cypress, do Zero a Nuvem

Repositorio do curso **Cypress, do Zero a Nuvem**, da Escola Talking About Testing.

Este projeto foi organizado para ser simples de executar e servir como base de estudos de testes E2E com Cypress, incluindo execucao local, simulacao mobile e integracao com CI/Cypress Cloud.

## O que voce vai praticar

- Configuracao de projeto Cypress do zero
- Interacao com elementos comuns de aplicacoes web
- Upload de arquivos
- Validacoes de comportamento e conteudo
- Criacao de comandos customizados
- Testes de links que abririam em nova aba
- Simulacao de viewport mobile
- Execucao em pipeline de integracao continua
- Integracao com Cypress Cloud

## Pre-requisitos

- Node.js 18+ (recomendado LTS)
- npm 9+
- Git

## Instalacao

```bash
npm install
```

## Comandos principais

### Abrir Cypress (modo interativo)

```bash
npm run cy:open
```

### Abrir Cypress com viewport mobile (410x860)

```bash
npm run cy:open:mobile
```

### Rodar testes em modo headless

```bash
npm test
```

### Rodar testes em modo headless com viewport mobile (410x860)

```bash
npm run test:mobile
```

## Comandos uteis do dia a dia

### Rodar um spec especifico

```bash
npx cypress run --spec "cypress/e2e/CAC-TAT.cy.js"
```

### Rodar com browser especifico

```bash
npx cypress run --browser chrome
```

### Abrir um spec especifico na interface

```bash
npx cypress open --e2e --config specPattern=cypress/e2e/privacyPolicy.cy.js
```

## Estrutura principal

```text
cypress/
  e2e/         # specs de teste
  fixtures/    # massa de dados
  support/     # comandos customizados e configuracoes globais
src/           # aplicacao alvo usada nos exercicios
lessons/       # conteudo e roteiro do curso
cypress.config.js
```

## Configuracao atual de viewport (desktop)

No `cypress.config.js`, o projeto usa por padrao:

- `viewportWidth: 1280`
- `viewportHeight: 880`

## Roteiro do curso

- Estrutura do curso: [lessons/_course-structure_.md](./lessons/_course-structure_.md)
- Pre-requisitos detalhados: [lessons/_pre-requisites_.md](./lessons/_pre-requisites_.md)
- Sobre a aplicacao alvo: [lessons/_the-app_.md](./lessons/_the-app_.md)

## Observacoes

- Os comandos `cy:open:mobile` e `test:mobile` sobrescrevem somente viewport para simular dispositivo movel.
- Se quiser evoluir este repositorio para uso profissional, o proximo passo natural e separar suites por tags, adicionar relatorios e publicar resultados no CI.

---

Curso da **Escola Talking About Testing**.
