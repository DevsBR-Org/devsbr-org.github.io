---
title: Conselho (Patriarch System)
description: Gerenciamento do conselho de raças e sistema de patriarca no admin
layout: default
category: admin
order: 25
---

# Conselho (Patriarch System)

O módulo de Conselho permite gerenciar o sistema de Patriarca do RF Online, definindo os membros do conselho de cada raça com seus respectivos cargos.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Conselho**

> **Permissão necessária:** `manage_council`

---

## Estrutura do Conselho

Cada raça possui **9 posições** no conselho:

| Posição | Tipo | Descrição |
| --- | --- | --- |
| **Leader** | Principal | Líder/Patriarca da raça |
| **Consul** | Esquerda | Conselheiro político |
| **Strike** | Esquerda | Comandante de ataque |
| **Defense** | Esquerda | Comandante de defesa |
| **Support** | Esquerda | Comandante de suporte |
| **Consul** | Direita | Conselheiro secundário |
| **Strike** | Direita | Vice-comandante de ataque |
| **Defense** | Direita | Vice-comandante de defesa |
| **Support** | Direita | Vice-comandante de suporte |

### Raças disponíveis

- **Bellato** — Raça de humanos
- **Cora** — Raça espiritual
- **Accretia** — Raça mecânica

---

## Definir Membros do Conselho

1. Selecione a **raça** desejada
2. Para cada posição, digite o **nome do personagem**
   - O sistema possui **autocomplete** para facilitar a busca
   - A raça do personagem é **validada automaticamente** (deve pertencer à raça selecionada)
3. Ao buscar, o sistema exibe informações do personagem: **Level**, **PvP Points**, **Guild** e **Grade**
4. Para desativar uma posição, deixe como **"None"**
5. Clique em **"Salvar Conselho"** para aplicar as alterações

> **Importante:** Não é possível colocar o mesmo personagem em duas posições diferentes.

---

## Forçar Ativação do Patriarca

O sistema permite forçar a ativação do patriarca (ProcType=4) diretamente pelo admin:

1. Clique no botão **"Forçar Ativação"**
2. Confirme a operação
3. O sistema atualiza a tabela `tbl_patriarch_elect`

> **Atenção:** Após forçar a ativação, é necessário **reiniciar o Zone/World Server** para que as alterações tenham efeito no jogo.

---

## Tabelas do Banco de Dados

| Tabela | Função |
| --- | --- |
| `tbl_patriarch_elect` | Registros de eleição e ProcType |
| `tbl_patriarch_candidate` | Membros do conselho e seus cargos |

---

## Próximos Passos

- [Visão Geral do Admin](gamecp-admin-panel) — Todas as abas do painel
- [Buscar Jogadores](admin-buscar) — Pesquisar contas e personagens
- [Configurações](configuracoes) — Ajustar funcionalidades do sistema
