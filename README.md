# Painel CRM

Mini CRM + painel financeiro para freelancer/agência. Site estático (um único `index.html`),
sem build e sem dependências. Os dados ficam no `localStorage` do navegador.

## Rodar localmente
1. Abra a pasta no VS Code.
2. Instale a extensão **Live Server** (Ritwick Dey).
3. Clique com o botão direito em `index.html` → **Open with Live Server**.
   (Também funciona dando dois cliques em `index.html`.)

## Publicar: GitHub + Vercel
1. Instale o Git (git-scm.com) e crie conta no GitHub e na Vercel.
2. No terminal do VS Code (Ctrl + '), dentro da pasta do projeto:
   git init
   git add .
   git commit -m "Primeira versão do CRM"
   git branch -M main
3. No GitHub: New repository → nome `painel-crm` → Create (não marque README).
4. Copie os 2 comandos que o GitHub mostra e rode:
   git remote add origin https://github.com/SEU-USUARIO/painel-crm.git
   git push -u origin main
5. Na Vercel: Add New → Project → Continue with GitHub → escolha `painel-crm`.
6. Framework Preset: **Other**. Deixe Build Command e Output Directory em branco. Clique **Deploy**.
7. A cada `git add . && git commit -m "..." && git push`, a Vercel publica de novo sozinha.

## Importante
- Os dados do `localStorage` são separados por endereço: o que você cadastrar no Live Server
  não aparece no site da Vercel. Para levar dados, use Configurações → Exportar backup e
  depois Importar backup no outro endereço.
- Trocar de navegador ou limpar dados do navegador apaga os dados. Faça backups.
- Para banco real, veja `schema.sql`, `BACKEND_SETUP.md` e `.env.example`.
