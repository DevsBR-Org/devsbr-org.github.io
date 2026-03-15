---
title: Sistema AutoCash
description: Cash automatico por tempo online
layout: default
category: administracao
order: 5
---

# Sistema AutoCash

O AutoCash recompensa jogadores com **cash automatico** por permanecerem online em mapas e regioes configurados. O processamento e feito via cron otimizado, sem necessidade de acao do jogador.

---

## Visao Geral

| Recurso              | Descricao                                       |
| -------------------- | ----------------------------------------------- |
| **Gatilho**          | Tempo online em mapas/regioes especificas        |
| **Recompensa**       | Cash por minuto configuravel                     |
| **Processamento**    | Cron automatico com intervalo configuravel       |
| **Mapas**            | Selecao de mapas e zonas validas                 |
| **Controle**         | Admin define mapas, valores e horarios           |

O jogador nao precisa fazer nada alem de jogar normalmente.

---

## Configuracao (Admin)

A configuracao e feita em duas areas:

### 1. Configuracao Geral (DevsBR Panel)

Acesse **WordPress Admin > DevsBR Panel > Configuracao AutoCash**.

| Opcao                  | Descricao                                      |
| ---------------------- | ---------------------------------------------- |
| **Ativar Sistema**     | Liga/desliga o AutoCash                         |
| **Cash por minuto**    | Quantidade de cash por minuto online             |
| **Batch Size**         | Jogadores processados por ciclo                  |
| **Maximo de Ciclos**   | Ciclos por execucao do cron                      |
| **Tempo Maximo (seg)** | Limite de tempo por execucao                     |
| **Token de Seguranca** | Token unico para chamada do cron                 |

### 2. Configuracao de Mapas e Regioes (GameCP Admin)

No GameCP Admin, configure quais mapas e zonas contam para o AutoCash:

| Campo              | Descricao                                       |
| ------------------ | ----------------------------------------------- |
| **Mapa**           | Codigo do mapa (ex.: mapas de PVP)               |
| **Coordenadas**    | X, Y, Z da regiao                                |
| **Raio**           | Area de influencia ao redor das coordenadas      |
| **Horario**        | Janela de horario (inicio/fim) para o AutoCash   |

### Suporte a Mapas

O sistema permite controle granular:

- **So ganha AutoCash em mapas de PVP**: cadastre apenas mapas PVP.
- **So conta tempo na base da raca**: defina regioes com coordenadas da base.
- **Horarios especificos**: ative o AutoCash apenas em determinados periodos.
- **Ignorar mapas AFK**: nao cadastre mapas onde jogadores ficam parados.

---

## Funcionamento

1. O servidor registra o **tempo de jogo** dos personagens.
2. O cron, ao ser acionado, consulta:
   - Tempo jogado por personagem.
   - Mapas/regioes onde esteve.
   - Tempo ainda nao convertido em cash.
3. Para minutos "nao pagos" em areas validas:
   - Calcula o cash devido.
   - Atualiza controle interno (evita pagamento duplicado).
   - Credita o cash na conta do jogador.

---

## Cron Otimizado

O AutoCash utiliza um **cron seguro** com token unico para evitar execucoes nao autorizadas.

### Configuracao do Cron

Na tela de Configuracao AutoCash, o sistema exibe:

- **Token de seguranca** unico.
- **URL completa do cron** com o token.
- **Comandos prontos** para copiar:

| Metodo      | Descricao                                       |
| ----------- | ----------------------------------------------- |
| **wget**    | Comando wget para Linux                          |
| **curl**    | Comando curl para chamada HTTP                   |
| **crontab** | Linha pronta para adicionar ao crontab           |

### Otimizacao de Performance

| Parametro          | Recomendacao                                   |
| ------------------ | ---------------------------------------------- |
| **Intervalo**      | A cada 1 minuto (recomendado)                   |
| **Batch Size**     | Ajuste conforme numero de jogadores online       |
| **Maximo Ciclos**  | Evite valores muito altos em servidores lotados  |
| **Tempo Maximo**   | Defina limite para nao travar o cron             |

### Cloudflare

Se usar Cloudflare, crie uma regra de **Skip** para o caminho do cron, evitando bloqueio por firewall.

---

## Visao do Jogador

O jogador nao interage diretamente com o AutoCash:

- Joga normalmente nos mapas configurados.
- O cash e creditado automaticamente na conta.
- No GameCP, o saldo aparece atualizado nos modulos que consomem cash.

Nao ha tela especifica para o jogador; o sistema e transparente.

---

## Boas Praticas

- Comece com uma **taxa moderada** de cash por minuto e ajuste conforme a economia.
- Use mapas e regioes para evitar AFK farming em areas seguras.
- Combine com **Loja**, **Wallet** e **Battlepass** para dar utilidade ao cash.
- Monitore os primeiros dias: verifique se o total gerado e equilibrado.
- Ajuste batch size e ciclos conforme a carga do servidor.
- Mantenha o cron rodando a cada minuto para distribuicao uniforme.
