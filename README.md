# GameCP Docs

Documentacao oficial do **GameCP** — painel de controle para servidores de RF Online integrado ao WordPress/WooCommerce.

Site: [devsbr-org.github.io](https://devsbr-org.github.io)

---

## Sobre

Este repositorio contem a documentacao completa do GameCP v1.6.0, cobrindo todos os modulos do jogador e do painel administrativo. O site e gerado com **Jekyll** e hospedado no **GitHub Pages**.

---

## Estrutura

```
├── _config.yml              # Configuracao do Jekyll
├── _layouts/
│   ├── default.html         # Layout principal com sidebar
│   └── portal.html          # Landing page
├── style/
│   └── LOGO2.png            # Logo DevsBR
├── docs.md                  # Pagina inicial da documentacao
├── index.md                 # Portal de entrada
└── *.md                     # Paginas de documentacao (36+)
```

---

## Modulos Documentados

### Primeiros Passos
- Visao Geral do GameCP
- Instalacao e Ativacao

### Seguranca
- Autenticacao 2FA
- Verificacao de Email

### Modulos do Jogador
- Inventario
- GameCP Coins
- Carteira (Wallet)
- Loja e Checkout
- Leilao
- Venda de Personagens
- Guild (Recompensas)
- Quests
- Battle Pass
- Spin Wheel
- Redeem
- New Player

### Painel Admin
- Dashboard
- Buscar Jogadores
- Enviar Itens
- Race Transfer
- Conselho (Patriarch System)
- Configuracoes
- Registro

### Economia (Admin)
- Cash e Premium (interface unificada)
- Wallet
- GameCP Coins
- AutoCash
- Mapas (AutoCash)

### Loja (WooCommerce)
- Produtos
- Novo Produto (Redeem Variavel)
- Pedidos
- Cupons
- Categorias
- Marcas
- Atributos

### Ferramentas Admin
- Historico de Logs
- Pesquisar Itens
- JSON Generator
- Sprite Sheet

---

## Tecnologias

- **Jekyll** com tema Cayman (remote theme)
- **GitHub Pages** para hospedagem
- **Markdown** (kramdown/GFM) para conteudo
- **CSS** customizado com tema dark

---

## Desenvolvimento Local

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

Acesse `http://localhost:4000` no navegador.

---

## Licenca

Uso interno DevsBR. Todos os direitos reservados.
