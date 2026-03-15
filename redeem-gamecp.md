---
title: Redeem (Resgates)
description: Como gerenciar o sistema de resgates antecipados no painel admin
layout: default
category: admin
order: 15
---

# Redeem (Resgates Antecipados)

O sistema de resgates permite gerenciar pacotes de pré-venda. Jogadores que compraram antes do servidor abrir podem resgatar seus itens escolhendo a raça.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Resgates**

---

## Como Funciona

1. O jogador compra um pacote na pré-venda (antes do servidor abrir)
2. O sistema armazena o pacote vinculado ao login
3. Quando o servidor abre, o jogador acessa o GameCP e resgata escolhendo a raça (ACC, BELL ou CORA)
4. O sistema entrega o produto correspondente à raça escolhida

---

## Ativar/Desativar Resgates

1. Na seção superior, use o toggle **"Ativar resgates para jogadores"**
2. Salve

---

## Configurar Produtos por Raça

Para cada faixa de preço, você precisa configurar qual produto WooCommerce será entregue por raça.

### Adicionar nova configuração

1. Clique em **"Adicionar Novo"**
2. Preencha:

| Campo | O que preencher |
| --- | --- |
| **Valor** | Preço do pacote (ex: 50.00) |
| **Moeda** | Selecione: BRL, USD ou EUR |
| **Produto ACC** | Selecione o produto WooCommerce para raça Accretia |
| **Produto BELL** | Selecione o produto WooCommerce para raça Bellato |
| **Produto CORA** | Selecione o produto WooCommerce para raça Cora |

3. Clique em **"Adicionar"**

### Excluir uma configuração

Clique no botão de **excluir** na tabela de configurações existentes.

---

## Gerenciar Pacotes dos Jogadores

Na seção **"Pacotes Antecipados"**, você pode ver e gerenciar os pacotes individuais:

1. Use o campo de busca para filtrar por **login**
2. A tabela exibe: Login, Valor, Quantidade, Order ID, Data, Status (usado ou não)
3. Para excluir pacotes, marque os checkboxes desejados
4. Selecione **"Excluir selecionados"** no dropdown de ações
5. Clique em **"Aplicar"**

> Use o checkbox **"Selecionar Todos"** para marcar todos os pacotes da página atual.

---

## Próximos Passos

- [New Player](newplayer) — Recompensas para novos jogadores
- [Loja e Checkout](gamecp-shop-checkout) — Compras integradas com WooCommerce
- [Quests](quests) — Criar missões com recompensas
