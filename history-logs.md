---
title: Historico de Logs
description: Auditoria de itens via API do ZoneServer
layout: default
category: administracao
order: 3
---

# Historico de Logs (History Logs)

Ferramenta de **auditoria de itens** que consulta e interpreta logs do ZoneServer (arquivos `.his`). Permite rastrear o caminho de qualquer item e investigar a economia do servidor com filtros avancados.

---

## Visao Geral

| Tipo de Evento  | Descricao                |
| --------------- | ------------------------ |
| **TRADE**       | Trocas entre jogadores   |
| **SELL**        | Vendas para NPC          |
| **BUY**         | Compras de NPC           |
| **DUMP**        | Itens descartados        |
| **TRUNK**       | Movimentos de bau        |
| **PICK UP**     | Itens coletados (loot)   |
| **REWARD**      | Recompensas de sistemas  |
| **READ_CASH**   | Leituras de cash/saldo   |

---

## Acesso

A aba **"Historico de Itens"** fica em **Admin > Historico de Itens** no GameCP.

### Requisitos

- Conta logada como **admin** com permissao **"manage_settings"**.
- Modulo **History Logs** ativado nas opcoes.
- URL da **API RF Logs** configurada em **DevsBR > ZoneServer**.

---

## Formulario de Busca com Filtros Avancados

### Campos de Filtro

| Campo           | Descricao                                        |
| --------------- | ------------------------------------------------ |
| **Buscar**      | Nick ou serial do personagem (com autocomplete)   |
| **Tipo**        | Busca por **Nick** ou **Serial**                  |
| **Eventos**     | Selecao de tipos de evento (checkboxes)           |
| **Data**        | Data do dia para busca                            |
| **De / Ate**    | Intervalo de horario (horas cheias + 23:59)       |

### Filtro por Tipo de Evento

O dropdown de eventos permite selecionar quais tipos incluir:

| Evento           | Descricao                                       |
| ---------------- | ----------------------------------------------- |
| **Troca**        | Logs de TRADE entre personagens                  |
| **Venda**        | Vendas de itens para NPC/loja                    |
| **Compra**       | Compras de itens                                 |
| **Jogar Fora**   | Itens descartados no chao                        |
| **Bau**          | Movimentacoes envolvendo o bau                   |
| **Loot**         | Itens coletados do chao (drop de mobs)           |
| **Recompensa**   | Itens recebidos de sistemas                      |
| **Read Cash**    | Leituras de cash/saldo                           |

Botoes auxiliares: **"Selecionar Todos"** e **"Limpar Todos"**. Se nenhum estiver marcado, todos sao considerados.

### Filtro por Periodo

- **Data**: selecione o dia especifico.
- **De / Ate**: defina o intervalo de horario dentro do dia.
- O sistema valida que a hora final seja maior que a inicial.

### Busca por Personagem

- Digite o **nick** ou **serial** do personagem.
- O campo possui **autocomplete** para facilitar a busca.
- Selecione o tipo (Nick ou Serial) conforme o dado disponivel.

---

## Resultados da Busca

Apos enviar o formulario:

### Resumo

- Total de logs encontrados.
- **Badges por tipo de evento** com contagem individual.
- Aviso de **"Limite atingido"** se houver muitos registros.

### Organizacao dos Resultados

Os logs sao exibidos em **acordeao** com tres niveis:

| Nivel               | Descricao                                      |
| ------------------- | ---------------------------------------------- |
| **Por Tipo**        | Bloco com cabecalho colorido e icone            |
| **Por Hora**        | Agrupamento por faixa de horario                |
| **Por Entrada**     | Card individual com detalhes do evento          |

### Detalhes de Cada Log

Cada card de log exibe:

| Informacao        | Descricao                                       |
| ----------------- | ----------------------------------------------- |
| **Personagem**    | Nome do personagem envolvido                     |
| **Serial**        | Serial do personagem                             |
| **IP**            | IP de origem                                     |
| **Itens**         | Itens movimentados com icone, nome e quantidade  |
| **Direcao**       | Ganho (+) ou perdido (-) com cores diferentes    |
| **Talics**        | Upgrades e slots do item                         |

Para eventos **PICK UP**, o sistema agrupa pickups consecutivos do mesmo personagem em um unico card.

---

## Busca de Item por Serial

Alem da busca por personagem, o admin pode buscar pelo **serial de um item** especifico para rastrear toda a cadeia de movimentacoes (quem pegou, trocou, vendeu, descartou).

---

## Exemplos de Uso Pratico

### Investigar Duplicacao de Itens

1. Busque pelo **serial do personagem suspeito**.
2. Filtre por **TRADE**, **PICK UP** e **REWARD**.
3. Procure padroes de recebimento de grandes quantidades em pouco tempo.

### Rastrear Sumico de Item

1. Busque pelo **nick do jogador** na data da ocorrencia.
2. Marque **TRADE**, **TRUNK** e **DUMP**.
3. Verifique se o item foi trocado, guardado no bau ou descartado.

### Acompanhar Economia

1. Use filtros de **SELL** e **BUY**.
2. Analise quais itens sao mais negociados.
3. Combine com dados de Wallet e Leilao.

---

## Mensagens de Erro Comuns

| Mensagem                                        | Solucao                                    |
| ----------------------------------------------- | ------------------------------------------ |
| "URL da API RF Logs nao configurada"             | Preencha em DevsBR Panel > ZoneServer       |
| Erro de conexao com a API                        | Verifique firewall, porta e endpoint        |
| "A hora final deve ser maior que a hora inicial" | Ajuste o intervalo de horario               |
| "Nenhum log encontrado"                          | Amplie o periodo ou inclua mais eventos     |

---

## Boas Praticas

- Use como **ferramenta de auditoria**, nao como monitor em tempo real.
- Prefira **intervalos curtos** (1-2 horas) para buscas mais rapidas.
- Combine com dados de **Wallet**, **Leilao** e **Loja** para panorama completo.
- Ao compartilhar prints com jogadores, **oculte IPs** e dados sensiveis.
- Evite buscas grandes em horarios de pico do servidor.
