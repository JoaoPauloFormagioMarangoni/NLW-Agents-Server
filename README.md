# NLW Agents

Projeto desenvolvido durante o evento **NLW (Next Level Week) - Agents** da Rocketseat.

## 📋 Sobre o Projeto

Sistema de gerenciamento de salas e perguntas com integração de IA para respostas automáticas.

## 🛠️ Tecnologias Utilizadas

### Backend
- **Node.js** - Runtime JavaScript
- **TypeScript** - Linguagem de programação
- **Fastify** - Framework web rápido e eficiente
- **Drizzle ORM** - ORM moderno para TypeScript
- **PostgreSQL** - Banco de dados relacional
- **Zod** - Validação de schemas

### Ferramentas de Desenvolvimento
- **Biome** - Linter e formatter
- **Docker** - Containerização
- **Drizzle Kit** - Ferramentas de migração

## 🏗️ Arquitetura

- **Arquitetura Modular**: Separação clara entre rotas, banco de dados e configurações
- **Type Safety**: Validação de tipos em tempo de compilação com TypeScript e Zod
- **ORM**: Drizzle ORM para mapeamento objeto-relacional
- **CORS**: Configurado para desenvolvimento frontend

## 🚀 Setup e Configuração

### Pré-requisitos
- Node.js 18+
- Docker e Docker Compose
- npm ou yarn

### Instalação

1. **Clone o repositório**
```bash
git clone <url-do-repositorio>
cd server
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure as variáveis de ambiente**
Crie um arquivo `.env` na raiz do projeto:
```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

4. **Inicie o banco de dados**
```bash
docker compose up -d
```

5. **Execute as migrações**
```bash
npm run db:migrate
```

6. **Popule o banco com dados iniciais (opcional)**
```bash
npm run db:seed
```

### Executando o Projeto

**Desenvolvimento:**
```bash
npm run dev
```

**Produção:**
```bash
npm start
```

O servidor estará disponível em `http://localhost:3333`

## 📊 Estrutura do Banco de Dados

- **rooms**: Salas de discussão
- **questions**: Perguntas e respostas por sala

## 🔧 Scripts Disponíveis

- `npm run dev` - Inicia o servidor em modo desenvolvimento
- `npm start` - Inicia o servidor em modo produção
- `npm run db:generate` - Gera migrações do banco
- `npm run db:migrate` - Executa migrações
- `npm run db:seed` - Popula o banco com dados iniciais

## 📝 API Endpoints

- `GET /health` - Health check
- `GET /rooms` - Lista todas as salas
- `POST /rooms` - Cria uma nova sala
- `GET /rooms/:id/questions` - Lista perguntas de uma sala
- `POST /rooms/:id/questions` - Cria uma pergunta em uma sala
