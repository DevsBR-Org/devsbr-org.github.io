---
title: Passe de Batalha (Battlepass)
description: Sistema de temporadas com trilhas Free e Premium
layout: default
category: modulos
order: 7
---

# Passe de Batalha (Battlepass)

O Battlepass e um sistema de **temporadas com recompensas progressivas** em duas trilhas: Free e Premium. Os jogadores acumulam XP e desbloqueiam niveis para resgatar itens, cash e outros premios.

---

## Visao Geral

| Recurso            | Descricao                                         |
| ------------------ | ------------------------------------------------- |
| **Temporadas**     | Periodos com inicio e fim configurados pelo admin  |
| **Niveis**         | Progresso por XP com recompensas em cada nivel     |
| **Trilha Free**    | Recompensas disponiveis para todos os jogadores    |
| **Trilha Premium** | Recompensas extras para quem possui o passe pago   |
| **Recompensas**    | Itens, cash, pontos, premium e mais                |
| **Weapon Skins**   | Selecao de skins de arma como recompensa           |

---

## Acesso ao Painel Admin

1. Faca login no GameCP com conta de administrador.
2. Acesse **Admin > Battlepass** no menu lateral.
3. A tela exibe as opcoes de gerenciamento de temporadas e recompensas.

---

## Criando uma Nova Temporada

Na tela do Battlepass, clique em **"Cadastrar nova temporada"** e preencha:

| Campo              | Descricao                                          |
| ------------------ | -------------------------------------------------- |
| **Nome**           | Nome identificador (ex.: "Season 1 - 2026")        |
| **Descricao**      | Texto curto sobre a tematica (opcional)             |
| **Data de inicio** | Dia em que a temporada comeca a valer               |
| **Data de fim**    | Dia em que a temporada encerra                      |

Clique em **"Cadastrar"** para salvar. A temporada aparecera na lista para edicao.

---

## Gerenciando uma Temporada

1. Na area **"Gerenciar Temporada"**, selecione a temporada desejada no campo de selecao.
2. As datas, descricao e os niveis/recompensas ja cadastrados sao carregados automaticamente.
3. Sem selecionar uma temporada, nao e possivel editar niveis ou recompensas.

---

## Trilhas e Niveis (Free x Premium)

Dentro da temporada selecionada existem duas abas:

### Trilha Normal (Free)

- Disponivel para todos os jogadores que acumulam XP.
- Cada nivel possui:
  - Botao para **adicionar recompensas**.
  - Botao para **remover o nivel**.
  - Campo **"XP necessaria"** para definir o requisito daquele nivel.

### Trilha Premium

- Recompensas exclusivas para quem possui o passe premium ativo.
- A XP necessaria e a mesma definida na trilha Normal.
- Estrutura identica, porem focada em premios extras.

---

## Criando Niveis

1. Acesse a aba **Normal** ou **Premium**.
2. Clique em **"Adicionar Nivel"**.
3. Um novo bloco e criado com titulo automatico (ex.: "Nivel 5").
4. Na trilha Normal, preencha o campo **"XP necessaria"** para cada nivel.

---

## Cadastrando Recompensas em um Nivel

Dentro de cada nivel, clique em **"Adicionar Item"** para criar uma linha de recompensa.

### Categorias de Recompensa

| Categoria      | Descricao                                      |
| -------------- | ---------------------------------------------- |
| **Items**      | Item do jogo (arma, armadura, consumivel)       |
| **Cash**       | Moeda de cash do servidor                       |
| **GamePoint**  | Gold, Dalant ou outros pontos                   |
| **Premium**    | Beneficios ligados ao passe premium             |
| **MaxLevel**   | Premios especiais para niveis finais            |

### Campos da Recompensa

| Campo          | Descricao                                      |
| -------------- | ---------------------------------------------- |
| **Item**       | Busca por nome ou codigo com autocomplete       |
| **Talics**     | Pedras/bonus adicionais ao item                 |
| **Quantidade** | Numero de unidades (ex.: 1 arma, 10 pocoes)     |
| **Tempo**      | Duracao para itens temporarios (0 = permanente) |
| **Valor**      | Quantia para categorias de moeda/pontos         |
| **Bonus**      | Valor extra junto com a recompensa principal    |

### Selecao de Weapon Skin

Quando a recompensa e do tipo **Items** e se trata de uma arma, e possivel selecionar uma **skin de arma** especifica. O admin escolhe a aparencia visual que o jogador recebera ao desbloquear aquele nivel.

### Botoes de Acao

- **Remover**: apaga a recompensa do nivel.
- **Duplicar**: cria uma copia da recompensa no mesmo nivel, util para cadastrar conjuntos de armadura mudando apenas detalhes.

Voce pode adicionar **varias recompensas** no mesmo nivel, em ambas as trilhas.

---

## Salvando as Configuracoes

1. Apos ajustar todos os niveis e recompensas, role ate o final da pagina.
2. Clique em **"Salvar recompensas"**.
3. Aguarde a confirmacao. Alteracoes so sao gravadas ao clicar nesse botao.

---

## Visao do Jogador

O jogador acessa o Battlepass pelo menu do GameCP e visualiza:

### Elementos da Tela

| Elemento              | Descricao                                      |
| --------------------- | ---------------------------------------------- |
| **Barra de progresso**| XP atual e progresso geral na temporada         |
| **Niveis Free**       | Recompensas da trilha gratuita                  |
| **Niveis Premium**    | Recompensas da trilha paga                      |
| **Status por nivel**  | Disponivel, resgatado ou bloqueado              |

### Condicoes de Resgate

- **Trilha Normal**: basta atingir a XP necessaria do nivel.
- **Trilha Premium**: precisa ter o passe premium ativo E atingir a XP necessaria.
- Recompensas ja resgatadas ficam marcadas com indicacao visual.
- Niveis ainda nao alcancados exibem botao desativado com mensagem de XP insuficiente.

### Fluxo de Resgate

1. O jogador atinge a XP de um nivel.
2. O botao **"Resgatar"** fica disponivel.
3. Ao clicar, o item e entregue ao personagem.
4. O nivel e marcado como resgatado.

---

## Boas Praticas

- Crie temporadas com duracao equilibrada (30 a 90 dias e uma boa faixa).
- Distribua recompensas de forma progressiva: itens mais valiosos nos niveis mais altos.
- Use a trilha Premium para itens cosmeticos ou exclusivos, incentivando a compra do passe.
- Teste o fluxo completo com uma conta de teste antes de publicar a temporada.
- Combine o Battlepass com outros modulos (Quests, Wallet, Loja) para uma experiencia integrada.
