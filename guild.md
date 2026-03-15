---
title: Sistema de Guilds
description: Gerenciamento de guilds, membros, ranking e recompensas
layout: default
category: modulos
order: 10
---

# Sistema de Guilds

O módulo de Guilds oferece **gerenciamento completo de guilds** para líderes, membros e administradores, integrado ao GameCP.

---

## Visão Geral

| Recurso | Descrição |
|---------|-----------|
| **Perfil da Guild** | Edição de descrição, emblema e configurações |
| **Membros** | Lista completa com ranks, stats e busca |
| **Tesouraria** | Controle de Gold e Dalant da guild |
| **Ranking** | Classificação por battle score entre guilds |
| **Recrutamento** | Configurações de entrada de novos membros |
| **Recompensas (Admin)** | Sistema de premiação por posição no ranking |

---

## Gerenciamento da Guild (Líder)

### Perfil da Guild

O líder da guild tem acesso às seguintes funcionalidades:

1. **Editar Descrição**: Altere a descrição pública da guild
2. **Emblema**: Visualize o emblema atual da guild
3. **Nível e Stats**: Acompanhe o nível da guild e suas estatísticas gerais
4. **Tesouraria**: Gerencie os recursos financeiros da guild

### Tesouraria

| Moeda | Descrição |
|-------|-----------|
| **Gold** | Moeda principal acumulada pela guild |
| **Dalant** | Moeda secundária da guild |

O líder pode visualizar o saldo atual e acompanhar o histórico de movimentações.

### Configurações de Recrutamento

O líder pode definir as regras de entrada para novos membros:

- Abrir ou fechar recrutamento
- Definir requisitos mínimos para ingresso
- Aprovar ou rejeitar solicitações pendentes

### Ações de Liderança

- **Promover/Rebaixar** membros de rank
- **Expulsar** membros da guild
- **Transferir liderança** para outro membro
- **Editar informações** gerais da guild

---

## Membros da Guild

A página de membros exibe o **roster completo** da guild com informações detalhadas.

### Informações Exibidas

| Coluna | Descrição |
|--------|-----------|
| **Nome** | Nome do personagem membro |
| **Rank** | Posição hierárquica na guild |
| **Stats** | Estatísticas do membro (nível, classe, etc.) |
| **Emblema** | Emblema da guild exibido junto ao membro |

### Busca e Filtragem

- **Busca por nome**: Pesquise membros pelo nome do personagem
- **Filtro por rank**: Filtre membros por posição hierárquica
- **Ordenação**: Ordene por diferentes critérios (nome, rank, stats)

---

## Ranking de Guilds

O Ranking exibe a **classificação geral das guilds** do servidor em formato de leaderboard.

### Como Funciona

1. As guilds são ordenadas por **battle score** (pontuação de batalha)
2. Cada guild exibe seu **emblema** ao lado do nome
3. As **cores de raça** são aplicadas para identificação visual (Bellato, Cora, Accretia)
4. O **líder** de cada guild é identificado na listagem
5. O **número de membros** é exibido para cada guild

### Informações do Ranking

| Dado | Descrição |
|------|-----------|
| **Posição** | Classificação no ranking |
| **Guild** | Nome e emblema da guild |
| **Raça** | Raça da guild (com cor identificadora) |
| **Líder** | Nome do líder da guild |
| **Membros** | Quantidade total de membros |
| **Battle Score** | Pontuação de batalha (critério de ordenação) |

### Comparação entre Guilds

O ranking permite comparar guilds lado a lado, facilitando a análise de desempenho entre elas.

---

## Administração: Aba Guild Rewards

O admin pode configurar **recompensas automáticas** para guilds baseadas na posição no ranking.

### Tiers de Recompensa

As recompensas são organizadas por **tiers** (níveis), onde cada tier corresponde a uma faixa de posições no ranking:

| Configuração | Descrição |
|--------------|-----------|
| **Posição no ranking** | Define qual posição (1º, 2º, 3º, etc.) recebe a recompensa |
| **Itens/Prêmios** | O que será entregue (itens, cash, coins, etc.) |
| **Requisitos de stats** | Filtros mínimos para elegibilidade (ex: nível mínimo) |
| **Flag de recompensa única** | Garante que cada membro receba apenas uma vez |

### Funcionalidades de Recompensa

- **Recompensas por posição**: Configure prêmios diferentes para cada posição no ranking (1º lugar recebe mais que 2º, etc.)
- **Broadcast para todas as guilds**: Envie notificações ou recompensas para todas as guilds do servidor
- **Entrega condicional**: Defina condições que devem ser atendidas para a entrega da recompensa
- **Filtros por requisito de stats**: Exija stats mínimos dos membros para receberem a recompensa
- **Flags de recompensa única**: Evite que um membro receba a mesma recompensa mais de uma vez
- **Bônus para novos membros**: Configure recompensas especiais para membros recém-ingressados
- **Período e cooldown**: Defina a periodicidade das recompensas e o tempo de espera entre entregas

### Configurando Recompensas

1. Acesse **Admin > Guild Rewards** no painel administrativo
2. Crie um novo tier de recompensa
3. Defina a **posição ou faixa de posições** no ranking
4. Configure os **prêmios** para esse tier
5. (Opcional) Defina **requisitos de stats** e **condições de entrega**
6. (Opcional) Ative **flags de recompensa única** ou **bônus para novos membros**
7. Configure o **período** e **cooldown** desejado
8. Salve as configurações

---

## Próximos Passos

- [Ranking e Battle Pass](battlepass-gamecp) — Sistema de Battle Pass com progressão
- [Leilão](leilao) — Mercado de itens entre jogadores
- [Inventário](inventory) — Visualização de inventário dos personagens
