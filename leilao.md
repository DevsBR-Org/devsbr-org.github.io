---
title: Sistema de Leilão
description: Mercado entre jogadores com preço fixo e venda de personagens
layout: default
category: modulos
order: 5
---

# Sistema de Leilão

O Leilão é um **mercado público** entre jogadores, integrado ao GameCP. Inclui venda de itens com preço fixo e, desde a v1.5.9, **venda de personagens** com transferência automática.

---

## Visão Geral

| Recurso | Descrição |
| --- | --- |
| **Tipo** | Preço fixo (sem lances) |
| **Vendedor** | Recebe em Wallet (menos taxa) |
| **Comprador** | Paga via checkout WooCommerce |
| **Taxa** | Configurada pelo admin (ex: 10%) |
| **Itens** | Venda de itens do inventário |
| **Personagens** | Venda de personagens inteiros (v1.5.9+) |

> O leilão é de **preço fixo**. Não existe sistema de lances.

---

## Menu do Leilão

- **Explorar**: Ver e comprar itens anunciados por outros jogadores
- **Meus Leilões**: Gerenciar seus itens e personagens à venda
- **Personagens** (auction-chars): Marketplace de personagens à venda

---

## Leilão de Itens

### Como Anunciar um Item

1. Acesse o **GameCP** com sua conta
2. Vá até o menu **Inventário**
3. Escolha o **personagem** cujo inventário deseja visualizar
4. Procure o item que deseja vender
5. Clique no **botão de leilão** (ícone de etiqueta) no item desejado
6. No modal de registro, você verá:
   - Nome, tipo, nível, grade e quantidade do item
   - Upgrades e gems (quando existirem)
   - Campo de **preço** para definir o valor
   - **Taxa do leilão** exibida abaixo do campo de preço
7. Digite o preço desejado
8. Clique em **"Registrar"**
9. O item é removido do inventário e passa a constar no leilão

> Nem todos os itens podem ser listados. Itens bloqueados aparecem com ícone de cadeado.

> A conta **não pode estar logada no jogo** para registrar itens. O GameCP bloqueia a operação se a conta estiver online.

### Gerenciando Meus Leilões

Na tela **Leilão > Meus Leilões**, cada item mostra:

| Campo | Descrição |
| --- | --- |
| **Nome** | Nome do item |
| **Level mínimo** | Nível necessário para equipar |
| **Preço** | Valor definido pelo vendedor |
| **Status** | Estado atual do anúncio |
| **Ações** | Operações disponíveis |

### Status dos Itens

| Status | Descrição |
| --- | --- |
| **Ativo** | Disponível para compra |
| **Reservado** | Vinculado a um pedido em andamento |
| **Vendido** | Venda concluída, valor creditado na Wallet |
| **Cancelado** | Item retirado do leilão |
| **Pagamento Pendente** | Pedido aberto aguardando pagamento |

### Ações Disponíveis

| Ação | Quando disponível | Descrição |
| --- | --- | --- |
| **Editar preço** | Item ativo, sem pagamento pendente | Altera o valor do anúncio |
| **Retirar** | Item ativo, sem reserva | Remove do leilão e devolve ao inventário |
| **Reenviar** | Produto desvinculado | Recria o vínculo com a loja WooCommerce |

### Como Comprar Itens

1. Acesse **Leilão > Explorar**
2. Use os **filtros** para encontrar itens (tipo, level, grade, raça)
3. Clique em **"Comprar"** no item desejado
4. O item é adicionado ao **carrinho do GameCP**
5. Conclua o pedido pelos métodos de pagamento disponíveis
6. Após confirmação:
   - O **comprador recebe o item** via entrega automática
   - O **vendedor recebe o valor líquido** na Wallet (com taxa descontada)

---

## Venda de Personagens

Desde a **v1.5.9**, o leilão suporta a **venda de personagens inteiros** entre jogadores.

### Como Funciona

| Etapa | Descrição |
| --- | --- |
| **1. Listagem** | O vendedor lista um personagem para venda com preço definido |
| **2. Produto WooCommerce** | O sistema cria automaticamente um produto WooCommerce vinculado ao personagem |
| **3. Compra** | O comprador adquire o personagem via checkout WooCommerce |
| **4. Transferência** | Após pagamento confirmado, o personagem é transferido automaticamente para a conta do comprador |
| **5. Pagamento** | O vendedor recebe o valor líquido na Wallet |

### Passo a Passo para Vender um Personagem

1. Acesse o **GameCP** com sua conta
2. Vá até a seção de **Venda de Personagens** no menu de leilão
3. Selecione o **personagem** que deseja vender
4. Defina o **preço** de venda
5. Confirme a listagem
6. O sistema cria automaticamente um **produto WooCommerce** com os dados do personagem
7. O personagem aparece no marketplace para outros jogadores

### Requisitos para Venda de Personagem

- A conta **não pode estar logada no jogo**
- O personagem não pode estar em uso ativo
- O vendedor deve ter apenas o personagem selecionado disponível para venda (sem restrições administrativas)

### Para o Comprador

1. Navegue pelo marketplace de personagens no leilão
2. Visualize os detalhes do personagem (classe, nível, equipamentos)
3. Clique em **"Comprar"**
4. Conclua o pagamento via WooCommerce
5. O personagem é **transferido automaticamente** para sua conta

---

## Taxas e Saldo

O leilão cobra uma **taxa em porcentagem** sobre o valor de venda (tanto para itens quanto para personagens):

- A taxa é exibida no momento do registro
- Após a venda, o sistema:
  1. Calcula o valor **bruto** (preço definido pelo vendedor)
  2. Aplica a **taxa do leilão**
  3. Credita na **Wallet** apenas o valor **líquido**

O saldo na Wallet pode ser usado em qualquer área do GameCP que aceite carteira como pagamento.

---

## Visão para Administradores

Na aba **Auction** do painel admin, o administrador pode:

- Consultar **todos os itens e personagens** registrados no leilão
- Filtrar por: login, personagem, raça, status, nível, grade, faixa de preço
- Visualizar quantidade total, paginação e data de criação
- Auditar vendas de personagens e transferências realizadas

Essa tela é voltada para **auditoria e acompanhamento**, ajudando a identificar itens suspeitos, padrões de uso e possíveis abusos.

---

## Boas Práticas

- Verifique se a **conta está offline** no jogo antes de registrar ou retirar itens
- Defina preços razoáveis — valores extremos podem indicar abuso ou ficar parados
- Use o leilão para movimentar a economia do servidor de forma saudável
- Na venda de personagens, certifique-se de que todos os itens do personagem estão em ordem antes de listar

---

## Tutoriais Relacionados

- [Carteira (Wallet)](wallet)
- [Loja e Checkout](gamecp-shop-checkout)
- [Inventário](inventory)
- [Painel Admin](gamecp-admin-panel)
- [Venda de Personagens](venda-personagens)
