---
title: Pesquisar Itens
description: Como buscar itens no banco de dados e gerenciar permissões de leilão
layout: default
category: admin
order: 24
---

# Pesquisar Itens

Ferramenta de busca avançada no banco de dados de itens do jogo. Também permite controlar quais itens podem ser vendidos no leilão.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Pesquisar Itens**

---

## Buscar Itens

1. **Categoria** — Selecione a categoria (ou "Todas Categorias")
2. **Busca** — Digite o nome ou código do item (mínimo 3 caracteres)
3. **Level** — Defina o range de level mínimo e máximo (opcional)
4. **Grade** — Filtre por grau: Normal, Type B, A, C, D, Upper, Type L ou Type M
5. **Resultados por página** — Escolha 20, 50 ou 100
6. Clique em **"Buscar"** ou pressione Enter

---

## Resultados

A tabela mostra:

| Coluna | O que exibe |
| --- | --- |
| **Ícone** | Imagem do item (passe o mouse para ver tooltip) |
| **Código** | Código interno do item |
| **Nome** | Nome do item |
| **Level** | Nível do item |
| **Grade** | Grau/raridade |
| **Leilão** | Toggle para permitir/bloquear no leilão |
| **Ações** | Botão para copiar o código |

---

## Controlar Itens no Leilão

1. Use o **toggle** na coluna "Leilão" para permitir ou bloquear cada item
2. Use **"Marcar Todos"** ou **"Desmarcar Todos"** para operações em massa
3. O contador mostra quantas alterações estão pendentes
4. Clique em **"Salvar"** para aplicar as alterações

---

## Próximos Passos

- [JSON Generator](json-generator) — Gerar JSONs dos itens
- [Enviar Itens](admin-enviar-itens) — Enviar itens para personagens
- [Leilão](leilao) — Configurar o sistema de leilão
