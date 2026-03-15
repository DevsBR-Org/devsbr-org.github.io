---
title: GameCP Coins
description: Como gerenciar a moeda virtual GameCP Coins no painel admin
layout: default
category: admin
order: 9
---

# GameCP Coins

GameCP Coins são pontos internos do painel, usados como moeda no **Spin the Wheel** e outros módulos.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **GameCP Coins**

---

## Consultar Saldo de um Jogador

1. No campo **"Login do Jogador"**, digite o login da conta
2. Clique em **"Consultar"**
3. O sistema exibe o saldo atual de GameCP Coins do jogador

---

## Adicionar ou Remover Coins

1. No campo **"Login do Jogador"**, digite o login da conta
2. No campo **"Quantidade"**, informe o valor (ex: 100)
3. No campo **"Ação"**, selecione:
   - **Adicionar** — soma ao saldo atual
   - **Remover** — subtrai do saldo (nunca fica negativo, será zerado se a quantidade for maior que o saldo)
4. Clique em **"Aplicar"**

> Todas as operações são registradas nos logs de auditoria.

---

## Histórico de Transações

O histórico mostra todas as movimentações de GameCP Coins.

### Filtrar o histórico

1. No campo **"Filtrar por Login"**, digite o login para buscar (opcional)
2. No campo **"Tipo de Ação"**, selecione o filtro:
   - **Todos** — todas as transações
   - **Adicionado (Admin)** — coins adicionados manualmente
   - **Removido (Admin)** — coins removidos manualmente
   - **Spin (Custo)** — coins gastos na roleta
   - **Spin (Prêmio)** — coins ganhos na roleta
3. Clique em **"Buscar"**

O histórico carrega automaticamente ao abrir a aba e suporta paginação.

---

## Próximos Passos

- [Cash e Premium](cash-premium) — Gerenciar cash e premium do jogo
- [Spin Wheel](spin-wheel) — Configurar a roleta de prêmios
- [Carteira (Wallet)](wallet) — Gerenciar créditos da carteira
