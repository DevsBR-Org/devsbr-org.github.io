---
title: Histórico de Logs
description: Como pesquisar logs de itens do servidor no painel admin
layout: default
category: administracao
order: 19
---

# Histórico de Logs

Permite buscar e visualizar logs de transações de itens do ZoneServer do RF Online (pickup, trade, sell, buy, upgrade, etc.).

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **History Logs**

---

## Pesquisar Logs

Preencha os filtros de busca:

| Campo | O que preencher |
| --- | --- |
| **Termo de Busca** | Nome do personagem ou nome do item |
| **Tipo de Busca** | Selecione se está buscando por nickname, código do item, etc. |
| **Data** | Data para filtrar |
| **Hora Início / Hora Fim** | Intervalo de horário (padrão: 00:00 a 23:59) |
| **Tipo de Evento** | pickup, trade, sell, buy, dump, trunk, reward, read_cash ou upgrade |
| **Código do Item** | Código específico do item (opcional) |

Clique em **"Buscar"** para ver os resultados.

---

## Tipos de Eventos

| Evento | Descrição |
| --- | --- |
| **pickup** | Item coletado do chão |
| **trade** | Item trocado entre jogadores |
| **sell** | Item vendido para NPC |
| **buy** | Item comprado de NPC |
| **dump** | Item descartado |
| **trunk** | Item movido para/do baú |
| **reward** | Item recebido como recompensa |
| **read_cash** | Item obtido via cash shop |
| **upgrade** | Item aprimorado |

Os resultados são paginados com 100 registros por página.

---

## Próximos Passos

- [Painel Admin](gamecp-admin-panel) — Visão geral do painel admin
- [Sprite Sheet](sprite-sheet) — Processar ícones de itens
- [Configurações](configuracoes) — Ajustar funcionalidades do sistema
