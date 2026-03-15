---
title: Sistema Redeem
description: Pacotes de itens e codigos promocionais
layout: default
category: modulos
order: 8
---

# Sistema Redeem

O Redeem permite criar **pacotes de itens** que jogadores resgatam pelo GameCP. Inclui resgate por codigo promocional, compra antecipada de pacotes (early-redeem-buy), variantes por raca e selecao de personagem.

---

## Visao Geral

| Recurso                | Descricao                                       |
| ---------------------- | ----------------------------------------------- |
| **Pacotes**            | Conjuntos de itens configuraveis                 |
| **Codigos**            | Codigos promocionais gerados pelo admin          |
| **Early Redeem Buy**   | Compra antecipada de pacotes pela loja           |
| **Variantes por Raca** | Pacotes com itens diferentes por raca            |
| **Selecao de Char**    | Jogador escolhe o personagem para receber        |
| **Integracao**         | WooCommerce e entrega automatica                 |

---

## Resgate por Codigo (Code Redemption)

### Fluxo do Jogador

1. O jogador recebe um **codigo promocional** (via evento, campanha, suporte).
2. Acessa o GameCP e vai na aba **Redeem/Resgates**.
3. Digita o codigo no campo de resgate.
4. Seleciona o **personagem** que recebera os itens.
5. Confirma o resgate.
6. Os itens sao entregues automaticamente.

### Geracao de Codigos (Admin)

O administrador pode gerar codigos promocionais:

1. Acesse **Admin > Redeem** no GameCP.
2. Na secao de geracao de codigos:
   - Defina o **pacote** associado ao codigo.
   - Configure a **quantidade de usos** (unico ou multiplo).
   - Gere o codigo (aleatorio ou personalizado).
3. Distribua o codigo por eventos, redes sociais ou suporte.

| Opcao              | Descricao                                       |
| ------------------ | ----------------------------------------------- |
| **Codigo unico**   | Cada codigo so pode ser usado uma vez            |
| **Codigo multiplo**| Mesmo codigo pode ser usado por varios jogadores |
| **Expiracao**      | Data limite para uso do codigo                   |

---

## Compra Antecipada (Early Redeem Buy)

O sistema permite vender pacotes pela loja que ficam disponiveis para resgate posterior.

### Fluxo

1. O jogador compra um pacote na **Loja** (WooCommerce).
2. Apos aprovacao do pagamento, um **registro de Redeem** e criado automaticamente.
3. O jogador acessa o GameCP, vai em **Redeem/Resgates**.
4. Visualiza o pacote pendente e escolhe o **personagem**.
5. Confirma o resgate e os itens sao entregues.

Isso permite que o jogador compre antes e escolha o personagem depois.

---

## Variantes por Raca (Race-Specific)

Pacotes podem ter **itens diferentes por raca** do personagem:

| Raca       | Itens Exemplo                                    |
| ---------- | ------------------------------------------------ |
| **Bellato** | Armadura Bellato, Arma MAU, Escudo Bellato       |
| **Cora**    | Armadura Cora, Staff Cora, Manto Cora            |
| **Accretia**| Armadura Accretia, Launcher, Modulo Accretia     |

Quando o jogador seleciona um personagem para resgate, o sistema identifica a raca e entrega os itens correspondentes.

### Configuracao (Admin)

1. Ao criar o pacote, ative a opcao de **variantes por raca**.
2. Configure os itens para cada raca separadamente.
3. O sistema entrega automaticamente a variante correta com base no personagem selecionado.

---

## Visao do Jogador no GameCP

Quando o modulo Redeem esta ativo e o jogador possui pacotes disponiveis:

### Tela de Resgates

- Lista de **pacotes pendentes** para a conta.
- Informacoes de cada pacote: nome, descricao, status.
- Botao para **resgatar** e campo de **selecao de personagem**.

### Fluxo de Resgate

1. Acessar o GameCP e ir em **Redeem/Resgates**.
2. Escolher o pacote disponivel.
3. Selecionar o **personagem** que recebera os itens.
4. Confirmar o resgate.
5. Pacote marcado como resgatado e itens entregues.

---

## Visao do Administrador

### Configurando Pacotes

| Campo          | Descricao                                       |
| -------------- | ----------------------------------------------- |
| **Nome**       | Nome do pacote exibido ao jogador                |
| **Descricao**  | Detalhes do conteudo                             |
| **Itens**      | Lista de itens com quantidades                   |
| **Raca**       | Se aplicavel, variantes por raca                 |
| **Regras**     | Expiracao, limite de uso                         |

### Associando Pacotes

O admin pode associar pacotes a jogadores de diversas formas:

- **Compra na loja**: pedido WooCommerce aprovado gera o registro.
- **Codigo promocional**: jogador digita o codigo para receber.
- **Registro manual**: admin associa diretamente a uma conta.

### Gerenciamento

- Visualize todos os pacotes criados e seus status.
- Acompanhe resgates realizados para auditoria.
- Exclua pacotes quando necessario.

---

## Integracao com Outros Modulos

| Modulo          | Integracao                                      |
| --------------- | ----------------------------------------------- |
| **Loja**        | Compra gera registro de Redeem automaticamente   |
| **Wallet**      | Compra de pacotes com creditos da carteira       |
| **Battlepass**   | Pacotes como parte de progressoes                |
| **New Player**   | Kits iniciais via Redeem                         |

---

## Boas Praticas

- Use descricoes claras para os pacotes (conteudo, restricoes, validade).
- Mantenha historico dos resgates para auditoria.
- Para codigos promocionais, defina expiracao para evitar uso indefinido.
- Use variantes por raca para garantir que cada jogador receba itens compativeis.
- Teste o fluxo completo (geracao de codigo, resgate, entrega) antes de distribuir.
