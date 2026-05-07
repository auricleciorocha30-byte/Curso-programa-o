# CodeMaster Pro 🚀

Uma plataforma de aprendizado interativo para programação, com aulas teóricas, editor de código ao vivo e mentoria por IA.

## ✨ Funcionalidades

- 📚 Trilha de aprendizado estruturada em módulos
- 💻 Editor de código Monaco (mesmo do VS Code)
- 🔍 Preview de HTML em tempo real
- 🤖 Mentor IA integrado (powered by Supabase)
- 📊 Progresso salvo automaticamente no navegador
- 🔄 Refaça qualquer aula ou módulo a qualquer momento
- 🔐 Autenticação via Supabase

## 🛠️ Stack

- **Framework:** Next.js 16 (App Router)
- **Linguagem:** TypeScript
- **Editor:** Monaco Editor
- **Animações:** Framer Motion
- **Backend/Auth:** Supabase
- **Deploy:** Vercel

## 🚀 Como rodar localmente

### 1. Clone o repositório

```bash
git clone https://github.com/SEU_USUARIO/code-master-pro.git
cd code-master-pro
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure as variáveis de ambiente

Copie o arquivo de exemplo e preencha com suas credenciais do Supabase:

```bash
cp .env.local.example .env.local
```

Edite o `.env.local`:
```env
NEXT_PUBLIC_SUPABASE_URL=https://SEU_PROJETO.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=SUA_CHAVE_ANON
```

> Encontre essas chaves em: **Supabase Dashboard → Project Settings → API**

### 4. Inicie o servidor de desenvolvimento

```bash
npm run dev
```

Acesse [http://localhost:3000](http://localhost:3000)

## ☁️ Deploy no Vercel

1. Faça push do código para o GitHub
2. Acesse [vercel.com](https://vercel.com) e importe o repositório
3. Em **Settings → Environment Variables**, adicione:
   - `NEXT_PUBLIC_SUPABASE_URL`
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY`
4. Clique em **Deploy**

> ⚠️ **Nunca** faça commit do arquivo `.env.local` — ele já está no `.gitignore`.

## 📁 Estrutura do Projeto

```
src/
├── app/
│   ├── auth/          # Rotas de autenticação
│   ├── dashboard/     # Trilha de aprendizado
│   ├── lesson/[id]/   # Página de aula com editor
│   └── challenge/     # Área de desafios
├── components/
│   └── AIMentor.tsx   # Chat com mentor IA
├── data/
│   └── curriculum.ts  # Conteúdo das aulas e módulos
└── utils/
    ├── progress.ts    # Hook de progresso (localStorage)
    └── supabase/      # Clientes Supabase
```

## 📝 Licença

MIT
