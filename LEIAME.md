# 📱 Despesas Recorrentes — Guia de Publicação

## O que está neste projeto

```
despesas-app/
├── index.html        ← o app completo
├── manifest.json     ← configuração PWA (nome, ícone, tela cheia)
├── sw.js             ← service worker (funciona offline)
└── icons/
    ├── icon-192.png  ← ícone do app
    └── icon-512.png  ← ícone do app (maior)
```

---

## Passo a passo: GitHub + Netlify

### 1. Criar repositório no GitHub

1. Acesse [github.com](https://github.com) e faça login
2. Clique em **"New repository"** (botão verde)
3. Nome sugerido: `despesas-app`
4. Deixe como **Public**
5. Clique em **"Create repository"**

### 2. Fazer upload dos arquivos

1. Na página do repositório criado, clique em **"uploading an existing file"**
2. Arraste **todos os arquivos e a pasta `icons`** para a área de upload
3. Clique em **"Commit changes"**

### 3. Publicar no Netlify

1. Acesse [netlify.com](https://netlify.com) e faça login
2. Clique em **"Add new site" → "Import an existing project"**
3. Escolha **GitHub** e autorize
4. Selecione o repositório `despesas-app`
5. Deixe todas as configurações padrão e clique em **"Deploy site"**
6. Em ~1 minuto o Netlify gera um link tipo: `https://meu-app-xyz.netlify.app`

> Opcional: em **Site settings → Domain management** você pode renomear para algo como `despesas-felipe.netlify.app`

---

## Instalar no iPhone (ícone na tela inicial)

1. Abra o **Safari** no iPhone (obrigatoriamente Safari, não Chrome)
2. Acesse o link do Netlify
3. Toque no botão **Compartilhar** (quadrado com seta para cima)
4. Role para baixo e toque em **"Adicionar à Tela de Início"**
5. Confirme o nome **"Despesas"** e toque em **"Adicionar"**
6. ✅ Pronto! O ícone aparece na tela inicial e abre em tela cheia

---

## Como os dados ficam salvos

- Os dados ficam salvos no **armazenamento local do iPhone** (localStorage)
- Não precisam de internet após o primeiro carregamento
- Ficam no dispositivo, não em nuvem
- Para não perder os dados, não limpe os dados do Safari

---

## Notificações

- Na primeira vez que abrir o app, toque no ícone 🔔
- Autorize as notificações
- O app vai alertar sobre despesas vencendo em até 3 dias

---

## Atualizações futuras

Se precisar atualizar o app, basta substituir o `index.html` no GitHub.
O Netlify re-publica automaticamente em ~1 minuto.
