---
title: Sistema de Inventário
description: Visualização de inventário, itens equipados e busca de itens
layout: default
category: modulos
order: 4
---

# Sistema de Inventário

O Inventário permite que jogadores **visualizem os itens de seus personagens** diretamente pelo GameCP, com exibição detalhada de grades, raridades e tooltips.

---

## Visão Geral

| Recurso | Descrição |
|---------|-----------|
| **Visualização** | Grid visual dos itens do personagem |
| **Itens Equipados** | Exibição dos itens atualmente equipados |
| **Grades/Raridade** | Cores indicando a raridade do item |
| **Tooltips** | Detalhes completos ao passar o mouse |
| **Ícones** | Sprite Sheet para renderização dos ícones |
| **Admin** | Busca e envio de itens para jogadores |

---

## Requisitos

> **Importante**: Para visualizar o inventário, o **personagem deve estar offline** (desconectado do jogo). Se o personagem estiver online, o GameCP bloqueia o acesso ao inventário.

---

## Visualização do Inventário

### Acessando

1. Faça login no GameCP
2. Clique em **"Inventário"** no menu
3. Selecione o **personagem** desejado
4. Aguarde o carregamento dos itens

### Layout CSS Grid

O inventário é exibido em um **layout de grid** que replica a organização visual do inventário do jogo:

- **Slots organizados** em formato de grade
- **Itens equipados** exibidos em posições fixas (capacete, armadura, arma, etc.)
- **Inventário geral** com os demais itens em slots sequenciais

### Itens Equipados

Os itens equipados são exibidos em destaque, mostrando cada slot de equipamento:

| Slot | Descrição |
|------|-----------|
| **Arma** | Arma principal equipada |
| **Escudo/Off-hand** | Item na mão secundária |
| **Capacete** | Proteção de cabeça |
| **Armadura** | Proteção do corpo |
| **Luvas** | Proteção das mãos |
| **Botas** | Proteção dos pés |
| **Acessórios** | Anéis, colares, etc. |

### Cores de Grade/Raridade

Cada item possui uma **cor de borda** que indica sua raridade:

| Cor | Grade | Significado |
|-----|-------|-------------|
| **Branco** | Normal | Item comum |
| **Verde** | Incomum | Item com bônus leve |
| **Azul** | Raro | Item com bônus moderado |
| **Roxo** | Épico | Item com bônus elevado |
| **Dourado** | Lendário | Item com bônus máximo |

> As cores e grades podem variar conforme a configuração do servidor.

### Tooltips de Itens

Ao passar o mouse sobre um item, um **tooltip** é exibido com informações detalhadas:

- Nome do item
- Tipo e categoria
- Nível mínimo para uso
- Atributos e bônus
- Upgrades aplicados
- Gems inseridas (se houver)
- Quantidade (para itens empilháveis)

---

## Sprite Sheet (Ícones dos Itens)

Os ícones dos itens são renderizados a partir de uma **Sprite Sheet** — uma imagem única contendo todos os ícones do jogo.

### Como Funciona

1. O GameCP utiliza uma Sprite Sheet configurada pelo admin
2. Cada item possui coordenadas (posição X/Y) na Sprite Sheet
3. O CSS posiciona a Sprite Sheet para exibir o ícone correto de cada item
4. Isso otimiza o carregamento (uma única imagem em vez de centenas)

> Para mais detalhes sobre configuração da Sprite Sheet, veja o tutorial [Sprite Sheet](sprite-sheet).

---

## Administração: Busca e Envio de Itens

O admin possui funcionalidades avançadas para gerenciamento de itens.

### Busca de Itens

1. Acesse **Admin > Inventário** no painel administrativo
2. Utilize a **barra de busca** para encontrar itens por nome ou código
3. Visualize os resultados com detalhes do item

### Envio de Itens

O admin pode enviar itens diretamente para jogadores:

1. Busque o item desejado no sistema
2. Selecione o **jogador/personagem** destinatário
3. Defina a **quantidade** a ser enviada
4. Confirme o envio

> Os itens enviados pelo admin são registrados no histórico para auditoria.

---

## Próximos Passos

- [Sprite Sheet](sprite-sheet) — Configuração dos ícones de itens
- [Leilão](leilao) — Registre itens do inventário no leilão
- [GameCP Coins](gamecp-coins) — Moeda virtual do GameCP
