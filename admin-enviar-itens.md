---
title: Enviar Itens
description: Como enviar itens para personagens pelo painel admin
layout: default
category: admin
order: 21
---

# Enviar Itens

Permite enviar itens diretamente para um personagem específico ou para **todos os personagens** do servidor de uma vez.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Enviar Itens**

---

## Enviar para um Personagem Específico

1. No campo **"Nome do Personagem"**, digite o nome do char
2. Clique em **"Acessar"** (ou pressione Enter)
3. O sistema valida o personagem e mostra o histórico de envios anteriores
4. Na seção **"Configuração do Item"**, preencha:

| Campo | O que preencher |
| --- | --- |
| **Código Item** | Digite o código do item ou busque pelo nome (autocomplete) |
| **Talics** | Selecione a talic no dropdown e clique em **"+"** para adicionar. Use **"-"** para remover a última |
| **Quantidade** | Quantidade do item (1-255) |
| **Tempo** | Tempo de aluguel em horas (0 = permanente) |

5. Para enviar **múltiplos itens**, clique em **"Adicionar Linha"**
6. Use os botões de ação em cada linha:
   - **Duplicar** — copia a linha (se for armadura, oferece criar o set completo automaticamente)
   - **Mover ↑ / ↓** — reordena as linhas
   - **Remover** — exclui a linha
7. No campo **"Motivo"**, descreva o motivo do envio (obrigatório)
8. Clique em **"Enviar Item"**

---

## Enviar para Todos os Personagens

1. Marque o toggle **"Enviar para Todos os Personagens"**
2. O campo de nome some e o botão muda para vermelho
3. Configure os itens normalmente
4. Preencha o **motivo**
5. Clique em **"Enviar para Todos"**
6. Confirme no popup de confirmação

> **Atenção:** Envio em massa exclui GMs automaticamente e **não pode ser desfeito**.

---

## Gerar Set de Armadura Automaticamente

Ao duplicar uma linha com código de armadura (ex: `ihbom01`), o sistema detecta o padrão e oferece criar as outras partes do set automaticamente (ih, iu, il, ig, is).

1. Preencha o código de uma peça de armadura
2. Clique no botão **duplicar**
3. No popup, clique em **"Sim, criar partes"** para gerar todas as partes do set

---

## Próximos Passos

- [Pesquisar Itens](search-items) — Buscar itens no banco de dados
- [Cash e Premium](cash-premium) — Gerenciar cash e premium
- [Histórico de Logs](history-logs) — Ver logs de ações
