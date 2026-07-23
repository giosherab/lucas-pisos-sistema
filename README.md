# 🏠 Lucas Pisos - Sistema de Gestão

Sistema completo de gestão para loja de pisos, porcelanatos, argamassas e acessórios.

## ✅ Funcionalidades

| Funcionalidade | Descrição |
|----------------|-----------|
| **Dashboard** | KPIs em tempo real, alertas de estoque baixo, top produtos, vendas dos últimos 7 dias |
| **Estoque** | Cadastro, edição, exclusão, filtros, status de estoque, margem de lucro |
| **Vendas (PDV)** | Carrinho, múltiplas formas de pagamento, baixa automática no estoque |
| **Relatórios** | Receita, custo, lucro, margem, vendas por pagamento, estoque por categoria |
| **Recibo** | Impressão de recibo em PDF pronto para impressora térmica |
| **Exportar** | Backup JSON e CSV do estoque |
| **Importar** | Restaurar dados de backup JSON |
| **Alterar Senha** | Troca de senha direto no sistema |

## 🔐 Login

- Acesse o sistema com e-mail e senha cadastrados no Firebase
- Dados salvos na nuvem (Firebase Realtime Database)
- Acesso de qualquer dispositivo com internet

## ☁️ Firebase - Configuração Necessária

### 1. Criar projeto no Firebase

1. Acesse: https://console.firebase.google.com
2. Clique em **"Criar projeto"**
3. Nome: `lucas-pisos-sistema`
4. Desative Google Analytics (não precisa)
5. Clique em **"Criar projeto"**

### 2. Ativar Realtime Database

1. No menu lateral, clique em **"Realtime Database"**
2. Clique em **"Criar banco de dados"**
3. Escolha **"Iniciar no modo bloqueado"**
4. Clique em **"Ativar"**

### 3. Configurar Regras de Segurança

1. Vá em **Realtime Database > Regras**
2. Substitua as regras por:

```json
{
  "rules": {
    "users": {
      "$uid": {
        ".read": "auth != null && auth.uid == $uid",
        ".write": "auth != null && auth.uid == $uid"
      }
    }
  }
}
```

3. Clique em **"Publicar"**

### 4. Ativar Authentication

1. No menu lateral, clique em **"Authentication"**
2. Clique em **"Começar"**
3. Ative **"E-mail/Senha"** (método nativo)
4. Salve

### 5. Criar primeiro usuário

1. Em Authentication, vá na aba **"Usuários"**
2. Clique em **"Adicionar usuário"**
3. E-mail: `admin@lucaspisos.com.br`
4. Senha: `lucas2026`
5. Clique em **"Adicionar usuário"**

### 6. Pegar as credenciais do Firebase

1. Clique no ícone ⚙️ **Configurações do projeto** (engrenagem)
2. Vá em **"Geral"**
3. Em **"Seus aplicativos"**, clique no ícone **</>** (Web)
4. Dê um apelido: `Lucas Pisos Web`
5. Clique em **"Registrar aplicativo"**
6. Copie o objeto `firebaseConfig` que aparece

### 7. Substituir no código

Abra os arquivos `index.html` e `painel.html` e substitua esta parte:

```javascript
const firebaseConfig = {
    apiKey: "SUA_API_KEY",
    authDomain: "SEU_PROJETO.firebaseapp.com",
    databaseURL: "https://SEU_PROJETO-default-rtdb.firebaseio.com",
    projectId: "SEU_PROJETO",
    storageBucket: "SEU_PROJETO.appspot.com",
    messagingSenderId: "000000000",
    appId: "1:000000000:web:000000000000"
};
```

Pelos valores reais do seu projeto Firebase.

### 8. Hospedar no Firebase Hosting (opcional)

Se quiser hospedar no Firebase (grátis):

```bash
npm install -g firebase-tools
firebase login
firebase init hosting
# Selecione o projeto lucas-pisos-sistema
# Diretório público: . (ponto)
# SPA: Yes
firebase deploy
```

Ou use GitHub Pages, Netlify, Vercel, etc.

## 🚀 Como usar no dia a dia

### 1º dia - Cadastrar produtos
1. Faça login
2. Vá em **📦 Estoque**
3. Clique em **"Novo Produto"**
4. Preencha código, nome, categoria, unidade, estoque, mínimo, custo e preço
5. Salve

### Vender
1. Vá em **💰 Vendas**
2. Selecione o produto e quantidade
3. Clique em **"Adicionar ao Carrinho"**
4. Escolha a forma de pagamento
5. Clique em **"Finalizar Venda"**
6. O estoque baixa automaticamente!

### Acompanhar
1. Vá em **📊 Dashboard**
2. Veja vendas do mês, estoque, ticket médio
3. Alertas de estoque baixo aparecem automaticamente

### Fim do mês
1. Vá em **📈 Relatórios**
2. Selecione o período
3. Veja receita, custo, lucro e margem

## 💾 Backup

- Vá em **⚙️ Config**
- Clique em **"Exportar Backup JSON"**
- Guarde o arquivo em um pendrive

## 🎨 Cores da marca

- Azul escuro: `#1a3a5c`
- Laranja: `#e87b0c`

## 📁 Arquivos

| Arquivo | Função |
|---------|--------|
| `index.html` | Tela de login |
| `painel.html` | Sistema completo |
| `logo.png` | Logo da Lucas Pisos |

---
Desenvolvido para Lucas Pisos 🏠
