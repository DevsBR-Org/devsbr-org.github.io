---
title: "Loja: Categorias"
description: Gerenciamento de categorias de produtos pelo painel admin
layout: default
category: admin
order: 33
---

# Loja: Categorias

Organize os produtos da loja em categorias diretamente pelo painel admin do GameCP.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. No submenu **Loja**, clique em **Categorias**

> **Permissão necessária:** `manage_woocommerce`

---

## Lista de Categorias

A página exibe todas as categorias em um layout de duas colunas:

- **Coluna esquerda** — Formulário para criar/editar
- **Coluna direita** — Lista de categorias existentes

---

## Criar Categoria

1. No formulário à esquerda, preencha:

| Campo | Descrição |
| --- | --- |
| **Nome** | Nome da categoria (obrigatório) |
| **Slug** | URL amigável (gerado automaticamente se vazio) |
| **Categoria Pai** | Selecione uma categoria pai para criar hierarquia |
| **Descrição** | Descrição opcional da categoria |

2. Clique em **"Criar Categoria"**

---

## Editar Categoria

1. Na lista de categorias, clique no botão **editar** da categoria desejada
2. O formulário à esquerda é preenchido com os dados atuais
3. Altere os campos necessários
4. Clique em **"Salvar Alterações"**

---

## Excluir Categoria

1. Clique no botão **excluir** da categoria
2. Confirme a exclusão no modal de confirmação

> **Atenção:** Excluir uma categoria não exclui os produtos associados a ela.

---

## Visibilidade

É possível controlar a visibilidade das categorias na loja, permitindo ocultar categorias específicas sem excluí-las.

---

## Próximos Passos

- [Produtos](admin-woo-produtos) — Gerenciar produtos
- [Marcas](admin-woo-marcas) — Gerenciar marcas de produtos
- [Atributos](admin-woo-atributos) — Gerenciar atributos
