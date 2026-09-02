# Armazenamento (SSOT)

## Objetivo

Este documento descreve a arquitetura oficial de armazenamento do Cravo Homelab.

O seu objetivo é identificar:

- onde os dados residem;
- como são armazenados;
- quem depende deles;
- que mecanismos de proteção existem;
- como recuperar os dados em caso de desastre.

---

# Filosofia de Armazenamento

O sistema foi concebido para cumprir quatro objetivos:

1. Centralização da informação.
2. Eliminação de duplicações desnecessárias.
3. Facilidade de pesquisa e recuperação.
4. Continuidade operacional.

Nenhum dado importante deve existir exclusivamente em dispositivos pessoais.

A informação familiar deve residir em sistemas centralizados e documentados.

---

# Visão Geral

```text
Utilizadores
      │
      ▼

Nextcloud
Paperless
Home Assistant

      │
      ▼

Lenovo Host

      │
   iSCSI
      │

      ▼

NAS QNAP
```

---

# Camadas de Armazenamento

## Camada 1 - SSD Local

### Estado

VALIDADO

### Localização

Servidor Lenovo ThinkCentre M710 SFF

### Tipo

SSD 256 GB

### Função

Armazenamento rápido para:

- Sistema Operativo
- Docker
- Configuração dos serviços
- Bases de dados ativas
- Ficheiros temporários

### Princípio

Apenas dados que beneficiem de elevado desempenho devem permanecer no SSD local.

---

## Camada 2 - NAS Principal

### Estado

VALIDADO

### Equipamento

NAS QNAP

### Ligação

iSCSI

### Função

Armazenamento permanente.

Concentra:

- documentos familiares;
- fotografias;
- arquivo digital;
- multimédia;
- cópias de segurança;
- dados persistentes.

### Princípio

O NAS é considerado o repositório principal de dados da família.

---

# Distribuição de Dados

## Nextcloud

### Finalidade

Documentos vivos.

Informação em utilização diária.

### Exemplos

- documentos pessoais;
- documentos partilhados;
- fotografias;
- ficheiros de trabalho;
- documentação corrente.

---

## Paperless

### Finalidade

Arquivo documental permanente.

### Exemplos

- faturas;
- garantias;
- contratos;
- seguros;
- documentos fiscais;
- documentação digitalizada.

### Regra

Um documento arquivado definitivamente deve residir no Paperless.

---

## GitHub

### Finalidade

Conhecimento.

### Conteúdo

- documentação;
- inventários;
- procedimentos;
- histórico;
- Fonte da Verdade.

### Regra

O GitHub guarda conhecimento.

Não guarda dados familiares.

---

# Evolução Histórica

## Solução Inicial

Disco USB externo.

### Problemas identificados

- dependência física;
- fiabilidade limitada;
- expansão reduzida.

---

## Solução Atual

NAS QNAP.

Ligação iSCSI ao servidor principal.

### Benefícios

- centralização;
- melhor capacidade;
- maior escalabilidade;
- melhor integração com serviços.

---

# Criticidade dos Dados

## Nível 1 - Crítico

Perda inaceitável.

Exemplos:

- Paperless;
- documentos legais;
- documentação técnica;
- fotografias familiares.

---

## Nível 2 - Importante

Recuperável com esforço.

Exemplos:

- configurações;
- automações;
- dashboards.

---

## Nível 3 - Recriável

Pode ser reconstruído.

Exemplos:

- contentores Docker;
- imagens Docker;
- caches temporárias.

---

# Princípios Operacionais

## Regra 1

Nenhum documento importante deve existir apenas num telemóvel.

---

## Regra 2

Nenhuma fatura deve existir apenas em papel.

---

## Regra 3

O Paperless é o arquivo oficial da família.

---

## Regra 4

O Nextcloud é a área de trabalho da família.

---

## Regra 5

O GitHub é a memória técnica permanente.

---

# Futuras Auditorias

Validar:

- estrutura real de volumes do QNAP;
- mapeamentos iSCSI;
- diretórios utilizados por cada serviço;
- política de backups;
- estratégia de recuperação após desastre.
