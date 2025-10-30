# Dashboard Shadcn

Projeto de exemplo: um dashboard construído com React + TypeScript + Vite, com componentes no estilo shadcn/ui (sidebar, tabelas e gráficos). Este README descreve o projeto atual, como rodar localmente, gerar build e onde colocar o link do deploy.

## Descrição do projeto

Este repositório contém uma interface de dashboard com:

- Sidebar responsiva
- Área de gráficos interativos
- Tabela de dados com componentes reutilizáveis
- Páginas de login e cadastro (skeletons / exemplos)

O design dos componentes segue a convenção usada por shadcn/ui, mas os componentes estão na pasta `src/components` do projeto.

## Tecnologias

- React 19
- TypeScript
- Vite
- TailwindCSS
- react-router-dom (roteamento)

## Pré-requisitos

- Node.js v18+ (recomendado)
- npm (ou pnpm / yarn)

## Como rodar localmente

1. Instale dependências:

```bash
npm install
```

2. Inicie o servidor de desenvolvimento:

```bash
npm run dev
```

Observações:

- O Vite tenta rodar por padrão na porta 5173. Se essa porta estiver em uso, ele tentará outra (por exemplo 5174) — verifique a URL mostrada no terminal.
- Abra a URL exibida no terminal (ex: `http://localhost:5174/`).

## Build e Preview

Para gerar o build de produção:

```bash
npm run build
```

Para ver um preview do build gerado localmente:

```bash
npm run preview
```

## Estrutura importante do projeto

- `src/main.tsx` - ponto de entrada da aplicação (renderiza o componente `Page` principal)
- `src/App.tsx` - exemplo de roteamento com `react-router-dom`
- `src/pages/dashboard/Page.tsx` - componente principal do dashboard
- `src/components/` - componentes reutilizáveis (sidebar, chart, table, etc.)
- `src/pages/` - páginas (login, signup, dashboard)

O projeto usa o alias `@` (configurado no `vite.config.ts` e `tsconfig.json`) apontando para `./src`. Ex.: `import X from '@/components/x'`.

## Deploy

Coloque aqui o link do deploy público do seu projeto (Netlify, Vercel, Railway, Render, GitHub Pages, etc):

LINK_DO_DEPLOY_AQUI

Exemplo de notas de deploy:

- Para Vercel/Netlify, a build command é `npm run build` e o diretório de publicação é o gerado pelo Vite (padrão `dist`).

## Solução de problemas comuns

- Página em branco:

  - Abra o DevTools do navegador e verifique o console por erros de import/export ou runtime.
  - Confirme que o Vite está rodando e verifique a porta no terminal.
  - Problemas com imports usando `@`: confirme se `vite.config.ts` e `tsconfig.json` têm o alias configurado.

- Erros de tipagem no build:
  - Rode `npm run build` para ver mensagens completas e corrija conforme o TypeScript apontar.

## Como ajudar / Contribuir

- Abra uma issue descrevendo o problema ou a feature.
- Envie PRs com mudanças pequenas e documentação atualizada.

---

Se quiser, eu posso:

- Adicionar instruções específicas para deploy em Vercel/Netlify.
- Preencher automaticamente o campo `LINK_DO_DEPLOY_AQUI` com o link do seu deploy se você me passar o URL.
