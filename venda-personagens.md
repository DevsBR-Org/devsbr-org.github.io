---
title: Venda de Personagens
description: Sistema de venda de personagens entre jogadores via WooCommerce
layout: default
category: modulos
order: 11
---

# Venda de Personagens

O sistema de Venda de Personagens permite que jogadores **listem seus personagens para venda**, com criação automática de produto WooCommerce e transferência automática após o pagamento.

---

## Visão Geral

| Recurso | Descrição |
|---------|-----------|
| **Listagem** | Jogadores anunciam personagens para venda |
| **Preço** | Definido pelo vendedor |
| **Produto** | Criação automática no WooCommerce |
| **Pagamento** | Via checkout WooCommerce |
| **Transferência** | Automática após confirmação de pagamento |
| **Admin** | Aba de gerenciamento de vendas |
| **Versão** | Adicionado na v1.5.9 |

---

## Como Funciona (Vendedor)

### Listando um Personagem para Venda

1. Faça login no GameCP
2. Acesse a opção de **Venda de Personagens**
3. Selecione o **personagem** que deseja vender
4. Defina o **preço** desejado
5. Confirme a listagem

### O que acontece ao listar

- O personagem é **bloqueado** para uso enquanto estiver à venda
- Um **produto WooCommerce** é criado automaticamente com os dados do personagem
- O personagem aparece na página de **personagens à venda** (auction-chars) para outros jogadores

### Requisitos e Restrições

| Requisito | Descrição |
|-----------|-----------|
| **Conta offline** | A conta do vendedor não pode estar logada no jogo |
| **Personagem elegível** | Nem todos os personagens podem ser vendidos (regras do admin) |
| **Preço válido** | O preço deve respeitar limites mínimos/máximos (se configurados) |
| **Um anúncio por vez** | Restrições de listagens simultâneas podem ser aplicadas |

---

## Como Funciona (Comprador)

### Navegando Personagens à Venda

1. Acesse a página de **personagens à venda** (auction-chars)
2. Navegue pela lista de personagens disponíveis
3. Visualize as **estatísticas** de cada personagem (nível, classe, raça, equipamentos)
4. Escolha o personagem desejado

### Comprando um Personagem

1. Clique no personagem para ver os **detalhes completos**
2. Revise as stats, equipamentos e preço
3. Clique em **"Comprar"** para adicionar ao carrinho WooCommerce
4. Complete o **checkout** normalmente (cartão, PIX, boleto, etc.)
5. Após a **confirmação do pagamento**, o personagem é transferido automaticamente

### Transferência Automática

Após o pagamento ser confirmado:

- O personagem é **removido da conta do vendedor**
- O personagem é **adicionado à conta do comprador**
- O produto WooCommerce é marcado como **concluído**
- Ambas as partes recebem confirmação da transação

---

## Administração

### Aba de Gerenciamento

O admin possui uma aba dedicada para gerenciar vendas de personagens:

1. Acesse **Admin > Venda de Personagens** no painel
2. Visualize todas as listagens ativas, pendentes e concluídas

### Funcionalidades do Admin

| Ação | Descrição |
|------|-----------|
| **Visualizar listagens** | Ver todos os personagens à venda |
| **Cancelar venda** | Remover um personagem da listagem |
| **Verificar transações** | Acompanhar o status de vendas em andamento |
| **Histórico** | Consultar vendas concluídas |

### Configurações

O admin pode definir:

- Se o módulo de venda está **ativo ou inativo**
- **Restrições** de quais personagens podem ser vendidos
- **Regras de preço** (mínimo/máximo)
- **Taxas** sobre a venda (se aplicável)

---

## Fluxo Completo

```
Vendedor lista personagem → Produto WooCommerce criado →
Comprador visualiza na página auction-chars → Comprador faz checkout →
Pagamento confirmado → Personagem transferido automaticamente
```

---

## Próximos Passos

- [Leilão](leilao) — Mercado de itens (diferente da venda de personagens)
- [Loja e Checkout](gamecp-shop-checkout) — Como funciona o checkout WooCommerce
- [Inventário](inventory) — Visualize os itens do personagem antes de comprar
