---
title: Configurações do GameCP
description: Como configurar manutenção, funcionalidades e verificação de email no painel admin
layout: default
category: admin
order: 7
---

# Configurações do GameCP

Aba de configurações rápidas do painel admin. Aqui você controla o que está ligado ou desligado no GameCP.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Configurações**

---

## Modo Manutenção

Bloqueia o acesso de todos os jogadores ao GameCP. Admins continuam acessando normalmente.

### Passo a passo

1. Marque o checkbox **"Ativar Modo Manutenção"**
2. Clique em **"Salvar Manutenção"**

Para desativar, desmarque o checkbox e salve novamente.

---

## Funcionalidades do GameCP

Nesta seção você liga ou desliga recursos individualmente. Cada toggle funciona de forma independente.

### Opções disponíveis

| Toggle | O que faz |
| --- | --- |
| **Buscar Jogadores** | Permite que jogadores pesquisem e vejam equipamentos de outros jogadores |
| **Cadastro de Conta** | Permite criar novas contas. Desativado = bloqueia registro e oculta o formulário |
| **Bloquear Leilão** | Oculta links do leilão e impede o acesso às páginas |
| **Bloquear Passe de Batalha** | Oculta o menu e bloqueia acesso ao Battle Pass |
| **Ativar AutoCash** | Liga/desliga a entrega automática de cash por tempo online |
| **Loja GameCP** | Ativa a página "Loja" no menu do GameCP |

### Passo a passo

1. Marque ou desmarque os toggles desejados
2. Clique em **"Salvar Funcionalidades"**

> **Nota:** O toggle do AutoCash só funciona se o módulo AutoCash estiver ativado nas configurações de módulos do WordPress.

---

## Verificação de Email Obrigatória

Permite escolher quais páginas do GameCP serão bloqueadas para jogadores que **não verificaram o email**.

### Páginas disponíveis para bloqueio

| Página | Descrição |
| --- | --- |
| **Personagens** | Visualizar personagens |
| **Inventário** | Visualizar e gerenciar itens |
| **Buscar Jogadores** | Pesquisar outros jogadores |
| **Carteira** | Acessar saldo e transações |
| **Loja** | Comprar itens na loja |
| **Leilão** | Acessar o sistema de leilões |
| **Navegar Leilão** | Buscar itens no leilão |
| **Resgates** | Resgatar códigos e prêmios |
| **Passe de Batalha** | Acessar o Battle Pass |
| **Roleta** | Girar a roleta de prêmios |
| **Carrinho** | Acessar o carrinho de compras |
| **Perfil** | Editar perfil da conta |

### Passo a passo

1. Marque as páginas que devem exigir email verificado
2. Clique em **"Salvar Verificação de Email"**

> Se nenhuma página for selecionada, a verificação de email não bloqueará nenhuma funcionalidade.

---

## Próximos Passos

- [Painel Admin](gamecp-admin-panel) — Visão geral do painel administrativo
- [2FA e Segurança](2fa-seguranca) — Configurar autenticação de dois fatores
- [Cash e Premium](cash-premium) — Gerenciar cash e premium dos jogadores
