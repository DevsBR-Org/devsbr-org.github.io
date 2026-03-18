---
title: GameCP Coins
description: Como gerenciar a moeda virtual GameCP Coins no painel admin
layout: default
category: admin
order: 9
---

# GameCP Coins

GameCP Coins são pontos internos do painel, armazenados na tabela `tbl_gamecp_gamepoints`. São usados como moeda no **Spin the Wheel** e outros módulos.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. No submenu **Jogadores**, clique em **GameCP Coins**

---

## Gerenciar Coins de um Jogador

1. No campo **"Buscar Jogador"**, digite o login da conta
2. Clique em **"Buscar"**
3. O sistema exibe um card com o **login** e o **saldo atual** de coins
4. Selecione a operação:

| Operação | Cor | Descrição |
| --- | --- | --- |
| **Adicionar** | Verde | Soma ao saldo atual |
| **Remover** | Vermelho | Subtrai do saldo (nunca fica negativo, será zerado se a quantidade for maior) |

5. Informe a **quantidade de coins**
6. Clique em **"Adicionar Coins"** ou **"Remover Coins"**
7. O saldo no card é atualizado automaticamente após a operação

---

## Enviar para Todos

1. Ative o toggle **"Enviar para todos"** (fica destacado em azul)
2. O campo de busca individual desaparece
3. Selecione **Adicionar** ou **Remover**
4. Informe a quantidade
5. Clique no botão de execução
6. Confirme no popup de confirmação

> **Atenção:** A operação será aplicada em **todas as contas** que possuem registro na tabela de GameCP Coins.

---

## Histórico de Transações

O painel inclui uma seção de **histórico de transações** que carrega automaticamente ao abrir a aba.

### Filtrar o histórico

| Filtro | Descrição |
| --- | --- |
| **Login** | Filtra por login do jogador (com autocomplete) |
| **Tipo de Ação** | Todos, Adicionado (Admin), Removido (Admin), Spin (Custo), Spin (Prêmio) |

1. Preencha os filtros desejados
2. Clique em **"Buscar"**

### Informações do histórico

| Coluna | Descrição |
| --- | --- |
| **Conta** | Login do jogador |
| **Ação** | Tipo da operação realizada |
| **Quantidade** | Valor da transação |
| **Saldo Antes** | Saldo antes da operação |
| **Saldo Depois** | Saldo após a operação |
| **Admin** | Quem executou (se aplicável) |
| **Data** | Data e hora da transação |

O histórico suporta **paginação** com opção de alterar o número de registros por página.

---

## Próximos Passos

- [Cash e Premium](cash-premium) — Gerenciar cash e premium do jogo
- [Spin Wheel](spin-wheel) — Configurar a roleta de prêmios
- [Carteira (Wallet)](wallet) — Gerenciar créditos da carteira
