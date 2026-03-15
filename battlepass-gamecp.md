---
title: Battle Pass
description: Como criar e gerenciar temporadas do passe de batalha no painel admin
layout: default
category: admin
order: 12
---

# Battle Pass

O Battle Pass (Passe de Batalha) permite criar temporadas com trilhas de recompensas **Normal** e **Premium**, cada uma com múltiplos níveis.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Battle Pass**

---

## Criar uma Nova Temporada

1. Clique em **"Cadastrar nova temporada"**
2. No modal, preencha:

| Campo | O que preencher |
| --- | --- |
| **Nome** | Nome da temporada (ex: "Temporada 1 - Inverno") |
| **Descrição** | Descrição breve da temporada |
| **Data de Início** | Quando a temporada começa |
| **Data de Fim** | Quando a temporada termina |

3. Clique em **"Cadastrar"**

---

## Configurar Recompensas

Após criar a temporada, configure as recompensas:

1. Selecione a temporada no dropdown (a página recarrega)
2. Escolha a trilha: **Normal** ou **Premium** (abas)
3. Clique em **"Adicionar Nível"** para criar um novo nível
4. Para cada nível:
   - Defina a **XP Necessária** para desbloquear
   - Clique em **"Adicionar Item"** para adicionar recompensas
5. Para cada item de recompensa, preencha:

| Campo | O que preencher |
| --- | --- |
| **Categoria** | Tipo: Items, Cash, PvpPoint, GamePoint, etc. |
| **Código Item** | Código do item (com autocomplete) — apenas para categoria "Items" |
| **Talics** | Selecione e adicione talics ao item |
| **Quantidade** | Quantidade a entregar |
| **Tempo** | Tempo de aluguel (0 = permanente) |
| **Valor** | Valor para categorias que não são itens (Cash, Premium, etc.) |

6. Clique em **"Salvar recompensas"**

---

## Editar uma Temporada

1. Selecione a temporada no dropdown
2. Altere as datas, descrição ou recompensas
3. Salve as alterações

---

## Excluir uma Temporada

1. Selecione a temporada no dropdown
2. Clique em **"Excluir temporada"**
3. Confirme no popup

> **Atenção:** Excluir uma temporada remove todos os níveis e recompensas associados.

---

## Próximos Passos

- [Quests](quests) — Criar missões com recompensas
- [Spin Wheel](spin-wheel) — Configurar a roleta de prêmios
- [New Player](newplayer) — Campanhas para novos jogadores
