---
title: Carteira (Wallet)
description: Sistema de carteira digital integrado ao GameCP
layout: default
category: modulos
order: 3
---

# Carteira (Wallet) do GameCP

A Wallet e uma **carteira digital de creditos** integrada ao GameCP. Os jogadores visualizam saldo, solicitam saques por diversos metodos e utilizam o saldo como desconto no checkout WooCommerce.

---

## Visao Geral

| Recurso              | Descricao                                       |
| -------------------- | ----------------------------------------------- |
| **Saldo**            | Creditos em moeda base (USD)                     |
| **Exibicao**         | Card com saldo formatado no painel do jogador    |
| **Saques**           | PIX, PayPal, Wise, USDT                         |
| **Minimo/Taxa**      | Valor minimo e taxa configurados pelo admin      |
| **Checkout**         | Desconto via saldo no WooCommerce                |
| **Admin**            | Creditar, debitar, aprovar saques                |
| **Historico**        | Registro completo de todas as operacoes          |

---

## Visao do Jogador

### Acessando a Carteira

1. Faca login no GameCP.
2. Clique em **"Carteira"** no menu.

### Tela da Carteira

A pagina exibe tres secoes principais:

#### 1. Card de Saldo Disponivel

- Saldo atual formatado (ex.: "US$ 15,00").
- Indica creditos disponiveis para uso ou saque.

#### 2. Informacoes de Saque

| Informacao       | Descricao                                   |
| ---------------- | ------------------------------------------- |
| **Minimo**       | Valor minimo para solicitar saque            |
| **Taxa**         | Porcentagem cobrada sobre o saque            |
| **Status**       | Se o sistema de saques esta ativo            |

#### 3. Formulario de Saque

| Campo              | Descricao                                   |
| ------------------ | ------------------------------------------- |
| **Valor**          | Quantia desejada (mascara de moeda)          |
| **Metodo**         | Selecao do metodo de pagamento               |
| **Dados**          | Informacoes para transferencia               |

---

## Metodos de Saque

| Metodo      | Descricao                                        |
| ----------- | ------------------------------------------------ |
| **PIX**     | Transferencia via chave PIX (Brasil)              |
| **PayPal**  | Transferencia para conta PayPal                   |
| **Wise**    | Transferencia internacional via Wise              |
| **USDT**    | Transferencia em criptomoeda USDT                 |

---

## Solicitando um Saque

1. Verifique o saldo disponivel no card principal.
2. Preencha o **valor do saque** no formulario.
3. Escolha o **metodo de pagamento** desejado.
4. Informe os **dados de pagamento** necessarios.
5. Clique em **"Solicitar Saque"**.

### Validacoes Automaticas

O sistema verifica antes de aceitar:

- Valor **nao menor** que o minimo configurado.
- Valor **nao maior** que o saldo disponivel.
- Dados de pagamento preenchidos corretamente.
- Nonce de seguranca valido.

Se tudo estiver correto, a solicitacao e registrada e o saldo atualizado. Caso contrario, mensagem de erro e exibida.

---

## Historico de Saques

Tabela na parte inferior da pagina com:

| Campo         | Descricao                            |
| ------------- | ------------------------------------ |
| **Data/Hora** | Quando foi solicitado                |
| **Valor**     | Quantia solicitada                   |
| **Metodo**    | PIX, PayPal, Wise ou USDT           |
| **Status**    | Pendente, Aprovado, Pago, Cancelado  |
| **Dados**     | Resumo dos dados de pagamento        |

---

## Integracao com WooCommerce (Desconto no Checkout)

O saldo da Wallet pode ser usado como desconto no **checkout do WooCommerce**.

### Requisitos

- Jogador logado no GameCP.
- Modulo Wallet habilitado.
- Saldo disponivel na carteira.

### Fluxo

1. O jogador monta um pedido na loja (WooCommerce).
2. No **carrinho** e no **checkout**, aparece o checkbox **"Use GameCP Wallet"**.
3. Ao marcar:
   - O sistema exibe o saldo disponivel.
   - Aplica desconto no subtotal, limitado pelo saldo e pelo valor do carrinho.
   - O desconto aparece como **"GameCP Wallet Discount"** nos totais.
4. Ao finalizar o pedido, o valor e **debitado** do saldo no banco.
5. Uma nota e adicionada ao pedido indicando quanto foi pago via Wallet.

### Conversao de Moeda

- O sistema suporta multi-moeda automaticamente.
- O saldo em USD e convertido para a moeda ativa da loja.
- O debito final e recalculado em USD equivalente.

Se o jogador nao tiver saldo, o checkbox nao e exibido.

---

## Configuracao pelo Admin

### Configuracoes de Saque

| Opcao              | Descricao                                   |
| ------------------ | ------------------------------------------- |
| **Minimo de saque**| Valor minimo para solicitar (ex.: US$ 10)    |
| **Taxa de saque**  | Porcentagem cobrada (ex.: 5%)                |
| **Metodos ativos** | PIX, PayPal, Wise, USDT                     |
| **Status**         | Ativar/desativar sistema de saques           |

### Funcoes Administrativas

| Acao               | Descricao                                   |
| ------------------ | ------------------------------------------- |
| **Consultar**      | Ver saldo de qualquer jogador                |
| **Creditar**       | Adicionar saldo (eventos, recargas)          |
| **Debitar**        | Remover saldo com registro em log            |
| **Aprovar saques** | Gerenciar solicitacoes pendentes             |
| **Historico**      | Ver todas as operacoes da carteira           |

### Fluxo de Aprovacao de Saques

1. O jogador solicita um saque.
2. A solicitacao fica com status **"Pendente"**.
3. O admin acessa a lista de saques pendentes.
4. Analisa os dados e decide:
   - **Aprovar**: marca como aprovado e realiza a transferencia.
   - **Cancelar**: devolve o saldo ao jogador.
5. O status e atualizado e o jogador pode acompanhar no historico.

---

## Economia Unificada

- O saldo funciona tanto no GameCP quanto na Loja WooCommerce.
- Todas as operacoes (credito, debito, saque, desconto) sao registradas.
- Auditoria completa de movimentacoes disponivel para o admin.

---

## Boas Praticas

- Defina **origem dos creditos** claramente (eventos, recargas, recompensas).
- Ajuste **minimo e taxa** de saque conforme a realidade do servidor.
- Monitore historico de saques e descontos regularmente.
- Documente regras para os jogadores: validade, limites, politica de saques.
- Teste o fluxo completo (credito, saque, desconto no checkout) antes de abrir ao publico.
