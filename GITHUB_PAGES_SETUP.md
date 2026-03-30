# Guia de Configuração - GitHub Pages

## 📋 Resumo
Este guia mostra como publicar o site permanentemente no GitHub Pages de forma gratuita.

## ✅ Pré-requisitos
- Conta GitHub (gratuita em github.com)
- Arquivo `index.html` e outros arquivos do projeto

## 🚀 Passo a Passo

### Passo 1: Criar Repositório no GitHub

1. Acesse [github.com](https://github.com)
2. Clique em "Sign in" (se já tiver conta) ou "Sign up" (para criar)
3. Após fazer login, clique no ícone **+** no canto superior direito
4. Selecione **"New repository"**
5. Preencha os dados:
   - **Repository name:** `guia-secretaria-ppgcom`
   - **Description:** "Guia de Processos - Secretaria MP-PPGCOM"
   - **Public:** Selecione (para que o site seja acessível)
   - **Initialize with:** Deixe desmarcado
6. Clique em **"Create repository"**

### Passo 2: Fazer Upload dos Arquivos

#### Opção A: Upload Direto (Mais Fácil)

1. No repositório criado, clique em **"Add file"** → **"Upload files"**
2. Arraste os arquivos ou clique para selecionar:
   - `index.html`
   - `README.md`
   - `MANUTENCAO.md`
   - `.gitignore`
3. Clique em **"Commit changes"**

#### Opção B: Usar Git (Mais Profissional)

```bash
# Clone o repositório (substitua USER pelo seu usuário GitHub)
git clone https://github.com/USER/guia-secretaria-ppgcom.git
cd guia-secretaria-ppgcom

# Copie os arquivos do projeto para este diretório
# (cp index.html, README.md, etc.)

# Adicione e faça commit
git add .
git commit -m "Versão inicial do site"

# Envie para GitHub
git push origin master
```

### Passo 3: Ativar GitHub Pages

1. Acesse o repositório no GitHub
2. Clique em **"Settings"** (engrenagem no canto superior direito)
3. No menu lateral, clique em **"Pages"**
4. Na seção **"Source"**:
   - Selecione **"Deploy from a branch"**
   - Branch: **"master"** (ou "main")
   - Pasta: **"/ (root)"**
5. Clique em **"Save"**

### Passo 4: Aguardar Publicação

1. Aguarde 1-2 minutos
2. Você verá uma mensagem: "Your site is live at: https://username.github.io/guia-secretaria-ppgcom"
3. Acesse o link para verificar se o site está funcionando

## 🎯 Seu Site Permanente

**URL do Site:** `https://seu-usuario.github.io/guia-secretaria-ppgcom`

Exemplo: `https://andrepaludo.github.io/guia-secretaria-ppgcom`

## 📝 Atualizando o Site

### Método 1: Editor Online (Recomendado)

1. Acesse o repositório no GitHub
2. Clique no arquivo que quer editar (ex: `index.html`)
3. Clique no ícone de lápis (✏️)
4. Faça as alterações
5. Clique em **"Commit changes"**
6. O site será atualizado automaticamente em 1-2 minutos

### Método 2: Via Git (Linha de Comando)

```bash
cd guia-secretaria-ppgcom

# Faça as alterações nos arquivos

# Adicione e faça commit
git add .
git commit -m "Descrição da alteração"

# Envie para GitHub
git push origin master
```

## 🔍 Verificando o Status

1. Acesse o repositório
2. Clique em **"Actions"** (abas no topo)
3. Você verá o histórico de deployments
4. Um ✅ verde indica sucesso
5. Um ❌ vermelho indica erro

## 🆘 Troubleshooting

### O site não aparece após fazer upload
- Aguarde 2-3 minutos
- Verifique se GitHub Pages está ativado em Settings → Pages
- Limpe o cache do navegador (Ctrl+Shift+Delete)

### Alterações não aparecem no site
- Aguarde 1-2 minutos após fazer commit
- Verifique em "Actions" se o deployment foi bem-sucedido
- Acesse o site em modo privado/incógnito

### Erro 404 - Página não encontrada
- Verifique se o arquivo `index.html` existe no repositório
- Verifique se GitHub Pages está apontando para a branch correta

### Formulário não funciona
- O formulário usa `mailto:` que abre o cliente de email local
- Isso é normal e funciona em qualquer navegador

## 📚 Recursos Adicionais

- [Documentação GitHub Pages](https://docs.github.com/en/pages)
- [Guia Git Básico](https://git-scm.com/book/pt-BR/v2)
- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## ✨ Dicas Importantes

✅ **Sempre use descrições claras** nos commits
✅ **Teste localmente** antes de fazer push
✅ **Faça backup** dos arquivos importantes
✅ **Revise o conteúdo** antes de publicar
✅ **Mantenha o README.md atualizado** com informações do projeto

---

**Pronto!** Seu site está permanentemente hospedado no GitHub Pages! 🎉
