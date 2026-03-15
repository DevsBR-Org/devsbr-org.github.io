---
title: Sprite Sheet
description: Como processar arquivos SPR para extrair ícones de itens
layout: default
category: administracao
order: 20
---

# Sprite Sheet

Ferramenta para upload e processamento de arquivos `.SPR` do RF Online, extraindo sprites individuais (imagens JPG) para uso no sistema.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Sprite Sheet**

---

## Processar um Arquivo SPR

1. Clique em **"Choose File"** (Escolher Arquivo)
2. Selecione um arquivo `.spr` do seu computador
3. Clique em **"Processar SPR"**
4. Aguarde o processamento (uma barra de progresso será exibida)
5. Veja o resultado no console de saída

> **Requisitos do servidor:** Python com biblioteca Pillow instalada, e funções `exec`/`shell_exec`/`proc_open` habilitadas no PHP.

---

## Gerenciar Sprites Gerados

Após o processamento, os sprites aparecem em uma galeria:

- **Visualizar** — Navegue pelos sprites gerados
- **Excluir individual** — Clique no botão de excluir em cada sprite
- **Excluir todos** — Clique em **"Excluir Todos"** para remover todas as imagens geradas

---

## Próximos Passos

- [JSON Generator](json-generator) — Gerar JSONs dos itens do jogo
- [Pesquisar Itens](search-items) — Buscar itens no banco de dados
- [Histórico de Logs](history-logs) — Pesquisar logs de itens
