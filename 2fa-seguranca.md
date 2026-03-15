---
title: Autenticação 2FA
description: Como configurar autenticação de dois fatores para administradores
layout: default
category: seguranca
order: 26
---

# Autenticação 2FA

A autenticação de dois fatores (2FA) adiciona uma camada extra de segurança ao login do admin usando o Google Authenticator.

---

## Como Acessar

1. Faça login no GameCP com sua conta admin
2. Clique em **Admin** no menu lateral
3. Clique na aba **2FA Setup**

---

## Ativar o 2FA

### Passo 1 — Gerar o Código Secreto

1. Clique em **"Gerar Código Secreto"**
2. O sistema gera um QR Code e um código manual

### Passo 2 — Configurar no Celular

1. Abra o **Google Authenticator** no celular
2. Toque em **"+"** para adicionar uma nova conta
3. **Escaneie o QR Code** exibido na tela, ou digite o código manualmente
4. O app vai mostrar um código de 6 dígitos que muda a cada 30 segundos

### Passo 3 — Verificar e Ativar

1. No campo **"Código de Verificação"**, digite o código de 6 dígitos que aparece no app
2. Clique em **"Verificar e Ativar 2FA"**
3. Se o código estiver correto, o 2FA é ativado

### Passo 4 — Salvar o Código de Backup

1. Após ativar, o sistema exibe um **código de backup**
2. **Copie e guarde** este código em local seguro
3. Ele será necessário se você perder acesso ao Google Authenticator

---

## Desativar o 2FA

1. Na página do 2FA, clique em **"Desativar 2FA"**
2. O 2FA é desligado mas o código secreto é mantido (pode reativar)

### Remover Completamente

1. Clique em **"Remover 2FA Completamente"**
2. Isso apaga o código secreto — será necessário reconfigurar do zero

---

## Tentativas Recentes

A tabela de tentativas mostra:
- **Status** — Sucesso ou Falha
- **IP** — Endereço de origem
- **Data/Hora** — Quando ocorreu

---

## Dicas

- Mantenha o **horário do celular sincronizado** (o 2FA depende do relógio)
- Se o código não funcionar, tente esperar o próximo ciclo de 30 segundos
- Se perder o celular, use o **código de backup** ou peça para outro admin resetar

---

## Próximos Passos

- [Configurações](configuracoes) — Ajustar funcionalidades do sistema
- [Painel Admin](gamecp-admin-panel) — Visão geral do painel admin
