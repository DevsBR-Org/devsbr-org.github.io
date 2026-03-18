---
title: "Loja: Cupons"
description: Criação e gerenciamento de cupons de desconto pelo painel admin
layout: default
category: admin
order: 32
---

# Loja: Cupons

Crie e gerencie cupons de desconto para a loja diretamente pelo painel admin do GameCP.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. No submenu **Loja**, clique em **Cupons**

> **Permissão necessária:** `manage_woocommerce`

---

## Lista de Cupons

A página exibe todos os cupons cadastrados:

| Coluna | Descrição |
| --- | --- |
| **Código** | Código do cupom |
| **Tipo** | Desconto fixo ou percentual |
| **Valor** | Valor do desconto |
| **Status** | Publicado ou Rascunho |
| **Usos** | Quantidade de vezes utilizado |
| **Data** | Data de criação |

### Busca

- Use o campo de busca para encontrar cupons pelo código

---

## Criar Novo Cupom

1. Clique no botão **"Novo Cupom"**
2. Preencha os campos no modal:

| Campo | Descrição |
| --- | --- |
| **Código** | Código que o cliente digitará (ex: `DESCONTO10`) |
| **Tipo de Desconto** | Fixo no carrinho, Fixo no produto ou Percentual |
| **Valor** | Valor do desconto |
| **Uso máximo** | Limite de usos totais (0 = ilimitado) |
| **Uso por cliente** | Limite de usos por cliente |
| **Data de expiração** | Data limite para uso do cupom |

3. Clique em **"Criar Cupom"**

---

## Gerenciar Cupons

- **Editar** — Clique no cupom para alterar suas configurações
- **Excluir** — Remova cupons que não são mais necessários

---

## Próximos Passos

- [Produtos](admin-woo-produtos) — Gerenciar produtos
- [Pedidos](admin-woo-pedidos) — Visualizar pedidos
- [Categorias](admin-woo-categorias) — Organizar categorias
