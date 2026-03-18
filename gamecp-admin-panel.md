---
title: Painel Admin e Permissões
description: Gerenciamento de administradores e permissões do GameCP
layout: default
category: administracao
order: 1
---

# Painel Admin do GameCP

O Painel Admin é o centro de controle do GameCP v1.6.0, com **28+ abas** organizadas por categoria para gerenciamento completo do servidor.

---

## Visão Geral

O Admin do GameCP é separado do WordPress. Ele oferece controle total sobre:

- **Administradores**: Contas do jogo com acesso admin e permissões granulares
- **Economia**: Cash, premium, wallet, GameCP Coins, GoldPoint/PvPPoint
- **Sistemas**: Leilão, quests, battlepass, spin wheel, new player, redeem, guild
- **Itens**: Busca, edição em massa, mapas de itens
- **WooCommerce**: Produtos, pedidos, cupons, categorias
- **Ferramentas**: Logs, sprite sheet, JSON generator, busca avançada

---

## Acessando o Painel Admin

### Requisitos

1. Estar logado no GameCP com conta do jogo
2. Conta estar cadastrada como administrador
3. Ter permissões para a aba desejada

### Como acessar

1. Acesse `seu-site.com/gamecp/`
2. Faça login com a conta do jogo (que é admin)
3. Clique em **"Admin"** no menu lateral
4. Navegue pelas abas disponíveis

---

## Criando Administradores

### Pelo WordPress Admin

1. Acesse **WordPress Admin > DevsBR Panel > GameCP Admin**
2. Clique em **"Adicionar Novo Administrador"**
3. Preencha:
   - **Login do Jogo**: Conta RF Online que será admin
   - **Nível**: Administrador, Moderador ou Suporte
   - **Permissões**: Marque as permissões específicas
4. Salve

### Níveis de Acesso

| Nível | Descrição |
| --- | --- |
| **Administrador** | Acesso total a todas as funções |
| **Moderador** | Acesso a módulos de eventos e jogadores |
| **Suporte** | Apenas visualização, sem edição |

---

## Permissões Disponíveis

| Permissão | Descrição |
| --- | --- |
| `manage_settings` | Configurações sensíveis do sistema |
| `manage_quests` | Criar e editar quests |
| `manage_battlepass` | Configurar passe de batalha |
| `manage_newplayer` | Campanhas de novo jogador |
| `manage_auction` | Gerenciar leilões e venda de personagens |
| `manage_wallet` | Operações de carteira |
| `manage_cash` | Adicionar/remover cash e premium |
| `manage_items` | Editar itens de jogadores |
| `manage_coins` | Gerenciar GameCP Coins |
| `manage_guild` | Gerenciar recompensas de guilda |
| `manage_redeem` | Gerenciar pacotes de resgate |
| `manage_spinwheel` | Configurar roleta de prêmios |
| `manage_council` | Gerenciar conselho/patriarca de raças |
| `view_logs` | Visualizar logs de auditoria |
| `manage_woocommerce` | Gerenciar produtos, pedidos, cupons e categorias da loja |

---

## Abas do Painel Admin por Categoria

### Ferramentas

| Aba | Descrição |
| --- | --- |
| **Dashboard** | Estatísticas rápidas (contas, personagens, online), últimas ações administrativas |
| **Search** | Pesquisa avançada de contas e personagens com ações rápidas |
| **History Logs** | Busca de logs de itens via API com filtros e agrupamento inteligente |
| **JSON Generator** | Geração de arquivos JSON para configurações do sistema |
| **Sprite Sheet** | Upload e processamento de arquivos .SPR para ícones de itens |

### Itens e Inventário

| Aba | Descrição |
| --- | --- |
| **Items** | Edição em massa de inventário e equipamentos com preview |
| **Search Items** | Busca avançada de itens por código, nome ou atributos |
| **Maps** | Mapas de itens do jogo para referência e configuração |

### Economia

| Aba | Descrição |
| --- | --- |
| **Cash/Premium** | Adicionar/remover cash, ativar/desativar premium, histórico |
| **GameCP Coins** | Gerenciamento da moeda virtual do painel |
| **Wallet** | Operações administrativas de carteira digital |
| **GoldPoint/PvPPoint** | Gerenciamento de pontos de gold e PvP |

### Sistemas

| Aba | Descrição |
| --- | --- |
| **Auction** | Visualização e auditoria de todos os itens e personagens no leilão |
| **Battlepass** | Gerenciamento de temporadas, níveis e recompensas (Free/Premium) |
| **Quests** | Criação e edição de missões, recompensas e cooldowns |
| **Spin Wheel** | Configuração da roleta: itens, chances e limites |
| **New Player** | Campanhas de boas-vindas, metas e recompensas por categoria |
| **Redeem Admin** | Gerenciamento de pacotes e códigos de resgate |
| **Race Transfer** | Transferência de raça com conversão automática de itens |
| **Guild Rewards** | Configuração de recompensas para guildas |

### Configuração

| Aba | Descrição |
| --- | --- |
| **Config** | Parâmetros gerais do sistema e módulos |
| **2FA Setup** | Configuração e gerenciamento de autenticação de dois fatores |
| **Register** | Configurações de registro de novas contas |
| **Council** | Gerenciamento de membros do conselho do servidor |

### WooCommerce

| Aba | Descrição |
| --- | --- |
| **Products** | CRUD de produtos com campos específicos do GameCP |
| **Novo Produto** | Criação simplificada de produto variável para Redeem |
| **Orders** | Visualização e gerenciamento de pedidos |
| **Coupons** | Criação e gerenciamento de cupons de desconto |
| **Categories** | Organização de categorias da loja |
| **Brands** | Gerenciamento de marcas de produtos |
| **Attributes** | Gerenciamento de atributos e termos de produtos |

---

## Sistema de Logs

Todas as ações administrativas são registradas automaticamente:

| Campo | Descrição |
| --- | --- |
| **Data/Hora** | Quando a ação foi executada |
| **Admin** | Quem executou |
| **Ação** | Tipo de operação |
| **Detalhes** | Informações específicas da ação |
| **IP** | Endereço de origem |

### Tipos de Ações Logadas

- Criação/edição de administradores
- Alterações de configurações
- Operações de cash/premium/coins
- Edição de itens (bulk edit)
- Transferência de raça
- Banimentos
- Operações de wallet
- Gerenciamento de leilão
- Alterações em quests, battlepass e eventos

### Cache de Logs

O dashboard usa cache de **5 minutos** para os logs. Para ver atualizações imediatas, clique no botão **"Atualizar"** no card de últimas ações.

---

## Autenticação 2FA

Administradores são **obrigados** a configurar 2FA:

1. No primeiro login como admin, será solicitada configuração
2. Escaneie o QR Code com Google Authenticator
3. Digite o código de 6 dígitos para confirmar
4. Nas próximas vezes, será solicitado o código no login

---

## Boas Práticas

### Segurança

- Apenas contas **confiáveis** devem ser admin
- Use permissões **mínimas necessárias** para cada cargo
- Verifique **logs regularmente**
- Mantenha **2FA ativo** sempre

### Hierarquia Sugerida

| Cargo | Permissões |
| --- | --- |
| **Dono** | Todas as permissões |
| **GM Chefe** | Quests, Battlepass, New Player, Busca, Cash, Items |
| **GM** | Busca de jogadores, visualização, quests |
| **Suporte** | Apenas visualização |

---

## Solução de Problemas

### Admin não aparece no menu

- Confirme que a conta está cadastrada como admin
- Verifique se o login está correto (case-sensitive)
- Limpe cache do navegador

### Aba não aparece

- Verifique se o módulo correspondente está ativo
- Confirme que o admin tem permissão para a aba
- Alguns módulos requerem configuração adicional

### Logs não aparecem

- Aguarde 5 minutos (cache) ou clique em "Atualizar"
- Verifique se a tabela de logs existe no banco

### 2FA não funciona

- Confirme que o horário do celular está sincronizado
- Tente gerar um novo código
- Peça para outro admin resetar seu 2FA se necessário

---

## Tutoriais Relacionados

- [Visão Geral do GameCP](gamecp-resumo)
- [Instalação e Ativação](gamecp-instalacao)
- [Race Transfer](rt-race-transfer)
- [Conselho (Patriarch)](admin-council)
- [Histórico de Logs](history-logs)
- [Sprite Sheet](sprite-sheet)
- [Quests](quests)
- [Battlepass](battlepass-gamecp)
- [AutoCash](autocash)
- [Loja: Produtos](admin-woo-produtos)
- [Loja: Pedidos](admin-woo-pedidos)
- [Loja: Cupons](admin-woo-cupons)
