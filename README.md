# GraphQL Aplikasi Pertama

Cliente web para estudar a integração entre Vue.js e uma API GraphQL. A aplicação permite autenticar usuários e executar operações de consulta, criação, alteração e exclusão de usuários e perfis.

## Funcionalidades

- Registro e login de usuários
- Exibição do usuário autenticado e de seus perfis
- Consulta e listagem de usuários
- Criação, alteração e exclusão de usuários
- Consulta e listagem de perfis
- Criação, alteração e exclusão de perfis
- Exibição de erros retornados pela API GraphQL

## Tecnologias

- Vue.js 2
- Vuex
- Vuetify 1
- Apollo Client 2
- GraphQL
- Vue CLI 3

As versões exatas das dependências estão registradas em `package-lock.json`.

## Pré-requisitos

Antes de iniciar, instale:

- [Node.js](https://nodejs.org/)
- npm, distribuído com o Node.js
- Uma API GraphQL compatível em execução

Por padrão, o cliente tenta acessar a API em:

```text
http://localhost:4000/
```

O endereço está configurado em `src/plugins/graphql.js`.

## Instalação

Clone o repositório e instale as dependências:

```bash
git clone git@github.com:brdoliveira/graphql-aplikasi-pertama.git
cd graphql-aplikasi-pertama
npm install
```

## Execução

Inicie o servidor de desenvolvimento:

```bash
npm run serve
```

O terminal exibirá o endereço local da aplicação, normalmente `http://localhost:8080/`.

## Comandos disponíveis

```bash
# Executa o projeto em modo de desenvolvimento
npm run serve

# Gera a versão de produção na pasta dist
npm run build

# Analisa o código com ESLint
npm run lint
```

## Estrutura do projeto

```text
src/
├── componentes/
│   ├── autenticacao/  # Registro, login e usuário autenticado
│   ├── comum/         # Componentes reutilizáveis
│   ├── perfil/        # Operações de perfis
│   └── usuario/       # Operações de usuários
├── plugins/
│   ├── graphql.js     # Cliente Apollo e autenticação das requisições
│   └── vuetify.js     # Configuração visual
├── App.vue            # Componente principal
├── main.js            # Ponto de entrada
└── store.js           # Estado global e token de autenticação
```

## Autenticação

Após o login, o token recebido da API é armazenado no `localStorage` e enviado no cabeçalho das requisições seguintes:

```text
Authorization: Bearer <token>
```

Esse mecanismo é adequado para fins de estudo. Antes de usar o projeto em produção, revise o armazenamento do token, a persistência da sessão e as políticas de segurança da aplicação.

## Observações

- O backend GraphQL não faz parte deste repositório e precisa estar em execução separadamente.
- As operações disponíveis dependem do schema implementado pelo backend.
- O projeto utiliza versões legadas do Vue, Vuetify e Apollo Client; uma migração deve ser planejada antes de uso em produção.

## Licença

Este projeto foi criado para fins de estudo. Adicione uma licença ao repositório caso pretenda distribuí-lo ou reutilizá-lo publicamente.
