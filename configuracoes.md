---
title: Configurações do GameCP
description: Opções de configuração, manutenção, 2FA e controle de funcionalidades
layout: default
category: admin
order: 7
---

# Configurações do GameCP

O painel de configurações permite que o admin **controle todas as funcionalidades** do GameCP, incluindo modo de manutenção, bloqueio de recursos, 2FA e regras de registro.

---

## Visão Geral

| Recurso | Descrição |
|---------|-----------|
| **Manutenção** | Ativar/desativar modo de manutenção |
| **Registro** | Controle de cadastro de novas contas |
| **Bloqueio de Recursos** | Habilitar/desabilitar funcionalidades individualmente |
| **Verificação de Email** | Exigir verificação por página |
| **2FA** | Autenticação em dois fatores |
| **Loja** | Ativar/desativar loja do GameCP |
| **Visualizações** | Controle de visibilidade para jogadores |

> **Nota**: Este é um módulo exclusivamente administrativo.

---

## Acessando

1. Faça login como **admin** no GameCP
2. Acesse **Admin > Configurações**
3. Navegue pelas abas de configuração

---

## Modo de Manutenção

Quando ativado, o GameCP exibe uma **página de manutenção** para todos os jogadores, impedindo o acesso ao painel.

| Opção | Descrição |
|-------|-----------|
| **Ativar/Desativar** | Liga ou desliga o modo de manutenção |
| **Mensagem** | Texto exibido aos jogadores durante a manutenção |

> Admins continuam tendo acesso ao painel mesmo durante a manutenção.

---

## Controle de Registro

### Toggle de Registro

- **Ativar**: Permite que novos jogadores criem contas
- **Desativar**: Bloqueia o cadastro de novas contas

### Configurações de Registro

| Opção | Descrição |
|-------|-----------|
| **Restrições de nome** | Regras para nomes de conta permitidos |
| **Regras de validação** | Requisitos de senha, email, etc. |
| **Campos obrigatórios** | Quais campos são necessários no cadastro |

---

## Bloqueio de Funcionalidades

O admin pode **habilitar ou desabilitar** funcionalidades individuais do GameCP:

| Funcionalidade | Descrição |
|----------------|-----------|
| **Leilão** | Mercado de itens entre jogadores |
| **Battle Pass** | Sistema de progressão com recompensas |
| **Loja** | Loja de itens do GameCP |
| **Visualização de jogadores** | Permitir que jogadores vejam perfis de outros |
| **Outras funcionalidades** | Cada módulo pode ser ativado/desativado individualmente |

### Como Bloquear um Recurso

1. Acesse **Admin > Configurações**
2. Localize o recurso desejado na lista
3. Alterne o **toggle** para ativar ou desativar
4. Salve as configurações

> Recursos desativados ficam ocultos no menu e inacessíveis para jogadores.

---

## Verificação de Email

O admin pode exigir **verificação de email** como requisito para acessar páginas específicas do GameCP.

| Configuração | Descrição |
|--------------|-----------|
| **Por página** | Defina quais páginas exigem email verificado |
| **Global** | Exija verificação para todo o painel |
| **Desativado** | Não exigir verificação de email |

### Configurando

1. Acesse **Admin > Configurações > Verificação de Email**
2. Selecione as **páginas** que exigem verificação
3. Salve as configurações

> Para mais detalhes, veja o tutorial [Verificação de Email](verificacao-email).

---

## Autenticação em Dois Fatores (2FA)

O admin pode configurar o sistema de **2FA** para aumentar a segurança das contas.

### Configurações Disponíveis

| Opção | Descrição |
|-------|-----------|
| **Ativar/Desativar** | Liga ou desliga o 2FA globalmente |
| **Lista de exclusão** | Contas que não precisam usar 2FA |
| **Códigos de recuperação** | Gerenciamento de códigos de backup |

### Configurando o 2FA

1. Acesse **Admin > Configurações > 2FA**
2. **Ative** o 2FA globalmente
3. (Opcional) Adicione contas à **lista de exclusão** — contas que não serão obrigadas a usar 2FA
4. Configure as opções de **códigos de recuperação**
5. Salve as configurações

### Lista de Exclusão

A lista de exclusão permite que determinadas contas fiquem **isentas** do requisito de 2FA. Útil para:

- Contas de teste
- Contas de serviço
- Situações especiais

### Códigos de Recuperação

- Jogadores recebem **códigos de recuperação** ao ativar o 2FA
- Esses códigos permitem acesso caso percam o dispositivo autenticador
- O admin pode gerenciar e resetar códigos de recuperação

> Para mais detalhes, veja o tutorial [2FA e Segurança](2fa-seguranca).

---

## Toggle da Loja

| Opção | Descrição |
|-------|-----------|
| **Ativar** | Loja visível e funcional para jogadores |
| **Desativar** | Loja oculta e inacessível |

---

## Toggle de Visualização de Jogadores

Controla se jogadores podem **ver perfis e informações** de outros jogadores no painel.

| Opção | Descrição |
|-------|-----------|
| **Ativar** | Jogadores podem visualizar perfis de outros |
| **Desativar** | Perfis de outros jogadores ficam ocultos |

---

## Próximos Passos

- [2FA e Segurança](2fa-seguranca) — Detalhes sobre autenticação em dois fatores
- [Verificação de Email](verificacao-email) — Configuração de verificação de email
- [Cash e Premium](cash-premium) — Gerenciamento de cash e premium
- [Painel Admin](gamecp-admin-panel) — Visão geral do painel administrativo
