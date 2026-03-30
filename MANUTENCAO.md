# Guia de Manutenção - Guia de Processos MP-PPGCOM

## 📚 Índice
1. [Acesso ao Repositório](#acesso-ao-repositório)
2. [Editando o Conteúdo](#editando-o-conteúdo)
3. [Estrutura HTML](#estrutura-html)
4. [Adicionando Novas Seções](#adicionando-novas-seções)
5. [Troubleshooting](#troubleshooting)

---

## Acesso ao Repositório

### Passo 1: Criar Conta GitHub (Se não tiver)
1. Acesse [github.com](https://github.com)
2. Clique em "Sign up"
3. Preencha os dados solicitados
4. Confirme seu email

### Passo 2: Acessar o Repositório
1. Acesse o repositório do projeto
2. Você verá todos os arquivos do site

---

## Editando o Conteúdo

### Método 1: Editor Online do GitHub (Mais Fácil)

**Para editar o arquivo index.html:**

1. Clique no arquivo `index.html`
2. Clique no ícone de lápis (✏️) no canto superior direito
3. Faça as alterações desejadas
4. Role até o final da página
5. Na seção "Commit changes":
   - Adicione uma descrição breve (ex: "Atualizar informações de bolsas")
   - Clique em "Commit changes"
6. As mudanças serão publicadas automaticamente em 1-2 minutos

**Exemplo de alterações comuns:**

#### Atualizar um texto existente
```html
<!-- Antes -->
<p>Informação antiga aqui</p>

<!-- Depois -->
<p>Informação nova aqui</p>
```

#### Adicionar um novo item em uma lista
```html
<ul>
    <li>Item existente</li>
    <li>Novo item aqui</li>  <!-- Adicione esta linha -->
</ul>
```

#### Atualizar um email ou telefone
```html
<!-- Antes -->
<li><strong>Email:</strong> email@antigo.com</li>

<!-- Depois -->
<li><strong>Email:</strong> andre.paludo@pucrs.br</li>
```

---

## Estrutura HTML

### Seções Principais do Site

O arquivo `index.html` está organizado em seções:

```html
<header>              <!-- Cabeçalho com título -->
<nav>                 <!-- Menu de navegação -->
<div class="container">
    <section id="programa">      <!-- Informações do Programa -->
    <section id="alunos">        <!-- Processos de Alunos -->
    <section id="disciplinas">   <!-- Processos de Disciplinas -->
    <section id="bancas">        <!-- Processos de Bancas -->
    <section id="bolsas">        <!-- Processos de Bolsas -->
    <section id="outros">        <!-- Outros Processos -->
</div>
<footer>              <!-- Rodapé -->
```

### Classes CSS Úteis

| Classe | Uso |
|--------|-----|
| `process-detail` | Container para detalhes de um processo |
| `highlight` | Caixa de destaque (avisos importantes) |
| `category-card` | Card de categoria clicável |
| `btn` | Botão |
| `hidden` | Oculta um elemento |

---

## Adicionando Novas Seções

### Exemplo: Adicionar um novo processo

1. **Localize a seção apropriada** (ex: dentro de `<section id="alunos">`)

2. **Adicione um novo card:**
```html
<div class="category-card" onclick="toggleDetail('novo-processo')">
    <div class="category-header">Nome do Novo Processo</div>
    <div class="category-content">
        <p>Descrição breve do processo.</p>
        <button class="btn">Ver Detalhes</button>
    </div>
</div>
```

3. **Adicione os detalhes:**
```html
<div id="novo-processo" class="process-detail hidden">
    <h2>Nome do Novo Processo</h2>
    <p>Descrição completa aqui...</p>
    
    <h3>Procedimentos Detalhados:</h3>
    <ol>
        <li><strong>Passo 1:</strong> Descrição</li>
        <li><strong>Passo 2:</strong> Descrição</li>
    </ol>
    
    <div class="highlight">
        <strong>⚠️ Observações Importantes:</strong>
        <ul>
            <li>Observação 1</li>
            <li>Observação 2</li>
        </ul>
    </div>
</div>
```

4. **Adicione um link no menu** (opcional):
```html
<ul class="nav-menu" id="navMenu">
    <li><a href="#novo-processo">Novo Processo</a></li>
</ul>
```

---

## Formulário de Contato

O site inclui um formulário de contato que envia mensagens para: **andre.paludo@pucrs.br**

### Como funciona:
- Usuários preenchem o formulário
- A mensagem é enviada via Formspree
- Você recebe um email com a mensagem

### Para receber emails:
1. Acesse [formspree.io](https://formspree.io)
2. Crie uma conta
3. Configure seu email (andre.paludo@pucrs.br)
4. Copie o código fornecido
5. Atualize o `action` do formulário no HTML

---

## Troubleshooting

### O site não atualiza após fazer commit
**Solução:**
- Aguarde 1-2 minutos
- Limpe o cache do navegador (Ctrl+Shift+Delete)
- Acesse o site em modo privado/incógnito

### Alterações não aparecem no site
**Solução:**
- Verifique se fez "Commit changes"
- Verifique se o arquivo está em `index.html` (não em uma cópia)
- Verifique a aba "Actions" no GitHub para erros de build

### Formulário de contato não funciona
**Solução:**
- Verifique se o email está correto
- Teste o formulário com um email de teste
- Verifique a pasta de spam

### Layout quebrado após editar
**Solução:**
- Verifique se fechou todas as tags HTML corretamente
- Use a ferramenta "Inspect" do navegador (F12) para ver erros
- Compare com o código original

---

## Dicas de Boas Práticas

✅ **Sempre faça backup** - Copie o arquivo antes de grandes alterações
✅ **Use descrições claras** - Ao fazer commit, descreva o que mudou
✅ **Teste antes de publicar** - Verifique o site após cada alteração
✅ **Mantenha a formatação** - Use a mesma estrutura para novos conteúdos
✅ **Atualize regularmente** - Revise o conteúdo semestralmente

---

## Contato para Suporte

Se tiver dúvidas sobre manutenção do site:
- **Email:** andre.paludo@pucrs.br
- **Telefone:** (51) 3320-3569

---

**Última atualização:** 2026-03-24
