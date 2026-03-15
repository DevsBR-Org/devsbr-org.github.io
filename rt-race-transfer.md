---
title: Race Transfer
description: Como transferir a raça de um personagem pelo painel admin
layout: default
category: administracao
order: 17
---

# Race Transfer (Transferência de Raça)

O Race Transfer permite transferir um personagem de uma raça/classe para outra, convertendo automaticamente todos os itens equipados e do inventário.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Race Transfer**

---

## Passo a Passo Completo

### Etapa 1 — Buscar o Personagem

1. No campo de busca, digite o **nome** ou **serial** do personagem
2. Clique em **"Buscar"** ou pressione Enter
3. Selecione o personagem nos resultados

### Etapa 2 — Escolher Nova Raça e Classe

Após selecionar o personagem, o sistema exibe as informações atuais (nome, level, raça, classe).

1. No campo **"Nova Raça"**, selecione a raça destino:
   - Bellato Masculino / Feminino
   - Cora Masculino / Feminino
   - Accretia
2. No campo **"Nova Classe Base"**, selecione a classe desejada (as opções mudam conforme a raça)
3. No campo **"Tipo de Armadura"**, selecione o tipo (ex: armadura Ranger para classe Force)
4. Clique em **"Gerar Pré-visualização"**

### Etapa 3 — Revisar e Confirmar

O sistema exibe uma comparação lado a lado:

| Coluna | O que mostra |
| --- | --- |
| **Antes** | Itens equipados e inventário atuais |
| **Depois** | Itens convertidos para a nova raça |

1. **Revise** todos os itens convertidos
2. Se necessário, **edite manualmente** um item clicando nele na coluna "Depois"
3. Para edição em massa, use o botão **"Edição em Massa"**
4. Preencha o campo **"Motivo da Transferência"** (obrigatório)
5. Clique em **"Confirmar Transferência"**

---

## Edição Manual de Itens

Ao clicar em um item na coluna "Depois":

1. O modal mostra o item original e sugestões de conversão
2. No campo **"Novo Código"**, altere o código do item (com autocomplete)
3. Ajuste a quantidade e talics se necessário
4. Confirme a edição

---

## Edição em Massa

O modal de edição em massa exibe uma tabela com todos os itens:

- **Original** — item antes da conversão
- **Convertido** — item após a conversão
- **Quantidade** e **Ações** — para editar cada item individualmente

---

## Próximos Passos

- [Painel Admin](gamecp-admin-panel) — Visão geral do painel admin
- [Cash e Premium](cash-premium) — Gerenciar cash e premium
- [Histórico de Logs](history-logs) — Ver logs de ações administrativas
