---
title: Autenticacao 2FA
description: Autenticacao de dois fatores para administradores
layout: default
category: seguranca
order: 1
---

# Autenticacao 2FA

O sistema de **Autenticacao de Dois Fatores (2FA)** adiciona uma camada extra de seguranca para administradores do GameCP. E opcional para admins regulares, mas pode ser configurado como obrigatorio com setup no primeiro login.

---

## Visao Geral

| Recurso              | Descricao                                       |
| -------------------- | ----------------------------------------------- |
| **Tipo**             | TOTP (Time-based One-Time Password)              |
| **Apps compativeis** | Google Authenticator, Authy, Microsoft Auth      |
| **Obrigatoriedade**  | Configuravel (opcional ou obrigatorio)           |
| **QR Code**          | Gerado automaticamente para cada admin           |
| **Codigos de backup**| Codigos de emergencia para recuperacao            |
| **Lista de exclusao**| Admins especificos podem ser excluidos            |

---

## Por que Usar 2FA

- **Seguranca extra**: mesmo com senha vazada, a conta fica protegida.
- **Padrao de mercado**: usado por bancos, redes sociais e servicos criticos.
- **Auditoria**: garante que e o admin real fazendo login.

---

## Configuracao Obrigatoria no Primeiro Login

Quando o 2FA esta configurado como obrigatorio:

1. O admin faz login no GameCP com usuario e senha.
2. O sistema detecta que o 2FA **nao esta configurado**.
3. O admin e **redirecionado automaticamente** para a tela de configuracao.
4. Nao e possivel acessar nenhuma outra area ate concluir o setup.

### Passo a Passo da Configuracao

1. **Abra o app autenticador** no celular (Google Authenticator, Authy ou similar).
2. **Escaneie o QR Code** exibido na tela do GameCP.
3. O app registra a conta e comeca a gerar codigos de 6 digitos.
4. **Digite o codigo atual** (6 digitos) no campo de verificacao.
5. **Confirme** para ativar o 2FA.
6. O sistema gera **codigos de backup** -- salve-os em local seguro.

### Geracao do QR Code

- O QR Code e gerado automaticamente e e **unico por admin**.
- Contem a chave secreta TOTP vinculada a conta.
- Nao compartilhe o QR Code com outras pessoas.
- Se precisar reconfigurar, um novo QR Code sera gerado.

### Codigos de Backup

Apos ativar o 2FA, o sistema fornece codigos de backup:

- Cada codigo pode ser usado **uma unica vez**.
- Servem para login quando o celular nao esta disponivel.
- **Guarde em local seguro** (gerenciador de senhas, papel trancado).
- Se todos os codigos forem usados, solicite novos ao sistema.

---

## Login com 2FA Ativo

1. Faca login com usuario e senha normalmente.
2. O sistema solicita o **codigo 2FA**.
3. Abra o app autenticador e digite o codigo atual (6 digitos).
4. Acesso liberado.

### Codigo Invalido

| Problema                        | Solucao                                   |
| ------------------------------- | ----------------------------------------- |
| Codigo nao aceito               | Verifique se o horario do celular esta sincronizado |
| Codigo expirado                 | Aguarde o proximo (muda a cada 30 segundos) |
| App com conta errada            | Confirme que esta usando a conta correta   |

---

## Administracao do 2FA

### Desativar 2FA de um Admin

Em **Admin > Configuracoes > 2FA**:

1. Selecione o administrador.
2. Clique em **"Desativar 2FA"**.
3. Confirme a acao.

> Use apenas em emergencias. A conta fica desprotegida ate reconfigurar.

### Lista de Exclusao do 2FA Obrigatorio

Alguns admins podem ser excluidos da obrigatoriedade:

1. Acesse **Admin > Admins**.
2. Edite o administrador desejado.
3. Marque **"Excluir do 2FA obrigatorio"**.
4. Salve.

| Cenario                          | Recomendacao                              |
| -------------------------------- | ----------------------------------------- |
| Admin com acesso limitado        | Pode ser excluido com cautela              |
| Admin com acesso total           | Manter 2FA obrigatorio                     |
| Conta de servico/bot             | Avaliar caso a caso                        |

> Use a exclusao com cautela. Reduz a seguranca da conta excluida.

---

## Solucao de Problemas

### Perdi o celular

1. Use um **codigo de backup** para fazer login.
2. Acesse as configuracoes de 2FA e reconfigure em um novo dispositivo.
3. Se nao tiver codigos de backup, peca para outro admin desativar o 2FA.

### Codigo sempre invalido

1. Verifique se o **horario do celular** esta correto e sincronizado com a internet.
2. Tente outro app autenticador.
3. Se persistir, desative e reconfigure o 2FA.

### Nao consigo acessar de jeito nenhum

1. Use codigos de backup.
2. Peca para outro admin desativar seu 2FA temporariamente.
3. Reconfigure em um novo dispositivo.

---

## Boas Praticas

- **Mantenha o app seguro**: proteja o celular com senha/biometria.
- **Salve os codigos de backup**: em gerenciador de senhas ou local seguro.
- **Nao compartilhe o QR Code**: cada admin deve ter o seu proprio.
- **Sincronize o horario**: mantenha o celular com hora automatica ativada.
- **Mantenha 2FA obrigatorio** para todos os admins com acesso privilegiado.
