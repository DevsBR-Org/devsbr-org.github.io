---
title: Guild (Recompensas de Guild)
description: Como configurar recompensas automáticas para guildas no painel admin
layout: default
category: modulos
order: 18
---

# Guild (Recompensas de Guild)

O sistema de recompensas de guild permite criar prêmios automáticos distribuídos para guildas com base na posição no ranking.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Guild Rewards**

---

## Criar uma Nova Recompensa

Preencha o formulário com:

### Informações básicas

| Campo | O que preencher |
| --- | --- |
| **Nome da Recompensa** | Nome identificador (ex: "Top 3 Guilds - Arma Especial") |
| **Descrição** | Descrição da recompensa |

### Critérios de entrega

| Campo | O que preencher |
| --- | --- |
| **Enviar para todos** | Marque para enviar a todas as guilds (ignora posição min/max) |
| **Posição Mínima / Máxima** | Faixa de posições no ranking (ex: 1 a 3 = top 3 guilds) |
| **Requisito de Stat** | Selecione um atributo e defina o valor mínimo |
| **Level Mínimo / Máximo** | Faixa de level dos membros |

### Alvo

| Campo | O que preencher |
| --- | --- |
| **Alvo de Entrega** | "Líder" (só o líder recebe) ou "Todos os Membros" |
| **Recompensa única** | Marque para entregar apenas uma vez |
| **Apenas novos membros** | Marque e defina quantos dias (apenas se alvo for "Todos os Membros") |

### Recompensa

| Campo | O que preencher |
| --- | --- |
| **Categoria** | Items, Cash, PvpPoint, GamePoint, Gold, Dalant, GoldPoint, ProcessingPoint, HuntingPoint, Premium ou MaxLevel |
| **Código do Item** | Código do item (apenas para categoria "Items") — com autocomplete |
| **Talics** | Talics do item |
| **Quantidade** | Quantidade a entregar |
| **Valor da Recompensa** | Valor para categorias que não são itens |
| **Período (dias)** | Duração em dias |
| **Ativa** | Marque para ativar a recompensa |

Clique em **"Salvar"**

---

## Gerenciar Recompensas

Na tabela abaixo do formulário, você pode:

- **Ativar/Desativar** — Use o toggle para ligar ou desligar a recompensa
- **Editar** — Clique para carregar os dados no formulário
- **Excluir** — Remova a recompensa

---

## Próximos Passos

- [Quests](quests) — Criar missões individuais
- [Battle Pass](battlepass-gamecp) — Configurar passe de batalha
- [New Player](newplayer) — Campanhas para novos jogadores
