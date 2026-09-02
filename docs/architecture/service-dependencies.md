# Dependências entre Serviços

## Objetivo

Este documento descreve as relações entre os vários componentes do Cravo Homelab.

O objetivo é compreender:

- quais os serviços críticos;
- quais as dependências existentes;
- qual o impacto da falha de cada componente;
- qual a ordem correta de recuperação.

Este documento complementa:

```text
docs/ssot/services.md
```

---

# Visão Geral

```text
                    Internet
                        │
                        ▼

                    WireGuard
                        │
                        ▼

                  AdGuard Home
                        │
                        ▼

             Nginx Proxy Manager
                        │
                        ▼

                   Authentik
             ┌──────────┼──────────┐
             │          │          │
             ▼          ▼          ▼

         Nextcloud   Paperless  Outros

             │
             ▼

         OnlyOffice
             │
             ▼

       Nextcloud Talk

             ▲
             │

       PostgreSQL
             ▲
             │

      Home Assistant
```

---

# Níveis de Dependência

## Nível 0

Infraestrutura Física

### Componentes

- Energia
- Rede
- Lenovo
- NAS QNAP

Sem estes componentes nada funciona.

---

## Nível 1

Serviços Fundamentais

### PostgreSQL

Responsável pelas bases de dados.

Consumidores:

- Home Assistant
- Nextcloud
- Paperless
- Authentik

---

### AdGuard Home

Responsável por:

- DNS
- resolução interna

Consumidores:

- toda a rede

---

# Nível 2

Identidade

## Authentik

Função:

Centralização da autenticação.

Consumidores:

- Nextcloud
- Talk
- futuras integrações

---

# Nível 3

Serviços de Dados

## Nextcloud

Função:

Armazenamento ativo.

Dependências:

- PostgreSQL
- Authentik
- Rede

---

## Paperless

Função:

Arquivo documental.

Dependências:

- PostgreSQL
- Rede
- Armazenamento

---

## Home Assistant

Função:

Automação.

Dependências:

- PostgreSQL
- Sensores
- Rede

---

# Nível 4

Serviços Complementares

## OnlyOffice

Dependência:

Nextcloud

Se falhar:

Os documentos continuam acessíveis.

Perde-se apenas edição integrada.

---

## Nextcloud Talk

Dependência:

Nextcloud

Se falhar:

A comunicação fica indisponível.

Os ficheiros permanecem acessíveis.

---

## Uptime Kuma

Dependência:

Rede

Se falhar:

Perde-se monitorização.

Não existe impacto direto na produção.

---

# Impacto de Falhas

## Falha PostgreSQL

Impacto:

Muito elevado.

Afeta:

- Home Assistant
- Nextcloud
- Paperless
- Authentik

Criticidade:

Crítica.

---

## Falha AdGuard

Impacto:

Elevado.

Afeta:

- resolução de nomes;
- domínios internos.

Criticidade:

Crítica.

---

## Falha Authentik

Impacto:

Elevado.

Afeta:

- autenticação;
- SSO.

Criticidade:

Elevada.

---

## Falha Nextcloud

Impacto:

Elevado.

Afeta:

- acesso a documentos ativos;
- sincronização;
- colaboração.

Criticidade:

Elevada.

---

## Falha Paperless

Impacto:

Moderado.

Afeta:

- consulta documental.

Criticidade:

Elevada.

---

## Falha Home Assistant

Impacto:

Elevado.

Afeta:

- automações;
- dashboards;
- monitorização.

Criticidade:

Crítica.

---

# Ordem de Recuperação

Em caso de desastre seguir:

## 1

Infraestrutura Física

- Energia
- Rede
- Lenovo
- NAS

---

## 2

PostgreSQL

---

## 3

AdGuard

---

## 4

Authentik

---

## 5

Home Assistant

---

## 6

Nextcloud

---

## 7

Paperless

---

## 8

OnlyOffice

---

## 9

Talk

---

## 10

Uptime Kuma

---

# Regra Fundamental

Antes de remover, alterar ou atualizar um serviço, consultar sempre este documento.

Uma alteração num serviço pode afetar múltiplos componentes dependentes.

---

# Definição de Sucesso

Qualquer pessoa deve conseguir compreender:

- o papel de cada serviço;
- as dependências existentes;
- o impacto de uma falha;

consultando exclusivamente este documento.
