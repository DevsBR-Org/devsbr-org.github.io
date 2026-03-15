---
title: Sistema de Quests
description: Missoes com recompensas e cooldowns no GameCP
layout: default
category: modulos
order: 4
---

# Sistema de Quests

As Quests sao **missoes de resgate de recompensas** que os jogadores podem completar pelo GameCP. O admin configura titulo, escopo, cooldown e recompensas; o jogador resgata diretamente pelo painel.

---

## Visao Geral

| Recurso         | Descricao                                       |
| --------------- | ----------------------------------------------- |
| **Titulo**      | Nome da quest (ex.: Login Diario, Evento Semanal)|
| **Descricao**   | Texto explicativo sobre a missao                 |
| **Escopo**      | Por conta ou por personagem                      |
| **Cooldown**    | Tempo entre resgates (segundos ate dias)         |
| **Level**       | Requisito de nivel minimo/maximo (auto ou manual)|
| **Recompensas** | Itens entregues automaticamente ao personagem    |
| **Status**      | Ativa ou inativa (toggle)                        |

---

## Acesso ao Cadastro de Quests (Admin)

1. Acesse o **GameCP** com conta de administrador.
2. No menu, entre em **Admin**.
3. Clique na aba **Quests**.
4. Certifique-se de que o modulo esta **ativado** nas configuracoes.

---

## Criando uma Nova Quest

### Selecionar ou Criar

- No campo **"Selecionar Quest"**, escolha uma quest existente para editar ou selecione **"Nova Quest..."** para criar do zero.

### Campos Principais

| Campo       | Descricao                                              | Obrigatorio |
| ----------- | ------------------------------------------------------ | ----------- |
| **Titulo**  | Nome amigavel da quest                                  | Sim         |
| **Descricao**| Texto explicativo exibido ao jogador                   | Nao         |
| **Escopo**  | **Por Conta** (uma vez por conta) ou **Por Personagem** (cada char separadamente) | Sim |
| **Ativa**   | Toggle que define se a quest aparece para jogadores     | Sim         |

### Configuracao de Cooldown

O cooldown define o **intervalo minimo entre um resgate e outro**.

| Parametro  | Descricao                                  |
| ---------- | ------------------------------------------ |
| **Valor**  | Numero (ex.: 24)                            |
| **Unidade**| Segundos, Minutos, Horas ou Dias            |

Exemplos praticos:

| Cenario            | Valor | Unidade  |
| ------------------ | ----- | -------- |
| Quest diaria       | 24    | Horas    |
| Quest semanal      | 7     | Dias     |
| Bonus rapido       | 30    | Minutos  |
| Evento pontual     | 3600  | Segundos |

Se o cooldown for zero ou invalido, o sistema nao aceita o cadastro.

### Requisitos de Level

| Modo       | Descricao                                                  |
| ---------- | ---------------------------------------------------------- |
| **Auto**   | Sistema calcula min/max com base no LevelLim/UpLevelLim dos itens |
| **Manual** | Admin informa **Min** e **Max** manualmente                |

No modo manual, o sistema valida que Min <= Max e ambos >= 1.

---

## Cadastro de Recompensas

Na secao **Recompensas**, defina o que o jogador recebe ao resgatar.

| Campo           | Descricao                                    | Obrigatorio |
| --------------- | -------------------------------------------- | ----------- |
| **Codigo Item** | Codigo da recompensa (com autocomplete)       | Sim         |
| **Talics**      | Pedras adicionais ao item (opcional)          | Nao         |
| **Quantidade**  | Unidades entregues (1 a 999)                  | Sim         |
| **Tempo**       | Tempo de aluguel (0 = permanente)             | Nao         |

### Tipos de Recompensa Suportados

- **Itens do jogo**: armas, armaduras, consumiveis.
- **Cash**: moeda do servidor.
- **Pontos**: GamePoint, Gold, Dalant, etc.

### Gerenciando Recompensas

- Clique em **"Adicionar Recompensa"** para criar outra linha.
- Clique em **"Remover"** para apagar uma linha especifica.
- E obrigatorio ter pelo menos **1 recompensa** com codigo preenchido.

---

## Toggle Ativa/Inativa

- **Ativa**: quest aparece no menu Quests do jogador e pode ser resgatada.
- **Inativa**: quest fica oculta, sem possibilidade de resgate.

O admin pode desativar temporariamente uma quest sem excluir, preservando historico e configuracoes.

---

## Salvando e Excluindo

- **Salvar Quest**: grava todas as configuracoes e recompensas.
- **Excluir Quest**: remove a quest, recompensas e historico de resgates.

A lista de quests exibe: ID, titulo, escopo, cooldown, nivel e status.

---

## Visao do Jogador

### Acessando as Quests

1. O jogador faz login no GameCP.
2. Clica em **Quests** no menu principal.
3. O sistema verifica conta RF, busca personagens e lista quests ativas.

### Escolha do Personagem

- No lado esquerdo, aparece a lista de personagens com nome e nivel.
- Ao selecionar um personagem, as quests sao filtradas pelo nivel e historico de resgate.

> Se a conta estiver **online no jogo**, aparece um alerta pedindo para desconectar antes de resgatar.

### Visualizacao das Quests

Cada quest e exibida em um card com:

- Imagem/icone baseada na primeira recompensa.
- Tempo de cooldown (ex.: "24 horas").
- Badges de nivel minimo e maximo.
- Informacao de qual personagem resgatou por ultimo (escopo por conta).

### Fluxo de Resgate

1. O jogador verifica se o botao **"Resgatar Quest"** esta disponivel.
2. Condicoes para resgate:
   - Conta **offline** no jogo.
   - Level do personagem dentro dos requisitos.
   - Cooldown cumprido.
3. Se faltar tempo, o botao exibe **"Disponivel em: HH:MM:SS"** com contagem regressiva.
4. Ao clicar em **"Resgatar Quest"**:
   - Popup de sucesso confirma o resgate.
   - O card e atualizado com novo cooldown.
   - Recompensas sao registradas para entrega ao personagem.
5. Em caso de erro (level invalido, conta online, cooldown), popup de erro e exibido.

---

## Boas Praticas

- Use nomes **claros e objetivos** para que o jogador entenda facilmente.
- Ajuste o cooldown conforme o tipo de recompensa (diaria, semanal, pontual).
- Quests fortes devem ter escopo **por conta**; quests de progressao podem ser **por personagem**.
- Use requisitos de level para segmentar o publico (iniciantes vs. endgame).
- Teste como admin se a quest aparece corretamente e se cooldown e requisitos funcionam.
