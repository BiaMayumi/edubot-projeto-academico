# EduBot USCS

O **EduBot USCS** é uma plataforma acadêmica web criada para centralizar, organizar e facilitar o acesso dos estudantes da **Universidade Municipal de São Caetano do Sul** às principais informações institucionais.

A navegação acontece por cards de temas oficiais. O usuário escolhe um assunto, visualiza uma explicação objetiva no painel do assistente e acessa o link institucional correspondente.

## Visão Geral

- Interface moderna com tema escuro/claro.
- Layout responsivo para desktop, notebook, tablet e celular.
- Cards acadêmicos organizados por categoria.
- Mascote EduBot integrado ao cabeçalho e ao painel do assistente.
- Busca por temas e filtros por categoria.
- Links oficiais abrindo em nova aba.
- Aplicação estática, pronta para deploy no Netlify.

## Conteúdo

Os temas foram organizados a partir do documento **Links Edubot.docx**.

Temas disponíveis:

- Calendário acadêmico
- Provas e sistemas de avaliação
- Disciplina EAD
- Dependência (DP) e adaptações
- Acesso ao campus (MagicKey)
- Localização e campus
- Canais de atendimento institucional
- Corpo docente e contatos
- Estágio e empregabilidade
- Cursos disponíveis
- Secretaria e documentos
- Biblioteca
- Carteirinha de estudante
- Apoio ao aluno
- Sistemas e portal do aluno
- Transferência de turma

## Tecnologias

- React
- Vite
- TypeScript
- Framer Motion
- Lucide React
- CSS moderno

## Estrutura

```txt
edubot/
├── frontend/
│   ├── index.html
│   ├── package.json
│   ├── public/
│   │   ├── _redirects
│   │   ├── favicon.ico
│   │   ├── favicon.png
│   │   └── apple-touch-icon.png
│   └── src/
│       ├── App.tsx
│       ├── api.ts
│       ├── assets/
│       │   └── edu-robot.png
│       ├── components/
│       │   ├── AssistantPanel.tsx
│       │   ├── Dashboard.tsx
│       │   ├── Footer.tsx
│       │   ├── ThemeToggle.tsx
│       │   └── TopicCard.tsx
│       ├── data/
│       │   ├── topics.ts
│       │   └── types.ts
│       ├── main.tsx
│       └── styles/
│           └── global.css
├── netlify.toml
└── README.md
```

## Como Rodar Localmente

```bash
cd frontend
npm install
npm run dev
```

Acesse:

```txt
http://localhost:5173
```

## Scripts

```bash
npm run dev
```

Inicia o servidor local de desenvolvimento.

```bash
npm run check
```

Executa a checagem TypeScript.

```bash
npm run build
```

Gera a versão de produção em `frontend/dist`.

```bash
npm run preview
```

Visualiza localmente a versão de produção.

## Deploy

O projeto é estático e está configurado para deploy no Netlify via `netlify.toml`.

Configuração usada:

```txt
Build command:
cd frontend && npm ci && npm run build

Publish directory:
frontend/dist
```

O arquivo `frontend/public/_redirects` garante que o app não mostre erro 404 ao recarregar ou abrir uma rota diretamente.

## Observações Técnicas

- O projeto atual é frontend estático e não depende de backend em produção.
- Os dados dos cards ficam em `frontend/src/data/topics.ts`.
- A camada `frontend/src/api.ts` simula chamadas assíncronas usando os dados locais.
- O mascote fica em `frontend/src/assets/edu-robot.png`.
- Arquivos de build, dependências, logs e caches são ignorados pelo Git.

## Integrantes

- Larissa Carvalho Pavan
- Beatriz Mayumi Fernandez de Oliveira
- Thiago Alves Serra
- Guilherme Bezerra de Carvalho
- Samuel Freitas Ribeiro de Castro
- Luana Ayumi Goto
- Maria Clara Ferreira Esteves

## Projeto Acadêmico

Projeto desenvolvido por alunos do curso de Inteligência Artificial da Universidade Municipal de São Caetano do Sul para a disciplina **Plataformas Computacionais para IA**.
