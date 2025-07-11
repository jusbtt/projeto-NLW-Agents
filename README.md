# NLW Agents

Este projeto foi desenvolvido durante o evento NLW da RocketSeat.

## Descrição

O **NLW Agents** é uma aplicação fullstack composta por um backend em Node.js (Fastify) e um frontend em React, utilizando TypeScript em ambos. O objetivo é gerenciar e exibir salas (rooms) cadastradas em um banco de dados PostgreSQL.

---

## Tecnologias e Bibliotecas Utilizadas

### Backend (`server/`)
- **Node.js** + **TypeScript**
- **Fastify**: Framework web para Node.js.
- **Zod**: Validação de esquemas e variáveis de ambiente.
- **drizzle-orm**: ORM para integração com PostgreSQL.
- **drizzle-seed**: Seed de dados para o banco.
- **postgres**: Cliente PostgreSQL.
- **@fastify/cors**: Suporte a CORS.
- **fastify-type-provider-zod**: Integração do Zod com Fastify.

### Frontend (`web/`)
- **React** + **TypeScript**
- **Vite**: Bundler e dev server.
- **@tanstack/react-query**: Gerenciamento de dados assíncronos.
- **React Router DOM**: Rotas SPA.
- **TailwindCSS**: Estilização utilitária.
- **clsx**, **tailwind-merge**, **class-variance-authority**: Utilitários para composição de classes CSS.
- **lucide-react**: Ícones SVG.

---

## Padrões de Projeto

- **Monorepo**: Estrutura separando `server` (backend) e `web` (frontend).
- **Type-safe**: Uso extensivo de TypeScript e validação com Zod.
- **Camadas**: Separação clara entre rotas, lógica de banco e validação.
- **Componentização**: Frontend baseado em componentes reutilizáveis.

---

## Setup do Projeto

### Pré-requisitos

- Node.js (v18+)
- PostgreSQL (pode ser via Docker)

### Configuração do Banco de Dados

1. Copie `.env.example` para `.env` em `server/` e ajuste as variáveis se necessário.
2. Suba o banco com Docker:
   ```sh
   cd server
   docker compose up -d