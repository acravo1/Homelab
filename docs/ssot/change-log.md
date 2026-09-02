# Change Log do Cravo Homelab

## Objetivo

Este documento regista todas as alterações relevantes efetuadas na infraestrutura.

O objetivo não é substituir o Git.

O objetivo é registrar decisões arquiteturais importantes que explicam a evolução do sistema.

Este documento responde às perguntas:

- O que mudou?
- Quando mudou?
- Porque mudou?
- Qual foi o impacto?

---

# Regras de Registo

Uma entrada deve ser criada quando ocorre uma alteração que afete:

- hardware;
- armazenamento;
- rede;
- autenticação;
- backup;
- automação;
- arquitetura dos serviços.

Alterações menores podem ser registadas apenas no histórico do Git.

---

# Formato das Entradas

## Data

AAAA-MM-DD

## Categoria

- Hardware
- Storage
- Network
- Services
- Security
- Documentation
- Home Assistant
- Other

## Alteração

Descrição objetiva.

## Motivo

Razão da alteração.

## Impacto

Consequências da alteração.

---

# Entradas

---

## 2026-06-25

### Categoria

Hardware

### Alteração

Aquisição de Lenovo ThinkCentre M710 SFF.

### Motivo

Substituição da infraestrutura anterior.

### Impacto

Criação da plataforma base do Homelab.

### Estado

VALIDADO

---

## 2026-XX-XX

### Categoria

Storage

### Alteração

Transição de armazenamento baseado em disco USB para NAS QNAP.

### Motivo

Maior capacidade e fiabilidade.

### Impacto

Centralização do armazenamento familiar.

### Estado

PROVÁVEL

---

## 2026-XX-XX

### Categoria

Authentication

### Alteração

Introdução do Authentik.

### Motivo

Unificação da autenticação.

### Impacto

Redução de múltiplas credenciais.

### Estado

PROVÁVEL

---

## 2026-XX-XX

### Categoria

Network

### Alteração

Implementação de acesso remoto através de WireGuard.

### Motivo

Eliminar exposição direta dos serviços à Internet.

### Impacto

Melhoria significativa da segurança.

### Estado

PROVÁVEL

---

## 2026-XX-XX

### Categoria

Storage

### Alteração

Implementação do Paperless-ngx.

### Motivo

Centralização do arquivo documental.

### Impacto

Digitalização e indexação dos documentos familiares.

### Estado

PROVÁVEL

---

## 2026-XX-XX

### Categoria

Network

### Alteração

Implementação de DNS interno através do AdGuard Home.

### Motivo

Simplificar o acesso aos serviços.

### Impacto

Introdução dos domínios internos.

Exemplos:

- nextcloud.lenovo
- paperless.lenovo
- homeassistant.lenovo

### Estado

PROVÁVEL

---

## 2026-09

### Categoria

Documentation

### Alteração

Início da reconstrução da Fonte Única da Verdade (SSOT).

### Motivo

Existência de documentação histórica divergente.

### Impacto

Criação de um sistema formal de governação documental.

### Estado

VALIDADO

---

# Registo de Alterações Futuras

Adicionar novas entradas acima das existentes.

As entradas mais recentes devem surgir primeiro.

---

# O que NÃO deve entrar aqui

Não registar:

- pequenas correções;
- alterações cosméticas;
- atualizações rotineiras;
- mudanças sem impacto arquitetural.

Para esse tipo de detalhe deve utilizar-se o histórico Git.

---

# Definição de Sucesso

Uma pessoa que nunca viu o sistema deve conseguir:

- compreender a evolução da infraestrutura;
- perceber as principais decisões técnicas;
- identificar alterações críticas;
- reconstruir o contexto histórico do projeto.

Este documento existe para preservar a história viva do Homelab.
