---
title: Mapas (AutoCash)
description: Como configurar mapas e zonas para o sistema de AutoCash
layout: default
category: admin
order: 25
---

# Mapas (AutoCash)

Configure os mapas do jogo e suas zonas para o sistema de AutoCash. Defina onde e quando os jogadores recebem cash automático.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **Mapas**

> Esta aba só aparece se o módulo AutoCash estiver ativado.

---

## Adicionar um Novo Mapa

1. Clique para expandir o formulário **"Adicionar Novo Mapa"**
2. Preencha:

| Campo | O que preencher |
| --- | --- |
| **Código do Mapa** | ID do mapa no jogo (número) |
| **Nome do Mapa** | Nome identificador (ex: "Sette Desert") |
| **Quantidade de Cash** | Quanto cash o jogador recebe neste mapa |

3. (Opcional) Configure a **zona legada**: Centro X/Y/Z e Raio X/Y/Z
4. Para adicionar zonas dinâmicas, clique em **"Adicionar Nova Zona"** e preencha:
   - **X / Y / Z** — Coordenadas do centro da zona
   - **Raio X / Y / Z** — Raio da zona
   - **Hora Início / Hora Fim** — Janela de horário em que a zona funciona (opcional)
5. Clique em **"Salvar Mapa"**

> Se nenhuma zona for configurada, o cash é entregue em qualquer lugar do mapa. Se pelo menos uma zona existir, o jogador precisa estar dentro de uma zona.

---

## Gerenciar Mapas

Na tabela de mapas:

- **Editar** — Clique para carregar os dados no formulário
- **Excluir** — Remova o mapa

---

## Próximos Passos

- [AutoCash](autocash) — Configurar entrega automática de cash
- [Configurações](configuracoes) — Ajustar funcionalidades do sistema
- [Cash e Premium](cash-premium) — Gerenciar cash e premium
