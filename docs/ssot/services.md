# Serviços (SSOT)

## Objetivo

Este documento descreve os serviços atualmente considerados parte integrante do Cravo Homelab.

Cada serviço deve possuir:

- uma função clara;
- uma justificação para a sua existência;
- dependências documentadas;
- um proprietário funcional.

Um serviço sem propósito documentado deve ser considerado candidato a remoção.

---

# Filosofia dos Serviços

Os serviços existem para resolver problemas.

Não existem para demonstrar tecnologias.

Antes de adicionar um novo serviço, deve responder-se às seguintes perguntas:

1. Que problema resolve?
2. Já existe um serviço que resolva esse problema?
3. A manutenção futura justifica o benefício obtido?
4. A família irá efetivamente utilizá-lo?

---

# Mapa Geral da Plataforma

```text
                 Authentik
                     │
                     ▼

     Nextcloud ─── OnlyOffice
          │
          ├── Talk
          │
          ▼

     PostgreSQL

          ▲
          │

Paperless     Home Assistant

          │
          ▼

      AdGuard

          │
          ▼

       NPM

          │
          ▼

     WireGuard

          │
          ▼

    Uptime Kuma
```

---

# Serviços em Produção

---

## Home Assistant

### Estado

VALIDADO

### Função

Plataforma central de automação doméstica.

### Responsabilidades

- automações;
- sensores;
- iluminação;
- notificações;
- integração de dispositivos;
- monitorização doméstica.

### Dependências

- PostgreSQL
- Rede local
- AdGuard
- Equipamentos IoT

### Proprietário Funcional

Habitação

---

## PostgreSQL

### Estado

PROVÁVEL

### Função

Motor central de bases de dados.

### Responsabilidades

Armazenar dados estruturados de:

- Home Assistant;
- Nextcloud;
- Paperless;
- Authentik.

### Princípio

Bases de dados dispersas devem ser evitadas.

Sempre que possível deve existir uma infraestrutura relacional centralizada.

---

## Nextcloud

### Estado

PROVÁVEL

### Função

Nuvem privada da família.

### Responsabilidades

- armazenamento de ficheiros;
- colaboração;
- sincronização;
- partilha de documentos;
- gestão de fotografias.

### Utilizadores

Família

---

## OnlyOffice

### Estado

PROVÁVEL

### Função

Edição colaborativa de documentos.

### Dependência Primária

Nextcloud

### Observação

Não é considerado um serviço autónomo.

Existe exclusivamente para complementar o Nextcloud.

---

## Nextcloud Talk

### Estado

PROVÁVEL

### Função

Mensagens e comunicações privadas.

### Dependência Primária

Nextcloud

### Utilizadores

Família

---

## Paperless-ngx

### Estado

PROVÁVEL

### Função

Arquivo documental permanente.

### Responsabilidades

- OCR;
- indexação;
- arquivo;
- pesquisa documental.

### Princípio

Documentos importantes não devem depender de pastas aleatórias em discos.

---

## Authentik

### Estado

PROVÁVEL

### Função

Gestão unificada de identidade.

### Responsabilidades

- autenticação;
- autorização;
- Single Sign-On;
- integração de acessos.

### Benefício

Reduz duplicação de credenciais.

---

## AdGuard Home

### Estado

PROVÁVEL

### Função

DNS interno.

### Responsabilidades

- resolução de nomes;
- domínio interno;
- filtragem DNS.

### Criticidade

Muito elevada.

Uma falha neste serviço afeta a utilização normal da infraestrutura.

---

## Nginx Proxy Manager

### Estado

PROVÁVEL

### Função

Publicação controlada de serviços.

### Responsabilidades

- reverse proxy;
- certificados;
- encaminhamento interno.

### Benefício

Eliminação de portas explícitas para os utilizadores.

---

## WireGuard

### Estado

PROVÁVEL

### Função

Acesso remoto seguro.

### Responsabilidades

- VPN;
- acesso remoto;
- extensão da rede doméstica.

### Princípio

Serviços não devem ser expostos diretamente à Internet.

---

## Uptime Kuma

### Estado

PROVÁVEL

### Função

Monitorização.

### Responsabilidades

- disponibilidade;
- alertas;
- validação de serviços.

### Benefício

Deteção precoce de falhas.

---

# Serviços em Avaliação

---

## Nextcloud Talk

Estado:

Homologação contínua.

---

## OnlyOffice

Estado:

Homologação contínua.

---

# Serviços Históricos

Serviços identificados em documentação anterior:

- Plex
- Samba
- Radarr
- Sonarr
- Prowlarr
- qBittorrent
- Heimdall
- Portainer

O estado atual destes serviços deverá ser validado posteriormente.

Até validação futura não fazem parte da SSOT atual.

---

# Criticidade por Serviço

## Nível Crítico

Falha com impacto imediato.

- Home Assistant
- PostgreSQL
- AdGuard
- WireGuard

---

## Nível Importante

Falha tolerável temporariamente.

- Nextcloud
- Paperless
- Authentik

---

## Nível Conveniência

Falha sem impacto estrutural.

- Uptime Kuma
- OnlyOffice
- Talk

---

# Política de Inclusão

Um serviço só deve integrar a SSOT quando:

- estiver operacional;
- tiver um propósito definido;
- possuir documentação;
- justificar o custo de manutenção.

Caso contrário deverá permanecer em:
    
docs/history/
ou

docs/lab/
até maturidade suficiente.

---

# Regra de Atualização

Sempre que um serviço for:

- adicionado;
- removido;
- substituído;
- consolidado;

este documento deve ser atualizado e a alteração registada em:

```text
docs/ssot/change-log.md
```
