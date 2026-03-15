---
title: Loja e Checkout
description: Integracao com WooCommerce dentro do GameCP
layout: default
category: modulos
order: 2
---

# Loja e Checkout

A Loja do GameCP oferece uma **interface integrada** ao WooCommerce para compras sem sair do painel. O jogador navega por categorias, adiciona itens ao carrinho e finaliza com diversos metodos de pagamento, incluindo desconto via Wallet.

---

## Visao Geral

| Recurso              | Descricao                                       |
| -------------------- | ----------------------------------------------- |
| **Produtos**         | Cadastrados no WooCommerce                       |
| **Interface**        | Loja propria dentro do GameCP                    |
| **Filtros**          | Navegacao por categorias                         |
| **Layout**           | Colunas configuraveis (3 a 6)                    |
| **Carrinho**         | Adicao, remocao e ajuste de quantidades          |
| **Checkout**         | Finalizacao integrada com WooCommerce            |
| **Pagamentos**       | Todos os gateways configurados no WooCommerce    |
| **Wallet**           | Desconto via saldo da carteira GameCP            |
| **Entrega**          | Automatica no servidor do jogo                   |

O GameCP nao substitui o WooCommerce; ele **usa o WooCommerce por tras**.

---

## Visao do Jogador

### Navegando na Loja

1. Faca login no GameCP.
2. Clique em **"Loja"** no menu.
3. Navegue pelos produtos disponiveis.

### Filtros por Categoria

- A loja exibe filtros por **categoria de produto** (ex.: Itens, Cash, VIP, Pacotes).
- O jogador clica na categoria desejada para filtrar os produtos exibidos.
- E possivel ver todos os produtos ou filtrar por categoria especifica.

### Layout de Colunas

O admin pode configurar o numero de colunas de exibicao:

| Colunas | Melhor Para                                      |
| ------- | ------------------------------------------------ |
| **3**   | Produtos com descricoes detalhadas                |
| **4**   | Balanco entre visual e informacao                 |
| **5**   | Muitos produtos, visual compacto                  |
| **6**   | Catalogo grande, cards menores                    |

### Produtos na Loja

Cada produto e exibido em um card com:

- Imagem do produto.
- Nome e descricao curta.
- Preco.
- Botao **"Adicionar ao carrinho"**.

---

## Gerenciamento do Carrinho

### Adicionando Itens

- Clique em **"Adicionar ao carrinho"** no card do produto.
- O produto e adicionado ao carrinho interno do GameCP.

### Revisando o Carrinho

Na aba **"Carrinho"**, o jogador pode:

| Acao                  | Descricao                                       |
| --------------------- | ----------------------------------------------- |
| **Ver itens**         | Lista de produtos adicionados                    |
| **Alterar quantidade**| Ajustar numero de unidades (quando permitido)    |
| **Remover item**      | Excluir produto do carrinho                      |
| **Ver subtotal**      | Valor parcial antes de descontos                 |
| **Ver descontos**     | Wallet GameCP e cupons WooCommerce               |

---

## Checkout e Pagamento

### Tela de Checkout

Ao seguir para o checkout, o sistema mostra:

- **Resumo do pedido** com todos os itens.
- **Campos obrigatorios** do WooCommerce (se houver).
- **Metodos de pagamento** disponiveis.
- **Opcao de Wallet** GameCP (quando habilitada).

### Gateways de Pagamento

Todos os gateways configurados no WooCommerce ficam disponiveis no checkout do GameCP:

| Gateway          | Descricao                                       |
| ---------------- | ----------------------------------------------- |
| **PIX**          | Pagamento instantaneo (Brasil)                   |
| **Cartao**       | Credito/debito via gateway                       |
| **PayPal**       | Pagamento internacional                          |
| **Boleto**       | Boleto bancario                                  |
| **Outros**       | Qualquer gateway WooCommerce configurado         |

### Finalizando o Pedido

1. Revise o resumo do pedido.
2. Selecione o metodo de pagamento.
3. (Opcional) Marque para usar saldo da Wallet.
4. Confirme o pagamento.
5. WooCommerce registra o pedido.
6. GameCP dispara a **entrega automatica** no servidor.

---

## Desconto via Wallet no Checkout

Se a **Wallet GameCP** estiver habilitada e o jogador tiver saldo:

### Fluxo

1. No **carrinho** ou **checkout**, aparece o checkbox **"Use GameCP Wallet"**.
2. O sistema exibe o saldo disponivel.
3. Ao marcar:
   - Desconto e aplicado no subtotal.
   - Limitado pelo saldo da Wallet e pelo valor do carrinho.
   - Linha **"GameCP Wallet Discount"** aparece nos totais.
4. Ao finalizar, o valor usado e **debitado** do saldo.
5. Nota adicionada ao pedido indicando o valor pago via Wallet.

### Conversao de Moeda

- Suporte automatico a multi-moeda.
- Saldo em USD convertido para a moeda da loja.
- Debito final recalculado em USD equivalente.

Se nao houver saldo, o checkbox nao e exibido.

---

## Configuracao pelo Admin

### Configurando Produtos no WooCommerce

1. Crie produtos normalmente no WooCommerce (itens RF, cash, VIP, pacotes).
2. Configure precos, categorias e descricoes.
3. Vincule cada produto ao sistema GameCP:
   - Tipo de entrega (item in-game, cash, VIP).
   - Pacote de itens associado.

### Configurando o Modulo Shop/Checkout

1. Garanta que o modulo esta **ativado** nas configuracoes do GameCP.
2. Configure o **layout de colunas** (3 a 6).
3. Configure **categorias** para filtros na loja.

### Configurando Gateways de Pagamento

- Configure os gateways desejados diretamente no **WooCommerce > Configuracoes > Pagamentos**.
- Todos os gateways ativos ficam disponiveis automaticamente no checkout do GameCP.

### Testando o Fluxo

1. Crie um pedido de teste com valor baixo.
2. Verifique a geracao do pedido no WooCommerce.
3. Confirme a entrega automatica no jogo.
4. Teste o desconto via Wallet (se habilitado).

---

## Boas Praticas

- Teste fluxos com **contas de teste** antes de abrir ao publico.
- Mantenha **lista clara** de quais produtos entregam quais itens no jogo.
- Use descricoes claras: "Entrega automatica", "Valido para 1 personagem", etc.
- Verifique regularmente pedidos com status pendente ou falho.
- Confira logs do GameCP em caso de duvidas na entrega.
- Combine com **Wallet** para oferecer flexibilidade de pagamento.
