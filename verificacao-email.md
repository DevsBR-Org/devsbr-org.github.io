---
title: Verificacao de Email
description: Sistema de verificacao de email para novas contas
layout: default
category: seguranca
order: 2
---

# Verificacao de Email

O sistema de **verificacao de email** garante que contas tenham emails validos e acessiveis. Essencial para recuperacao de senha, comunicacao e seguranca.

---

## Visao Geral

| Recurso          | Descricao                                       |
| ---------------- | ----------------------------------------------- |
| **Obrigatorio**  | Configuravel pelo admin                          |
| **Metodo**       | Link ou codigo de verificacao                    |
| **Bloqueio**     | Conta limitada ate verificar                     |
| **Reenvio**      | Disponivel na pagina de verificacao              |
| **Validade**     | Tempo de expiracao configuravel                  |

---

## Por que Usar

- **Comunicacao**: garante canal de contato valido com o jogador.
- **Recuperacao**: permite recuperar senha por email.
- **Seguranca**: dificulta criacao de contas falsas.
- **Marketing**: lista de emails validos para comunicacoes.

---

## Fluxo de Verificacao

### No Registro da Conta

1. O jogador cria uma conta informando seu email.
2. O sistema envia automaticamente um **email de verificacao**.
3. O jogador recebe o email com link ou codigo.
4. Clica no link ou digita o codigo no GameCP.
5. Email verificado, conta totalmente liberada.

### Se Nao Verificar

- A conta pode ter **acesso limitado** a determinadas funcoes.
- O sistema exibe aviso constante pedindo verificacao.
- Modulos sensiveis podem ficar bloqueados.

---

## Visao do Jogador

### Verificando o Email

1. Acesse sua caixa de entrada.
2. Procure a mensagem do GameCP (verifique spam tambem).
3. **Clique no link** de verificacao.
4. Ou **copie o codigo** e digite no campo do GameCP.
5. Confirmacao de verificacao e exibida.

### Reenvio de Verificacao

Se o email nao chegou ou o link expirou:

1. Acesse o GameCP.
2. Va para a **pagina de verificacao de email**.
3. Clique em **"Reenviar"**.
4. Um novo email e enviado com link/codigo atualizado.
5. Verifique sua caixa de entrada novamente.

### Nao Recebeu o Email

| Situacao                    | Acao                                         |
| --------------------------- | -------------------------------------------- |
| Email nao chegou            | Verifique a pasta de **spam/lixo eletronico** |
| Email incorreto             | Corrija no perfil ou peca ao admin            |
| Demora no recebimento       | Aguarde alguns minutos e tente reenviar       |
| Problema persistente        | Verifique configuracao SMTP do servidor       |

---

## Configuracao (Admin)

### Ativando o Modulo

1. Acesse **DevsBR Panel > Modulos**.
2. Ative **"Verificacao de Email"**.
3. Salve as configuracoes.

### Opcoes Disponiveis

| Opcao            | Descricao                                      |
| ---------------- | ---------------------------------------------- |
| **Obrigatorio**  | Bloquear funcoes sem verificacao                |
| **Metodo**       | Link ou codigo                                  |
| **Validade**     | Tempo de expiracao do link/codigo               |
| **Template**     | Personalizacao do email enviado                 |

### Personalizacao do Template

| Campo          | Descricao                                       |
| -------------- | ----------------------------------------------- |
| **Assunto**    | Titulo do email                                  |
| **Corpo**      | Texto com link/codigo de verificacao             |
| **Remetente**  | Nome e email de origem                           |

---

## Configuracao de SPF e DKIM

Para evitar que emails caiam no spam, configure os registros DNS do dominio:

### SPF (Sender Policy Framework)

- Adicione um registro TXT no DNS do dominio.
- Define quais servidores podem enviar emails em nome do dominio.
- Exemplo: `v=spf1 include:_spf.google.com ~all`

### DKIM (DomainKeys Identified Mail)

- Adicione uma chave publica no DNS do dominio.
- Assina digitalmente os emails enviados.
- O provedor de email (ou plugin SMTP) fornece a chave a ser adicionada.

### Dicas para Entregabilidade

| Acao                          | Descricao                                  |
| ----------------------------- | ------------------------------------------ |
| **Configure SPF**             | Registro TXT no DNS                         |
| **Configure DKIM**            | Chave publica no DNS                        |
| **Use SMTP dedicado**         | Plugin SMTP no WordPress (ex.: WP Mail SMTP)|
| **Teste o envio**             | Envie emails de teste e verifique spam      |
| **Evite palavras de spam**    | No assunto e corpo do email                 |
| **Use remetente com dominio** | Evite enderecos genericos (@gmail, @hotmail) |

---

## Solucao de Problemas

### Emails Nao Chegam

1. Verifique a configuracao **SMTP** do WordPress.
2. Teste o envio de email pelo WordPress (plugin de teste).
3. Verifique registros **SPF/DKIM** do dominio.
4. Confira se o provedor de email nao esta bloqueando.

### Link Expirado

- Peca reenvio da verificacao pelo GameCP.
- Links expiram apos o periodo configurado pelo admin.

### Email Incorreto

- O jogador pode corrigir no perfil do GameCP.
- O admin pode corrigir manualmente no painel.

---

## Boas Praticas

- **Configure SPF/DKIM** antes de ativar o modulo.
- **Teste o envio** com contas de teste para garantir entrega.
- **Personalize o template** com a identidade visual do servidor.
- **Defina validade curta** (24-48h) para links de verificacao.
- **Monitore taxas de verificacao** para identificar problemas de entrega.
