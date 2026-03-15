---
title: Race Transfer (RT)
description: Transferência de raça de personagens
layout: default
category: administracao
order: 2
---

# Race Transfer (RT)

O RT permite **mudar a raça de um personagem** de forma assistida e segura pelo GameCP.

---

## Visão Geral

| Recurso | Descrição |
| --- | --- |
| **Função** | Mudar raça (Bellato, Cora, Accretia) |
| **Conversão** | Itens são convertidos automaticamente |
| **Tipo de Armadura** | Seleção de Melee, Range ou Force na v1.6.0 |
| **Preview** | Mostra antes/depois da troca |
| **Segurança** | Operação registrada em log |
| **Acesso** | Apenas admins com permissão |

O RT evita edições manuais no banco, reduzindo risco de "quebrar" personagens.

---

## Quem usa o RT?

O módulo de RT é voltado para **staff/admin** (GM, dono do servidor, moderador com permissão).

No GameCP:

- Aparece como uma **aba administrativa** (Race Transfer / RT), apenas para usuários com permissão especial
- Jogadores comuns **não** acessam diretamente o RT

Usos comuns:

- Serviço pago (ex: "Troca de Raça Premium")
- Ferramenta interna para correções e migrações

---

## Quando usar o Race Transfer?

| Cenário | Descrição |
| --- | --- |
| **Mudança de facção** | Jogador quer trocar de raça sem perder o personagem |
| **Rebalanceamento** | Incentivar migração entre raças no servidor |
| **Correção** | Personagem criado na raça errada |
| **Evento especial** | Eventos de "Migração de Raça" |

---

## Passo a Passo

### 1. Acessar o RT

1. Entre no **GameCP** com um usuário administrador
2. Acesse a área **Admin**
3. Vá até a aba **Race Transfer (RT)**
4. Se não tiver permissão, o sistema exibirá aviso de acesso restrito

### 2. Selecionar o Personagem

1. No campo de busca, digite o **nome** ou **serial** do personagem
2. Clique em **Buscar**
3. O sistema exibe:
   - Nome do personagem
   - Raça atual
   - Classe atual
   - Serial do personagem
4. Confirme que é o personagem correto e avance

### 3. Escolher Nova Raça, Classe e Tipo de Armadura

1. Selecione a **nova raça** desejada (Bellato, Cora ou Accretia)
2. Após escolher a raça, o campo de **classe** é liberado
3. Selecione a **nova classe** compatível com a nova raça
4. **Novidade v1.6.0**: Selecione o **tipo de armadura** desejado:
   - **Melee** — armaduras de combate corpo a corpo
   - **Range** — armaduras de combate à distância
   - **Force** — armaduras de combate mágico

A seleção do tipo de armadura determina como os equipamentos serão convertidos, garantindo que o personagem receba armaduras compatíveis com seu estilo de jogo na nova raça.

> A lista de classes é filtrada automaticamente pela raça escolhida, evitando combinações inválidas.

### 4. Prévia de Itens (Antes e Depois)

Antes de confirmar, o RT gera uma **prévia** completa:

- Inventário e equipamentos **antes** da transferência
- Como ficarão os mesmos itens **depois**, de acordo com a nova raça e tipo de armadura selecionado

O sistema:

- Converte armaduras da raça antiga para equivalentes da nova raça, respeitando o tipo selecionado (Melee/Range/Force)
- Ajusta anéis, amuletos, poções e itens específicos que variam por raça
- Mantém itens "globais" (que servem para qualquer raça) sem alteração
- Marca itens sem equivalente perfeito com **aviso** (warning)

### 5. Confirmar a Transferência

1. Informe o **motivo da transferência** (campo obrigatório)
   - Exemplos: "Serviço pago – RT Premium", "Correção de personagem", "Evento de migração"
2. Clique em **Confirmar**
3. O sistema executa:
   - Atualização da raça e classe do personagem
   - Conversão dos itens compatíveis com base no tipo de armadura escolhido
   - Registro da ação em log administrativo
4. Mensagem de sucesso com resumo:
   - Raça antiga e nova raça
   - Tipo de armadura selecionado
   - Quantidade de itens convertidos

Se ocorrer algum problema, o sistema informa o erro e não aplica mudanças parciais.

---

## O que o RT faz com os itens?

| Tipo de Item | Ação |
| --- | --- |
| **Armaduras** | Convertidas para a nova raça, respeitando o tipo (Melee/Range/Force) selecionado |
| **Anéis e amuletos** | Convertidos para equivalentes da nova raça |
| **Poções especiais** | Convertidas conforme padrões de família de itens |
| **Itens globais** | Mantidos sem alteração |
| **Sem equivalente** | Marcados com aviso para avaliação manual |

---

## Boas Práticas

- Sempre **salvar o motivo** da transferência com clareza para auditorias futuras
- Evitar fazer RT em personagens com inventário lotado ou itens raros sem equivalentes claros
- Em casos sensíveis, considerar fazer backup manual antes
- Selecionar o **tipo de armadura** correto de acordo com a build desejada do personagem

---

## Uso Comercial do RT

Sugestão para monetização:

1. Crie um **serviço premium** de troca de raça na loja
2. O jogador compra o direito de RT
3. Abre ticket ou envia dados do personagem
4. A staff executa o RT pelo GameCP
5. Combine regras claras: limite de RT, garantias sobre itens, possibilidade de ajuste manual

---

## Tutoriais Relacionados

- [Painel Admin](gamecp-admin-panel)
- [Histórico de Logs](history-logs)
- [Visão Geral do GameCP](gamecp-resumo)
