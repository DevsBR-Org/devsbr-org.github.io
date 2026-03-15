---
title: GameCP - Visão Geral
description: Painel web completo para servidores RF Online
layout: default
category: introducao
order: 1
---

# GameCP v1.6.0 – Visão Geral

O **GameCP** é um painel web completo e moderno para servidores **RF Online**, integrado ao WordPress através do plugin DevsBR. Com mais de **40 páginas para jogadores** e **28+ abas administrativas**, oferece uma experiência profissional para todas as operações do servidor.

---

## Visão Geral

O GameCP é um **painel de controle web** que conecta seu site WordPress diretamente ao banco de dados do servidor RF Online. Funciona como um hub central onde jogadores e administradores gerenciam todas as operações — **tudo pelo navegador**, em PC ou celular, sem precisar abrir o cliente do jogo.

---

## Principais Funcionalidades

### Conta e Personagem

| Funcionalidade | Descrição |
| --- | --- |
| **Dashboard** | Visão geral da conta com estatísticas e informações |
| **Personagens** | Lista completa de personagens com detalhes e stats |
| **Inventário** | Visualização e gestão de itens equipados e no inventário |
| **Guild** | Informações da guilda, membros e recompensas |

### Economia e Loja

| Funcionalidade | Descrição |
| --- | --- |
| **Loja** | Catálogo de produtos com carrinho integrado ao WooCommerce |
| **Wallet** | Carteira digital para pagamentos, saques e transferências |
| **GameCP Coins** | Moeda virtual do painel com diversas formas de obtenção |
| **Leilão** | Mercado de itens entre jogadores com preço fixo |
| **Venda de Personagens** | Marketplace para venda de personagens com transferência automática |

### Eventos e Engajamento

| Funcionalidade | Descrição |
| --- | --- |
| **Quests** | Missões com recompensas, cooldowns e requisitos |
| **Battlepass** | Passe de batalha com trilhas Free e Premium por temporada |
| **Spin Wheel** | Roleta de prêmios com chances configuráveis |
| **New Player** | Recompensas e metas para novos jogadores |
| **Redeem** | Resgate de pacotes e códigos promocionais |

### Administração (28+ abas)

| Categoria | Abas |
| --- | --- |
| **Itens e Inventário** | Items, Search Items, Maps |
| **Economia** | Cash/Premium, GameCP Coins, Wallet, GoldPoint/PvPPoint |
| **Sistemas** | Auction, Battlepass, Quests, Spin Wheel, New Player, Redeem, Race Transfer, Guild Rewards |
| **Configuração** | Config, 2FA Setup, Register, Council |
| **WooCommerce** | Orders, Products, Coupons, Categories e mais |
| **Ferramentas** | History Logs, JSON Generator, Sprite Sheet, Search, Dashboard |

---

## Stack Tecnológica

| Componente | Tecnologia |
| --- | --- |
| **Backend** | PHP 8.2+ |
| **Frontend** | Bootstrap 5, jQuery |
| **CMS** | WordPress 5.0+ |
| **E-commerce** | WooCommerce 5.0+ |
| **Banco de Dados** | SQL Server (RF Online) via PDO SQLSRV ou DBLIB |
| **Segurança** | 2FA, Cloudflare Turnstile, Nonces/CSRF |

---

## Segurança

| Recurso | Descrição |
| --- | --- |
| **Autenticação 2FA** | Obrigatória para administradores via Google Authenticator |
| **Cloudflare Turnstile** | Proteção contra bots no login e formulários |
| **Verificação de Email** | Validação de email para novas contas |
| **Proteção por HWID** | Controle contra múltiplas contas |
| **Logs de Auditoria** | Registro de todas as ações administrativas com IP |
| **Nonces e CSRF** | Proteção em todos os formulários e requisições AJAX |

---

## Sistemas de Proteção Suportados

O GameCP é compatível com os principais sistemas de proteção para RF Online:

- **Odin**
- **DevCorp**
- **HGK**
- **SirinGuard**

---

## Integrações

### WooCommerce

- Loja completa dentro do GameCP com carrinho integrado
- Entrega automática de itens no jogo após pagamento
- Suporte a cupons, descontos e múltiplos métodos de pagamento
- Criação automática de produtos para leilão e venda de personagens

### APIs Externas

- API de Logs para histórico de itens
- Integração com gateways de pagamento
- Suporte a multi-moeda

---

## Por que usar o GameCP?

| Beneficio | Descrição |
| --- | --- |
| **Profissionalismo** | Interface moderna e responsiva com Bootstrap 5 |
| **Monetização** | Loja + Wallet + Leilão + Eventos integrados |
| **Automação** | Entrega automática de itens, menos trabalho manual |
| **Engajamento** | Quests, Battlepass, Spin Wheel mantêm jogadores ativos |
| **Segurança** | 2FA, HWID, Turnstile, logs de auditoria |
| **Flexibilidade** | Módulos podem ser ativados/desativados individualmente |
| **Escalabilidade** | 40+ páginas para jogadores, 28+ abas admin |

---

## Próximos Passos

1. [Instalação e Ativação](gamecp-instalacao)
2. [Painel Admin e Permissões](gamecp-admin-panel)
3. [Loja e Checkout](gamecp-shop-checkout)
4. [Carteira (Wallet)](wallet)

---

## Tutoriais Relacionados

- [Índice da Documentação](index)
- [Instalação e Ativação](gamecp-instalacao)
- [Painel Admin](gamecp-admin-panel)
- [Autenticação 2FA](2fa-seguranca)
