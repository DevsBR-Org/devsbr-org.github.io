---
title: Sistema New Player
description: Campanhas de boas-vindas para novos jogadores
layout: default
category: modulos
order: 6
---

# Sistema New Player

O New Player e um sistema de **campanhas de boas-vindas** para incentivar novos jogadores com recompensas especiais. O admin configura campanhas com metas, restricoes de elegibilidade e kits iniciais; o jogador acompanha seu progresso e resgata premios pelo GameCP.

---

## Visao Geral

| Recurso              | Descricao                                         |
| -------------------- | ------------------------------------------------- |
| **Campanhas**        | Configuraveis pelo admin com nome, descricao e status |
| **Metas**            | Level, tempo de jogo, PvP, Dalant, etc.            |
| **Recompensas**      | Itens organizados por categoria (starter gear)      |
| **Elegibilidade**    | Restricoes por data de criacao, level, HWID         |
| **Agendamento**      | Campanhas com status ativo/inativo                  |
| **Rastreamento**     | Controle de resgate por campanha + personagem       |

---

## Visao do Jogador

### Acessando o New Player

1. Faca login no GameCP.
2. Clique em **"New Player"** no menu.
3. Se nao houver campanha ativa, o jogador e redirecionado ao Dashboard.

### Tela do Jogador

A tela possui tres blocos:

| Bloco                     | Descricao                                      |
| ------------------------- | ---------------------------------------------- |
| **Cabecalho da campanha** | Nome e descricao configurados pelo admin        |
| **Seletor de personagem** | Lista de personagens elegiveis com progresso    |
| **Detalhes**              | Recompensas (esquerda) e metas (direita)        |

### Seletor de Personagem

- Exibe **apenas personagens elegiveis** conforme as restricoes.
- Cada card mostra: nome, raca, level e barra de progresso (ex.: "3/5 metas").
- Ao clicar, carrega recompensas e metas daquele personagem.
- Se nenhum personagem for elegivel, aparece aviso informativo.

### Recompensas (Starter Gear)

Cada recompensa e exibida em um card com:

- Icone do item (via Sprite Sheet).
- Nome, codigo e quantidade.
- Tempo de aluguel em dias (quando aplicavel).
- Talics configurados.

### Estados do Botao de Resgate

| Estado                  | Descricao                                      |
| ----------------------- | ---------------------------------------------- |
| **"Resgatar"**          | Todas as metas completas, recompensa disponivel |
| **"Resgatado"**         | Personagem ja resgatou (card esmaecido)         |
| **"Complete as metas"** | Metas pendentes, botao desativado               |

> O controle de resgate e sempre por **campanha + personagem**. Um mesmo login pode ter varios personagens elegiveis.

### Progresso das Metas

Para cada meta, o jogador ve:

- Icone **verde** quando a condicao esta atendida.
- Icone **vermelho** quando falta cumprir.
- Texto explicativo (ex.: "Level minimo 40 - seu personagem esta no 32").
- Barra visual com porcentagem de progresso.

Quando todas as metas ficam verdes, o selo **"Completo!"** aparece e os botoes de resgate sao liberados.

---

## Visao do Administrador

### Acesso

1. Acesse o GameCP como administrador.
2. Entre em **Admin > New Player**.
3. Requer permissao de **"manage_settings"**.

### Tela Admin

| Bloco                  | Descricao                                      |
| ---------------------- | ---------------------------------------------- |
| **Lista de campanhas** | Coluna esquerda com nome, data e status         |
| **Editor de campanha** | Coluna direita com dados e restricoes           |
| **Recompensas**        | Parte inferior da coluna direita                |

---

## Criando uma Campanha

1. Clique em **"Nova"** na lista de campanhas.
2. Preencha os dados:

| Campo          | Descricao                                       |
| -------------- | ----------------------------------------------- |
| **Nome**       | Nome exibido ao jogador                          |
| **Status**     | Switch ativo/inativo (agendamento)               |
| **Descricao**  | Texto no cabecalho para jogadores                |

3. Clique em **"Salvar Campanha"**.

Para excluir, selecione a campanha e clique em **"Excluir"**.

---

## Configurando Restricoes de Elegibilidade

No card **"Restricoes"**, ative e configure cada meta:

| Restricao                    | Descricao                                      |
| ---------------------------- | ---------------------------------------------- |
| **Data de Criacao**          | Personagem criado a partir de determinada data  |
| **Level Minimo**             | Nivel minimo exigido                            |
| **PvP Point Minimo**         | Pontos de PvP acumulados                        |
| **Tempo de Jogo (minutos)**  | Baseado no LogPlay do personagem                |
| **Dalant Minimo**            | Quantidade minima de Dalant                     |
| **Processing Point**         | ActionPoint_0 minimo                            |
| **Hunting Point**            | ActionPoint_1 minimo                            |
| **Gold Point**               | ActionPoint_2 minimo                            |

Cada restricao possui um checkbox para ativar/desativar e um campo de valor. Clique em **"Salvar Campanha"** apos ajustar.

---

## Configurando Recompensas (Starter Gear)

Com uma campanha selecionada, na secao **"Recompensas"**:

1. Clique em **"Adicionar Item"**.
2. Configure cada recompensa:

| Campo          | Descricao                                       |
| -------------- | ----------------------------------------------- |
| **Codigo**     | Codigo do item no banco                          |
| **Quantidade** | Numero de unidades                               |
| **Tempo**      | Aluguel em dias (0 = permanente)                 |
| **Talics**     | IDs de talics exibidas como icones               |

3. Reordene arrastando o icone de drag.
4. Clique em **"Salvar Recompensas"**.

---

## Rastreamento de Resgates (Claim Tracking)

O sistema registra cada resgate com:

- **Campanha** associada.
- **Personagem** que resgatou.
- **Data/hora** do resgate.
- **Itens** entregues.

O admin pode consultar esses registros para auditoria. O sistema impede resgates duplicados por personagem.

---

## Como o Sistema Decide Elegibilidade

1. Carrega a **campanha ativa**.
2. Busca personagens da conta e aplica as **restricoes**.
3. Apenas personagens que passam nos filtros aparecem na lista.
4. Calcula metas validas vs. pendentes para cada personagem.
5. No momento do resgate, revalida tudo antes de entregar.

---

## Boas Praticas

- Comece com campanhas simples (level minimo + tempo de jogo).
- Use a restricao de **data de criacao** para separar novos jogadores de personagens antigos.
- Configure **starter gear** equilibrado que ajude sem desequilibrar a economia.
- Combine com Quests e Battlepass para uma experiencia completa de onboarding.
- Monitore resgates nos primeiros dias para validar que as restricoes estao adequadas.
