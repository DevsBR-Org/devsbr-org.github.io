---
title: "Loja: Pedidos"
description: Visualização e gerenciamento de pedidos WooCommerce pelo painel admin
layout: default
category: admin
order: 31
---

# Loja: Pedidos

Visualize e gerencie todos os pedidos da loja diretamente pelo painel admin do GameCP.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. No submenu **Loja**, clique em **Pedidos**

> **Permissão necessária:** `manage_woocommerce`

---

## Lista de Pedidos

A página exibe os pedidos com paginação (20 por página):

| Coluna | Descrição |
| --- | --- |
| **ID** | Número do pedido |
| **Cliente** | Nome e conta do jogador |
| **Status** | Status do pedido (badges coloridos) |
| **Total** | Valor total do pedido |
| **Método** | Método de pagamento utilizado |
| **Data** | Data de criação do pedido |

### Filtros disponíveis

- **Busca por ID** — digite o número do pedido
- **Busca por login** — pesquisa pelo login da conta do jogo
- **Filtrar por status** — Processing, Completed, On-hold, Pending, Cancelled, Refunded, Failed
- **Filtrar por tipo** — Filtro específico para pedidos de leilão

---

## Detalhes do Pedido

Clique em um pedido para ver os detalhes completos:

### Informações exibidas

| Campo | Descrição |
| --- | --- |
| **Cliente** | Nome e email do comprador |
| **Conta do Jogo** | Login da conta vinculada |
| **Personagem** | Personagem selecionado para entrega |
| **Data** | Data e hora do pedido |
| **Método de Pagamento** | Forma de pagamento utilizada |
| **Total** | Valor total |
| **Status** | Status atual com badge colorido |

### Status e Cores

| Status | Cor | Descrição |
| --- | --- | --- |
| **Completed** | Verde | Pedido finalizado e entregue |
| **Processing** | Azul | Pedido em processamento |
| **On-hold** | Amarelo | Aguardando ação |
| **Pending** | Cinza | Pendente de pagamento |
| **Cancelled** | Vermelho | Pedido cancelado |
| **Refunded** | Roxo | Pedido reembolsado |

### Metadados do Jogo

O sistema exibe metadados específicos do GameCP:

- **Login da conta** (`_billing_login_account`)
- **Personagem** (`_billing_char_account`)
- **Entrega realizada** (`_devsbr_entrega_feita`)
- **Lock de entrega** (`_devsbr_entrega_lock`)

---

## Próximos Passos

- [Produtos](admin-woo-produtos) — Gerenciar produtos da loja
- [Cupons](admin-woo-cupons) — Criar cupons de desconto
- [Categorias](admin-woo-categorias) — Organizar categorias
