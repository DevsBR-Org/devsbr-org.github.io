---
title: "Loja: Produtos"
description: Gerenciamento de produtos WooCommerce pelo painel admin do GameCP
layout: default
category: admin
order: 30
---

# Loja: Produtos

Gerencie todos os produtos da loja diretamente pelo painel admin do GameCP, sem precisar acessar o WordPress.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. No submenu **Loja**, clique em **Produtos**

> **Permissão necessária:** `manage_woocommerce`
> **Requisito:** WooCommerce deve estar ativo no WordPress

---

## Lista de Produtos

A página exibe todos os produtos cadastrados com:

| Coluna | Descrição |
| --- | --- |
| **Nome** | Nome do produto |
| **Status** | Publicado, Rascunho, Pendente ou Privado |
| **Preço** | Preço regular e promocional |
| **Categoria** | Categorias associadas |
| **Estoque** | Quantidade em estoque |
| **Data** | Data de criação |

### Filtros disponíveis

- **Busca por texto** — pesquisa por nome do produto
- **Filtrar por categoria** — dropdown com todas as categorias
- **Filtrar por status** — Publicado, Rascunho, Pendente, Privado
- **Paginação** — 20 produtos por página

> **Nota:** Produtos da marca "leilão" são automaticamente excluídos da listagem.

---

## Criar Novo Produto

1. Clique no botão **"Novo Produto"** (ou acesse via submenu)
2. Preencha os campos:

| Campo | Descrição |
| --- | --- |
| **Nome** | Nome do produto |
| **Tipo** | Simple, Variable, Grouped ou External |
| **Status** | Publicado ou Rascunho |
| **Visibilidade** | Visibilidade no catálogo |
| **Preço** | Preço regular |
| **Categoria** | Selecione uma ou mais categorias |
| **Virtual** | Marque se for produto virtual (RF Online / MU Online) |

3. Clique em **"Criar Produto"**
4. O sistema redireciona para a página de edição do produto criado

---

## Editar Produto

1. Na lista de produtos, clique no produto desejado
2. Altere os campos necessários (nome, preço, status, categorias, etc.)
3. Clique em **"Salvar Alterações"**

---

## Excluir Produto

1. Na lista de produtos, clique no botão de **excluir** do produto
2. Confirme a exclusão no popup

> **Atenção:** A exclusão é permanente e não pode ser desfeita.

---

## Próximos Passos

- [Pedidos](admin-woo-pedidos) — Gerenciar pedidos da loja
- [Categorias](admin-woo-categorias) — Organizar categorias de produtos
- [Cupons](admin-woo-cupons) — Criar cupons de desconto
