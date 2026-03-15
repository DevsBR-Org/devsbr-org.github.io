---
title: GameCP Coins
description: Moeda virtual do GameCP para eventos, roleta e loja
layout: default
category: modulos
order: 5
---

# GameCP Coins

GameCP Coins é a **moeda virtual interna** do GameCP, utilizada para participar de eventos, comprar itens na loja e girar a roleta.

---

## Visão Geral

| Recurso | Descrição |
|---------|-----------|
| **Tipo** | Moeda virtual interna do GameCP |
| **Obtenção** | Eventos, admin, roleta, promoções |
| **Uso** | Roleta, loja, funcionalidades especiais |
| **Admin** | Adicionar/remover, histórico, rastreamento |
| **Diferencial** | Não é Cash nem Wallet — é exclusiva do GameCP |

---

## O que são GameCP Coins?

GameCP Coins são uma moeda exclusiva do painel GameCP, separada de Cash (moeda do servidor) e Wallet (carteira em dinheiro real). Elas funcionam como uma **moeda de engajamento** para incentivar a participação dos jogadores.

### Diferença entre as Moedas

| Moeda | O que é | Onde é usada | Como obter |
|-------|---------|-------------|------------|
| **GameCP Coins** | Moeda virtual do painel | Roleta, loja GameCP | Eventos, admin, roleta |
| **Cash** | Moeda premium do servidor | Loja do jogo (in-game) | Compra com dinheiro real, admin |
| **Wallet** | Carteira em dinheiro real | Checkout WooCommerce, saques | Vendas no leilão, depósitos |

> **Resumo**: GameCP Coins são para o painel, Cash é para o servidor, Wallet é dinheiro real.

---

## Como Ganhar GameCP Coins

### 1. Eventos

Administradores podem criar eventos que premiam jogadores com GameCP Coins como recompensa por participação ou conquistas.

### 2. Concessão pelo Admin

O admin pode adicionar coins diretamente na conta de qualquer jogador pelo painel administrativo.

### 3. Prêmios da Roleta (Spin Wheel)

A roleta pode ser configurada para dar GameCP Coins como prêmio em um ou mais segmentos.

### 4. Promoções e Bônus

Campanhas especiais podem incluir distribuição de coins para todos os jogadores ou para grupos específicos.

---

## Como Gastar GameCP Coins

### 1. Roleta (Spin Wheel)

A roleta pode exigir um custo em GameCP Coins para cada giro, configurável pelo admin.

### 2. Loja GameCP

Itens disponíveis na loja do GameCP podem ter preço em GameCP Coins, permitindo que jogadores troquem suas coins por itens, cash ou outros benefícios.

### 3. Funcionalidades Especiais

Dependendo da configuração do servidor, coins podem ser usadas para desbloquear funcionalidades ou serviços dentro do painel.

---

## Administração de GameCP Coins

### Acessando

1. Faça login como admin no GameCP
2. Acesse **Admin > GameCP Coins**
3. Utilize as ferramentas de gerenciamento

### Adicionar/Remover Coins

1. Busque o jogador pelo nome ou conta
2. Defina a **quantidade** de coins a adicionar ou remover
3. (Opcional) Adicione uma **descrição/motivo** para a operação
4. Confirme a ação

### Histórico de Transações

O admin tem acesso ao histórico completo de transações com **paginação**:

| Coluna | Descrição |
|--------|-----------|
| **Data** | Data e hora da transação |
| **Jogador** | Conta/personagem envolvido |
| **Ação** | Tipo da operação (adição, remoção, gasto, prêmio) |
| **Quantidade** | Número de coins movimentadas |
| **Saldo Antes** | Saldo do jogador antes da transação |
| **Saldo Depois** | Saldo do jogador após a transação |
| **Descrição** | Motivo ou origem da transação |

### Rastreamento de Saldo

- **Saldo antes/depois**: Cada transação registra o saldo anterior e posterior, garantindo rastreabilidade completa
- **Log de ações**: Todas as operações (admin, sistema, jogador) são registradas
- **Auditoria**: O admin pode verificar o histórico completo de qualquer jogador

---

## Próximos Passos

- [Roleta de Prêmios](spin-wheel) — Configuração da roleta que usa GameCP Coins
- [Loja e Checkout](gamecp-shop-checkout) — Loja onde coins podem ser gastas
- [Carteira (Wallet)](wallet) — Entenda a diferença entre Wallet e Coins
