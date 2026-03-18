---
title: "Loja: Atributos"
description: Gerenciamento de atributos de produtos pelo painel admin
layout: default
category: admin
order: 35
---

# Loja: Atributos

Gerencie os atributos de produtos da loja (cor, tamanho, tipo, etc.) diretamente pelo painel admin do GameCP.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. No submenu **Loja**, clique em **Atributos**

> **Permissão necessária:** `manage_woocommerce`

---

## O que são Atributos?

Atributos são propriedades dos produtos usadas para criar **variações** (ex: produto com diferentes tamanhos ou cores). Cada atributo pode ter múltiplos **termos** (valores).

**Exemplo:**
- Atributo: **Valor** → Termos: R$ 10, R$ 20, R$ 50
- Atributo: **Tipo** → Termos: Cash, Premium, Item

---

## Layout

A página usa um layout de duas colunas:

- **Coluna esquerda** — Formulário para criar/editar atributos
- **Coluna direita** — Lista de atributos e seus termos

---

## Criar Atributo

1. No formulário à esquerda, preencha:

| Campo | Descrição |
| --- | --- |
| **Nome** | Nome do atributo (obrigatório) |
| **Slug** | Identificador único (gerado automaticamente) |
| **Ordenação** | Como os termos são ordenados (nome, ID, etc.) |

2. Clique em **"Criar Atributo"**

---

## Gerenciar Termos

Após criar um atributo, adicione termos (valores) a ele:

1. Na lista de atributos, clique no atributo desejado para expandir
2. Digite o nome do novo termo
3. Clique em **"Adicionar"**
4. Para excluir um termo, clique no botão de remover ao lado dele

---

## Editar Atributo

1. Clique no botão **editar** do atributo na lista
2. Altere nome, slug ou ordenação
3. Clique em **"Salvar"**

---

## Excluir Atributo

1. Clique no botão **excluir** do atributo
2. Confirme no modal

> **Atenção:** Excluir um atributo remove também todos os seus termos e pode afetar produtos variáveis que usam esse atributo.

---

## Próximos Passos

- [Produtos](admin-woo-produtos) — Gerenciar produtos
- [Categorias](admin-woo-categorias) — Organizar categorias
- [Marcas](admin-woo-marcas) — Gerenciar marcas
