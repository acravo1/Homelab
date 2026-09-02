# Mapa de Conhecimento do Cravo Homelab

## Objetivo

Este documento funciona como o índice principal de toda a documentação do Cravo Homelab.

O seu objetivo é permitir localizar rapidamente:

- informação técnica;
- informação histórica;
- procedimentos;
- documentação familiar;
- princípios arquiteturais;
- documentação operacional.

Sempre que existir dúvida sobre onde procurar informação, este deverá ser o primeiro documento a consultar.

---

# Estrutura Geral

```text
docs/

├── philosophy/
├── architecture/
├── ssot/
├── operations/
├── services/
├── family/
├── standards/
└── history/
```

---

# Philosophy

Descreve os princípios fundamentais que orientam o projeto.

## Documentos

### 00-principios-fundamentais.md

Constituição do Cravo Homelab.

---

### 01-interpretacao-dos-principios.md

Interpretação detalhada dos princípios.

---

### 02-glossario.md

Glossário de termos oficiais.

---

### 03-regras-de-ouro.md

Regras operacionais essenciais.

---

### 04-roadmap-e-visao.md

Visão estratégica de longo prazo.

---

### 05-carta-do-administrador.md

Carta histórica para futuros administradores.

---

# Architecture

Descreve a arquitetura lógica da infraestrutura.

## Documentos

### architecture-principles.md

Princípios arquiteturais.

---

### service-dependencies.md

Dependências entre serviços.

---

### data-flow.md

Fluxos de informação.

---

# SSOT

Fonte Única da Verdade.

Descreve apenas o estado atual.

## Documentos

### hardware.md

Hardware em produção.

---

### storage.md

Arquitetura de armazenamento.

---

### network.md

Rede e conectividade.

---

### services.md

Serviços ativos.

---

### users-and-access.md

Identidade e acessos.

---

### backup-and-recovery.md

Estratégia de recuperação.

---

### asset-inventory.md

Inventário completo.

---

### house-map.md

Localização física dos ativos.

---

### criticality-matrix.md

Criticidade dos componentes.

---

### change-log.md

Histórico oficial de alterações.

---

# Operations

Procedimentos operacionais.

## Documentos

### rebuild-from-zero.md

Reconstrução integral.

---

### maintenance.md

Manutenção periódica.

---

### lifecycle-management.md

Gestão do ciclo de vida.

---

### new-service-onboarding.md

Integração de novos serviços.

---

### decision-records.md

ADRs e decisões arquiteturais.

---

### contributing.md

Contribuição documental.

---

### documentation-pipeline.md

Pipeline documental.

---

### document-audit-process.md

Processo de auditoria.

---

### checklists.md

Checklists operacionais.

---

# Services

Documentação individual dos serviços.

## Serviços

### home-assistant.md

Automação residencial.

---

### postgresql.md

Base de dados central.

---

### nextcloud.md

Armazenamento colaborativo.

---

### paperless.md

Arquivo documental.

---

### authentik.md

Identidade.

---

### adguard.md

DNS.

---

### wireguard.md

VPN.

---

### nginx-proxy-manager.md

Publicação de serviços.

---

### uptime-kuma.md

Monitorização.

---

# Family

Documentação orientada aos utilizadores finais.

## Documentos

### guia-familia.md

Introdução geral.

---

### nextcloud.md

Manual do Nextcloud.

---

### paperless.md

Manual do Paperless.

---

### talk.md

Manual do Nextcloud Talk.

---

### home-assistant.md

Manual do Home Assistant.

---

### faq.md

Perguntas frequentes.

---

# Standards

Normas de governação.

## Documentos

### naming-conventions.md

Convenções de nomenclatura.

---

### document-classification.md

Classificação documental.

---

# History

Preservação histórica.

## Documentos

### architecture-evolution.md

Evolução da infraestrutura.

---

### palmela-to-castelo-branco.md

Relatório da migração.

---

### lessons-learned.md

Conhecimento adquirido.

---

### retired-assets.md

Equipamentos aposentados.

---

# Percursos Recomendados

## Sou Utilizador da Família

Ler:

```text
family/
```

---

## Sou Administrador

Ler:

```text
philosophy/
ssot/
operations/
services/
```

---

## Quero Recuperar a Infraestrutura

Ler:

```text
ssot/
operations/
services/
```

---

## Quero Compreender a Evolução

Ler:

```text
history/
philosophy/
```

---

## Quero Fazer Uma Auditoria

Ler:

```text
ssot/
standards/
operations/
```

---

# Regra Fundamental

Se não souber onde procurar uma informação:

1. Consultar este documento.
2. Identificar a área correta.
3. Seguir as ligações para a documentação específica.

---

# Definição de Sucesso

O sistema documental será considerado maduro quando qualquer pessoa conseguir localizar qualquer informação relevante em menos de cinco minutos utilizando apenas este mapa de conhecimento.
