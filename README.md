# Sistema de Comunicação Kerry LATAM 2026/2027 — Mainframe TGT

Arquivo único e portátil (`index.html`). Senha de acesso: **TGTKER2026**.

## Subir no GIT
```bash
cd deploy
git init
git add .
git commit -m "Kerry LATAM comms system v3 — Mainframe TGT"
git branch -M main
git remote add origin <URL_DO_SEU_REPO>   # ex.: https://github.com/voce/kerry-latam.git
git push -u origin main
```

## Publicar na Vercel
**Opção A — CLI (mais rápido):**
```bash
npm i -g vercel
cd deploy
vercel deploy --prod
```
**Opção B — Git integration:** importe o repositório em vercel.com → deploy automático a cada push.

## Senha no servidor (recomendado)
A senha embutida (TGTKER2026) é client-side. Para proteção real:
Vercel → Project → Settings → **Deployment Protection → Password Protection**.

## Modo IA do Tradutor em produção
A função `api/translate.js` já está pronta. Na Vercel:
Settings → Environment Variables → `ANTHROPIC_API_KEY` = sua chave.
O front-end chama `/api/translate` automaticamente; sem a chave, ele usa o motor de regras (100% offline).
