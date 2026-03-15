---
title: Roleta de Premios (Spin Wheel)
description: Sistema de roleta com premios configuraveis
layout: default
category: modulos
order: 9
---

# Roleta de Premios (Spin Wheel)

O Spin Wheel e uma **roleta interativa** onde jogadores pagam para girar e ganhar premios. O custo pode ser em cash do servidor ou GameCP Coins, e cada premio tem probabilidade configuravel pelo admin.

---

## Visao Geral

| Recurso              | Descricao                                       |
| -------------------- | ----------------------------------------------- |
| **Tipo**             | Roleta visual interativa                         |
| **Custo por giro**   | Cash do servidor ou GameCP Coins                 |
| **Premios**          | Itens, cash, premium e mais                      |
| **Probabilidades**   | Peso configuravel por premio                     |
| **Itens raros**      | Marcacao especial para premios raros              |
| **Limites**          | Giros por dia/periodo                            |

---

## Configuracao (Admin)

### Acessando

1. Faca login como admin no GameCP.
2. Acesse **Admin > Spin Wheel**.

### Configuracoes Gerais

| Opcao               | Descricao                                       |
| -------------------- | ----------------------------------------------- |
| **Custo por giro**   | Valor cobrado por cada giro                      |
| **Tipo de custo**    | **Cash** do servidor ou **GameCP Coins**         |
| **Giros gratuitos**  | Quantidade de giros gratis por dia (opcional)    |
| **Cooldown**         | Tempo minimo entre giros                         |
| **Ativo**            | Habilitar ou desabilitar o modulo                |

### Configurando Premios

Para cada premio na roleta, configure:

| Campo           | Descricao                                        |
| --------------- | ------------------------------------------------ |
| **Nome**        | Nome exibido no segmento da roleta                |
| **Tipo**        | Item, Cash ou Premium                             |
| **Codigo**      | Codigo do item (quando tipo = Item)               |
| **Quantidade**  | Quantos itens/cash serao entregues                |
| **Peso**        | Probabilidade relativa (quanto maior, mais chance)|
| **Raro**        | Marcar como item raro (destaque visual)           |
| **Cor**         | Cor do segmento na roleta                         |

### Tipos de Recompensa

| Tipo         | Descricao                                         |
| ------------ | ------------------------------------------------- |
| **Item**     | Item do jogo entregue ao personagem                |
| **Cash**     | Moeda de cash creditada na conta                   |
| **Premium**  | Beneficio premium (VIP, tempo de premium, etc.)    |

### Sistema de Probabilidades por Peso

O Spin Wheel utiliza **pesos relativos**, nao porcentagens fixas. O sistema calcula a chance de cada premio com base no peso em relacao ao total.

**Exemplo de configuracao:**

| Premio          | Peso | Chance Calculada |
| --------------- | ---- | ---------------- |
| Pocao HP x10    | 40   | 40%              |
| Arma Rara       | 5    | 5%               |
| Cash 500        | 25   | 25%              |
| Armadura Epica  | 3    | 3%               |
| Premium 7 dias  | 2    | 2%               |
| Cash 100        | 25   | 25%              |
| **Total**       | **100** | **100%**      |

### Marcacao de Item Raro

Premios marcados como **raro** recebem destaque visual na roleta (brilho, cor diferenciada). Isso cria expectativa nos jogadores e valoriza premios especiais.

---

## Visao do Jogador

### Acessando a Roleta

1. Faca login no GameCP.
2. Clique em **"Roleta"** ou **"Spin Wheel"** no menu.
3. Visualize os premios disponiveis nos segmentos.

### Fluxo de Giro

1. **Verificar custo**: o valor em cash ou GameCP Coins e exibido no botao.
2. **Verificar saldo**: o sistema confere se o jogador tem saldo suficiente.
3. **Girar**: clique no botao **"Girar"**.
4. **Animacao**: a roleta gira e para no premio sorteado.
5. **Receber premio**: o item/cash/premium e entregue automaticamente ao personagem.
6. **Saldo atualizado**: o custo e debitado do saldo do jogador.

### Premios Raros

Quando o jogador ganha um item marcado como raro, a interface exibe uma animacao especial de destaque.

### Giros Gratuitos

Se configurados pelo admin, giros gratuitos sao renovados diariamente. O jogador ve a quantidade restante na tela.

---

## Boas Praticas

- **Balanceie os pesos** para manter a economia saudavel.
- **Limite giros diarios** para evitar inflacao de itens.
- **Varie os premios** regularmente para manter o interesse.
- **Use a marcacao de raro** com moderacao para criar valor.
- **Defina o custo** de forma que seja acessivel, mas nao trivial.
- **Monitore estatisticas** de giros e premios entregues para ajustar pesos.
