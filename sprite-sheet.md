---
title: Sprite Sheet
description: Processamento de icones de itens do jogo
layout: default
category: administracao
order: 4
---

# Sprite Sheet

O Sprite Sheet converte o arquivo `.SPR` do jogo em **icones visiveis** no GameCP.

---

## Visao Geral

| Recurso       | Descricao                                    |
| ------------- | -------------------------------------------- |
| **Origem**    | Arquivo .SPR do cliente do jogo              |
| **Saida**     | Imagens PNG/JPG organizadas                  |
| **Uso**       | Inventario, Leilao, Quests, Battlepass, etc. |
| **Beneficio** | Icones identicos aos do jogo                 |

Quando configurado, os itens mostram o **mesmo icone visual do cliente do jogo**.

---

## O que e o Sprite Sheet

- Nos arquivos originais do jogo, os icones dos itens vem agrupados em um arquivo especifico (SPR).
- O Sprite Sheet e a **versao traduzida desse arquivo para o GameCP**, em formato de imagem (JPG/PNG) ja cortada e organizada.
- O GameCP usa esse Sprite Sheet para mostrar o icone correto de cada item no **Inventario**, **Leilao**, **Quests**, **Battlepass**, **Spin Wheel**, **New Player** e outros modulos.

---

## Configuracao (Admin)

### Acesso

1. Acesse o **GameCP** com conta de administrador.
2. Entre em **Admin > Sprite Sheet**.
3. A tela exibe: formulario de upload, area de progresso e listagem de sprites gerados.

### Processando o Arquivo .SPR

**Pre-requisitos:**

- Arquivo **.SPR** correto do seu cliente (compativel com o servidor).
- Acesso ao painel admin do GameCP.

**Passo a passo:**

1. Na secao **"Arquivo .SPR"**, clique no campo de upload e selecione o arquivo.
2. Clique em **"Processar SPR"**.
3. Acompanhe a **barra de progresso**.
4. Apos o termino, mensagem de sucesso ou erro e exibida.
5. Imagens geradas sao salvas na pasta interna de sprites (uploads do WordPress).
6. Arquivos aparecem em **"Sprites Gerados"** na mesma tela.

---

## Impacto nas Telas do GameCP

Com o Sprite Sheet processado:

- **Inventario**: itens com icone real.
- **Leilao**: mesma imagem do cliente do jogo.
- **Quests, Battlepass, Spin Wheel, New Player**: icones carregados do Sprite Sheet.
- **Telas de admin**: busca de inventario e itens com icone correspondente.

Sem Sprite Sheet: icones genericos ou mensagens de "Icone nao encontrado".

---

## Gerenciamento dos Sprites

Na secao **"Sprites Gerados"**:

- Visualize todos os arquivos gerados com miniatura.
- **Excluir individual**: botao de lixeira em cada card.
- **Excluir todos**: botao para remover todos os sprites e recomecar.

---

## Quando Reprocessar

- Atualizacao do cliente do jogo com mudancas nos icones.
- Adicao de muitos itens novos ao servidor.
- Itens aparecendo sem icone mesmo com cadastro correto.

**Fluxo de reprocessamento:**

1. Obtenha o arquivo .SPR atualizado.
2. (Opcional) Exclua sprites antigos.
3. Envie o novo .SPR e processe.
4. Confira em Inventario e Leilao se os icones foram atualizados.

---

## Boas Praticas

- Mantenha backup dos **arquivos .SPR originais**.
- Use sempre o arquivo compativel com seu cliente e servidor.
- Apos processar, teste em: Inventario, Quests, Leilao e Battlepass.
- Se houver erros de ambiente (Python, permissoes), ajuste no servidor/hosting.
