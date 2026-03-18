---
title: Instalação e Ativação
description: Como instalar e configurar o GameCP no WordPress
layout: default
category: introducao
order: 2
---

# Instalação e Ativação do GameCP

Guia completo para instalar, configurar e ativar o GameCP v1.7.0 no seu servidor RF Online.

---

## Visão Geral

A instalação do GameCP envolve: configurar a conexão com o banco de dados do RF Online, ativar o módulo no WordPress, criar as tabelas auxiliares e configurar os administradores. Ao final, o painel estará acessível por URL direta, shortcode ou menu admin.

---

## Requisitos

| Requisito | Descrição |
| --- | --- |
| **Plugin DevsBR** | Instalado e ativado no WordPress |
| **PHP 8.2+** | Versão mínima obrigatória |
| **WordPress** | Versão 5.0 ou superior |
| **WooCommerce** | Instalado e configurado (para loja e checkout) |
| **SQL Server** | Banco de dados do RF Online com credenciais válidas |
| **Extensão PDO** | SQLSRV ou DBLIB para conexão com SQL Server |
| **Acesso Admin** | Usuário administrador do WordPress |

---

## Passo 1: Configurar Conexão com Banco

1. Acesse **WordPress Admin > DevsBR Panel > Configurações**
2. Preencha os dados de conexão:
   - **Host**: IP do servidor SQL (ex: `127.0.0.1` ou `192.168.1.100`)
   - **Porta**: Geralmente `1433`
   - **Usuário**: Usuário do banco
   - **Senha**: Senha do banco
   - **Bancos**: RF_User, RF_World, RF_Billing
3. Selecione o **Sistema de Proteção**: Odin, DevCorp, HGK ou SirinGuard
4. Clique em **Testar Conexão**
5. Se estiver OK, **Salve as configurações**

---

## Passo 2: Ativar o Módulo GameCP

1. Acesse **WordPress Admin > DevsBR Panel > Módulos**
2. Localize o módulo **"GameCP"**
3. Marque como **Ativo**
4. Salve as configurações

Ao ativar, o sistema:

- Registra as rotas internas do painel
- Cria/atualiza a página principal do GameCP
- Inicializa os hooks necessários

---

## Passo 3: Verificar a Página do GameCP

O sistema cria automaticamente uma página com o shortcode `[gamecp]`.

### Verificar se foi criada:

1. Acesse **Páginas > Todas as páginas**
2. Procure por **"Game Control Panel"** ou slug **`gamecp`**
3. Confirme que o conteúdo é apenas: `[gamecp]`
4. O status deve ser **Publicado**

### Se não foi criada automaticamente:

1. Crie uma nova página
2. Título: "Game Control Panel" (ou outro de sua preferência)
3. Conteúdo: `[gamecp]`
4. Slug: `gamecp`
5. Publique a página

---

## Passo 4: Criar Tabelas do GameCP

O GameCP precisa de tabelas auxiliares no banco de dados:

1. Acesse **DevsBR Panel > GameCP > Configurações**
2. Na seção **"Tabelas do Sistema"**, clique em **"Criar/Atualizar Tabelas"**
3. O sistema criará automaticamente:
   - `tbl_gamecp_users` — Dados dos usuários
   - `tbl_gamecp_wallet` — Carteira digital
   - `tbl_gamecp_admin_logs` — Logs administrativos
   - `tbl_gamecp_quests` — Sistema de quests
   - `tbl_gamecp_battlepass` — Passe de batalha
   - `tbl_gamecp_newplayer` — Campanhas new player
   - E outras tabelas conforme os módulos ativos
4. Confirme que o status está **"OK"** (verde)

---

## Passo 5: Configurar Administradores

1. Acesse **DevsBR Panel > GameCP Admin**
2. Clique em **"Adicionar Novo Administrador"**
3. Informe o **login do jogo** (conta RF Online)
4. Defina o **nível** de acesso:
   - **Administrador**: Acesso total
   - **Moderador**: Acesso limitado
   - **Suporte**: Apenas visualização
5. Marque as **permissões** específicas
6. Salve

---

## Passo 6: Acessar o GameCP

Existem três formas de acessar o GameCP:

### 1. URL Direta

```
https://seu-site.com/gamecp/
```

Acesso direto pelo navegador. O jogador faz login com a conta do jogo (não a conta WordPress).

### 2. Shortcode

Adicione `[gamecp]` em qualquer página do WordPress para renderizar o painel.

### 3. Menu Admin do WordPress

Acesse **WordPress Admin > DevsBR Panel > GameCP** para gerenciamento administrativo via painel WordPress.

---

## Configurações Adicionais

### Ativar Módulos

Em **DevsBR Panel > Módulos**, ative os módulos desejados:

| Módulo | Descrição |
| --- | --- |
| **GameCP Wallet** | Carteira digital |
| **GameCP Quests** | Sistema de missões |
| **GameCP Battlepass** | Passe de batalha |
| **GameCP Auction** | Sistema de leilão e venda de personagens |
| **GameCP New Player** | Recompensas para novos jogadores |
| **GameCP Spin Wheel** | Roleta de prêmios |
| **GameCP History Logs** | Histórico de itens (API) |
| **GameCP Coins** | Moeda virtual do painel |
| **GameCP Redeem** | Pacotes e códigos promocionais |

### Configurar WooCommerce

1. Certifique-se que o WooCommerce está ativo
2. Configure os métodos de pagamento
3. Crie produtos com os campos do GameCP
4. A loja aparecerá automaticamente no menu do GameCP

### Configurar Segurança

1. **2FA**: Será solicitado na primeira vez que um admin acessar
2. **Cloudflare Turnstile**: Configure em **DevsBR Panel > Segurança**
3. **Verificação de Email**: Ative em **Módulos > Verificação de Email**

---

## Solução de Problemas

### Tela em branco ou erro 500

| Causa provável | Solução |
| --- | --- |
| Plugin desativado | Verifique se o plugin DevsBR está ativo |
| Erro de PHP | Confira os logs de erro do PHP (`wp-content/debug.log`) |
| Shortcode incorreto | Confirme que a página tem apenas `[gamecp]` |
| Versão do PHP | Atualize para PHP 8.2 ou superior |

### Erro de conexão com banco

| Causa provável | Solução |
| --- | --- |
| Credenciais erradas | Teste a conexão em **DevsBR Panel > Configurações** |
| Firewall bloqueando | Verifique se a porta 1433 está liberada |
| Extensão ausente | Instale a extensão PDO SQLSRV ou DBLIB no PHP |
| Servidor SQL fora | Confirme que o SQL Server está rodando |

### Login não funciona

| Causa provável | Solução |
| --- | --- |
| Proteção errada | Verifique o sistema de proteção selecionado (Odin/DevCorp/HGK/SirinGuard) |
| Conta inexistente | Confirme que a conta existe no banco RF |
| Tabelas corrompidas | Recrie as tabelas em GameCP > Configurações |

### Módulos não aparecem

| Causa provável | Solução |
| --- | --- |
| Módulo inativo | Confirme que o módulo está ativo em DevsBR Panel > Módulos |
| Sem permissão | Verifique permissões do usuário |
| Cache | Limpe o cache do WordPress e do navegador |

### Página do GameCP retorna 404

| Causa provável | Solução |
| --- | --- |
| Permalinks | Acesse **Configurações > Links permanentes** e salve novamente |
| Página não publicada | Verifique se a página com `[gamecp]` está publicada |

---

## Checklist de Instalação

- [ ] PHP 8.2+ instalado e funcionando
- [ ] Plugin DevsBR instalado e ativo
- [ ] Conexão com SQL Server configurada e testada
- [ ] Sistema de proteção selecionado
- [ ] Módulo GameCP ativo
- [ ] Página /gamecp/ criada e publicada
- [ ] Tabelas do GameCP criadas com sucesso
- [ ] Pelo menos um administrador criado
- [ ] Acesso ao painel funcionando
- [ ] WooCommerce configurado (para loja)
- [ ] Módulos extras ativados conforme necessário
- [ ] Segurança configurada (2FA, Turnstile)

---

## Tutoriais Relacionados

- [Visão Geral do GameCP](gamecp-resumo)
- [Painel Admin e Permissões](gamecp-admin-panel)
- [Loja e Checkout](gamecp-shop-checkout)
- [Carteira (Wallet)](wallet)
- [Autenticação 2FA](2fa-seguranca)
