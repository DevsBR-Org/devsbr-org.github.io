---
title: Quests
description: Como criar e gerenciar missões com recompensas no painel admin
layout: default
category: admin
order: 11
---

# Quests

O sistema de quests permite criar missões que os jogadores podem completar para receber recompensas com cooldown.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Quests**

---

## Criar uma Nova Quest

1. No dropdown de quests, selecione **"Nova Quest..."**
2. Preencha os campos:

| Campo | O que preencher |
| --- | --- |
| **Título** | Nome da missão (ex: "Missão Diária") |
| **Escopo** | "Por Conta" (1 resgate por conta) ou "Por Personagem" (1 resgate por char) |
| **Ativa** | Marque para ativar a quest |
| **Cooldown** | Tempo de espera entre resgates. Informe o número e selecione a unidade (Segundos, Minutos, Horas ou Dias) |
| **Level Mode** | "Auto" (pega o level do char automaticamente) ou "Manual" (defina min/max level) |
| **Min Level / Max Level** | Apenas se Level Mode for "Manual" |

3. Na seção **Recompensas**, clique em **"Adicionar Recompensa"**
4. Para cada recompensa, preencha:
   - **Código Item** — digite o código ou busque pelo nome (autocomplete)
   - **Talics** — selecione a talic desejada e clique em **"+"** para adicionar (clique em **"-"** para remover)
   - **Qtd** — quantidade do item
   - **Tempo** — tempo de aluguel (0 para permanente)
5. Clique em **"Salvar Quest"**

> Você precisa adicionar pelo menos 1 recompensa para salvar.

---

## Editar uma Quest Existente

1. No dropdown, selecione a quest desejada
2. Os campos serão preenchidos automaticamente
3. Faça as alterações desejadas
4. Clique em **"Salvar Quest"**

---

## Excluir uma Quest

1. Selecione a quest no dropdown
2. Clique em **"Excluir Quest"**
3. Confirme a exclusão no popup

> **Atenção:** Excluir uma quest também remove todo o histórico de resgates dos jogadores.

---

## Lista de Quests

Na parte inferior da página, uma tabela exibe todas as quests cadastradas com:
- ID, Título, Escopo, Cooldown, Level e Status (Ativa/Inativa)

---

## Próximos Passos

- [Battle Pass](battlepass-gamecp) — Configurar passe de batalha
- [New Player](newplayer) — Campanhas para novos jogadores
- [Spin Wheel](spin-wheel) — Configurar a roleta de prêmios
