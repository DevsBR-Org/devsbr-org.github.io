---
title: "Loja: Novo Produto (Redeem)"
description: Criação de produto variável para o sistema de resgates antecipados
layout: default
category: admin
order: 36
---

# Loja: Novo Produto (Redeem Variável)

Ferramenta simplificada para criar produtos variáveis destinados ao sistema de **Resgates Antecipados**, com faixas de valor pré-configuradas.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. No submenu **Loja**, clique em **Novo Produto**

> **Permissão necessária:** `manage_woocommerce`

---

## O que esse módulo faz?

Cria automaticamente um **produto variável** no WooCommerce com:

- Atributo **"Valor"** registrado como taxonomia
- **Variações** com faixas de preço pré-definidas
- Categoria **"early-redemption"** (resgates antecipados)
- Flag de **produto virtual** ativado

---

## Como Criar

1. Preencha o **nome do produto**
2. Defina as **faixas de valor** (variações com preços diferentes)
3. Clique em **"Criar Produto"**
4. O sistema cria automaticamente:
   - O produto principal
   - A taxonomia de atributo "Valor"
   - Todas as variações com seus respectivos preços

---

## Quando Usar

Use este módulo quando precisar criar produtos para o sistema de Redeem que possuem múltiplas opções de valor (ex: pacotes de cash com valores diferentes).

Para produtos simples ou de outros tipos, use o módulo **[Produtos](admin-woo-produtos)** padrão.

---

## Próximos Passos

- [Produtos](admin-woo-produtos) — Gerenciar todos os produtos
- [Redeem](redeem-gamecp) — Configurar sistema de resgates
- [Categorias](admin-woo-categorias) — Organizar categorias
