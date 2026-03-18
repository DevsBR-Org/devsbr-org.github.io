---
title: "Loja: Marcas"
description: Gerenciamento de marcas de produtos pelo painel admin
layout: default
category: admin
order: 34
---

# Loja: Marcas

Gerencie as marcas (brands) dos produtos da loja pelo painel admin do GameCP. As marcas usam a taxonomia `product_brand` do WooCommerce.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. No submenu **Loja**, clique em **Marcas**

> **Permissão necessária:** `manage_woocommerce`

---

## Layout

A página usa um layout de duas colunas:

- **Coluna esquerda** — Formulário para criar/editar marcas
- **Coluna direita** — Lista de marcas existentes

---

## Criar Marca

1. No formulário à esquerda, preencha:

| Campo | Descrição |
| --- | --- |
| **Nome** | Nome da marca (obrigatório) |
| **Slug** | URL amigável (gerado automaticamente se vazio) |
| **Descrição** | Descrição opcional |

2. Clique em **"Criar Marca"**

---

## Editar Marca

1. Na lista, clique no botão **editar** da marca
2. O formulário é preenchido com os dados atuais
3. Altere os campos e clique em **"Salvar"**

---

## Excluir Marca

1. Clique no botão **excluir** da marca
2. Confirme no modal de confirmação

> **Nota:** Todas as ações de criação, edição e exclusão são registradas no log de auditoria do admin.

---

## Próximos Passos

- [Produtos](admin-woo-produtos) — Gerenciar produtos
- [Categorias](admin-woo-categorias) — Organizar categorias
- [Atributos](admin-woo-atributos) — Gerenciar atributos de produtos
