---
title: Carteira (Wallet)
description: Como gerenciar créditos, saques e configurações da carteira GameCP
layout: default
category: admin
order: 10
---

# Carteira (Wallet)

A carteira GameCP é um sistema de créditos em **USD** usado para compras na loja do GameCP. **Não é o cash do jogo.**

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Wallet**

---

## Configurações da Wallet

### Passo a passo

1. **Ativar Saques** — Marque o toggle para permitir que jogadores solicitem saques
2. **Valor Mínimo (USD)** — Defina o valor mínimo para solicitar saque (ex: 10.00)
3. **Taxa de Saque (%)** — Defina a porcentagem descontada do saque (ex: 5.00%)
4. Clique em **"Salvar Configurações"**

---

## Gerenciar Créditos

Aqui você pode adicionar, remover ou definir o saldo de um jogador.

### Passo a passo

1. Selecione o **tipo de operação**:
   - **Adicionar** — soma ao saldo atual
   - **Remover** — subtrai do saldo
   - **Definir** — substitui o saldo pelo valor informado
2. No campo **"Login da Conta"**, digite o login do jogador
3. No campo **"Valor (USD)"**, informe o valor
4. No campo **"Motivo da Operação"**, descreva o motivo (será registrado no histórico)
5. Clique em **"Executar Operação"**

---

## Solicitações de Saque

A tabela mostra os últimos 50 pedidos de saque, com status, valor, método de pagamento e dados.

### Aprovar um saque

1. Localize o saque com status **"Pendente"**
2. Clique no botão **"Aprovar"**
3. Confirme a operação

### Rejeitar um saque

1. Localize o saque com status **"Pendente"**
2. Clique no botão **"Rejeitar"**
3. Confirme a operação
4. O valor será **devolvido automaticamente** ao saldo do jogador

---

## Usuários com Saldo

Lista todas as contas que possuem crédito na carteira.

### Passo a passo

1. No campo **"Filtrar por login"**, digite um login para buscar (opcional)
2. Clique em **"Buscar"**
3. A lista é carregada automaticamente ao abrir a aba

---

## Próximos Passos

- [Cash e Premium](cash-premium) — Gerenciar cash e premium do jogo
- [GameCP Coins](gamecp-coins) — Gerenciar a moeda virtual do painel
- [Loja e Checkout](gamecp-shop-checkout) — Compras integradas com WooCommerce
