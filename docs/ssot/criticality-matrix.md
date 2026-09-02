# Matriz de Criticidade

## Objetivo

Este documento define a criticidade dos sistemas, serviços, equipamentos e dados do Cravo Homelab.

O seu objetivo é estabelecer prioridades objetivas para:

- recuperação;
- manutenção;
- investimento;
- monitorização;
- documentação.

Nem todos os componentes possuem a mesma importância.

Quando existem recursos limitados, deve ser dada prioridade aos elementos mais críticos.

---

# Filosofia

Os recursos são finitos.

O tempo é finito.

A atenção do administrador é finita.

Por isso é necessário definir claramente o que é:

- crítico;
- importante;
- conveniente;
- opcional.

---

# Níveis de Criticidade

## Nível 1 — Crítico

A falha provoca impacto imediato ou significativo.

A recuperação deve ser prioritária.

---

## Nível 2 — Importante

A falha é incómoda.

O sistema continua funcional.

---

## Nível 3 — Conveniência

A falha tem impacto reduzido.

---

## Nível 4 — Experimental

Sem impacto operacional.

---

# Dados

## Arquivo Documental

### Sistema

Paperless

### Criticidade

Nível 1

### Justificação

Contém documentação legal, fiscal e histórica.

---

## Fotografias Familiares

### Sistema

Nextcloud

### Criticidade

Nível 1

### Justificação

Conteúdo insubstituível.

---

## Documentação Técnica

### Sistema

GitHub

### Criticidade

Nível 1

### Justificação

Memória institucional do projeto.

---

# Infraestrutura

## Lenovo Host

### Criticidade

Nível 1

### Justificação

Executa a maioria dos serviços.

---

## NAS QNAP

### Criticidade

Nível 1

### Justificação

Armazenamento principal.

---

## ER605

### Criticidade

Nível 1

### Justificação

Gateway principal.

---

## Switch Principal

### Criticidade

Nível 2

---

## EAP653

### Criticidade

Nível 2

---

# Serviços

## PostgreSQL

### Criticidade

Nível 1

### Impacto

Afeta múltiplos serviços.

---

## AdGuard Home

### Criticidade

Nível 1

### Impacto

A resolução de nomes internos deixa de funcionar.

---

## Home Assistant

### Criticidade

Nível 1

### Impacto

Perda de automações.

---

## WireGuard

### Criticidade

Nível 2

### Impacto

Perda de acesso remoto.

---

## Nextcloud

### Criticidade

Nível 1

### Impacto

Documentos ativos indisponíveis.

---

## Paperless

### Criticidade

Nível 1

### Impacto

Arquivo documental indisponível.

---

## Authentik

### Criticidade

Nível 1

### Impacto

Autenticação comprometida.

---

## Nginx Proxy Manager

### Criticidade

Nível 2

---

## Uptime Kuma

### Criticidade

Nível 3

---

## OnlyOffice

### Criticidade

Nível 3

---

## Talk

### Criticidade

Nível 3

---

# Automação

## Sistema de Rega

### Criticidade

Nível 1

Durante períodos de utilização intensiva.

---

## Sensores Ambientais

### Criticidade

Nível 2

---

## Robôs Aspiradores

### Criticidade

Nível 3

---

# Conhecimento

## SSOT

### Criticidade

Nível 1

---

## ADRs

### Criticidade

Nível 2

---

## História

### Criticidade

Nível 2

---

## Manuais Familiares

### Criticidade

Nível 2

---

# Ordem de Recuperação

## Prioridade Máxima

```text
Energia
Rede
Armazenamento
```

---

## Segunda Prioridade

```text
PostgreSQL
AdGuard
Authentik
```

---

## Terceira Prioridade

```text
Nextcloud
Paperless
Home Assistant
```

---

## Quarta Prioridade

```text
WireGuard
NPM
```

---

## Quinta Prioridade

```text
Uptime Kuma
OnlyOffice
Talk
```

---

# Revisão

Esta matriz deve ser revista:

- após migrações;
- após alterações arquiteturais;
- após incidentes importantes;
- durante auditorias anuais.

---

# Regra Fundamental

Uma funcionalidade popular não é necessariamente crítica.

A criticidade é determinada pelo impacto da perda e não pela frequência de utilização.

---

# Definição de Sucesso

Qualquer pessoa deve conseguir determinar rapidamente:

- o que proteger primeiro;
- o que recuperar primeiro;
- onde investir esforço documental;

consultando apenas esta matriz.
