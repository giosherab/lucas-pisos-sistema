# 🏠 Lucas Pisos - Sistema de Gestão

## 📋 O que é?
Sistema completo de controle de estoque e vendas para a loja Lucas Pisos.
Funciona 100% no navegador, sem necessidade de servidor ou banco de dados.

## 🚀 Como instalar no domínio

### Opção 1: Hospedagem com cPanel (mais comum)
1. Acesse o cPanel do domínio (ex: lucaspisos.com.br/cpanel)
2. Vá em **Gerenciador de Arquivos**
3. Navegue até a pasta `public_html`
4. Faça upload dos 3 arquivos:
   - `index.html` (tela de login)
   - `painel.html` (sistema)
   - `.htaccess` (configurações)
5. Pronto! Acesse `https://lucaspisos.com.br`

### Opção 2: FTP
1. Use FileZilla ou similar
2. Conecte no servidor FTP do domínio
3. Envie os 3 arquivos para a pasta `public_html`
4. Pronto!

### Opção 3: GitHub Pages (GRÁTIS)
1. Crie um repositório no GitHub
2. Faça upload dos 3 arquivos
3. Ative GitHub Pages em Settings > Pages
4. Configure o domínio customizado
5. Pronto! Sem pagar nada de hospedagem

## 🔐 Login padrão
- **Usuário:** `admin`
- **Senha:** `lucas2026`

> ⚠️ **IMPORTANTE:** Altere a senha editando o arquivo `index.html` na linha onde está `s==='lucas2026'`

## 💾 Como funciona o salvamento?
- Todos os dados ficam salvos no **navegador** (LocalStorage)
- Mesmo fechando o computador, os dados permanecem
- Para fazer backup: vá em **⚙️ Config → 📥 Exportar Backup JSON**
- Para restaurar: vá em **⚙️ Config → 📤 Importar dados**

## 📱 Compatibilidade
- ✅ Google Chrome
- ✅ Mozilla Firefox
- ✅ Microsoft Edge
- ✅ Safari (Mac)
- ✅ Funciona no celular/tablet

## 🎨 Personalizar cores
As cores seguem a identidade visual da Lucas Pisos (azul + laranja).
Para alterar, edite as variáveis CSS no início de cada arquivo.

## 🆘 Suporte
Em caso de dúvidas, entre em contato com quem desenvolveu o sistema.

---
**Versão:** 1.0 | **Zero custo de hospedagem**
