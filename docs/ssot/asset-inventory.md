# Inventário de Ativos

## Objetivo

Este documento constitui o inventário oficial dos ativos físicos e lógicos do Cravo Homelab.

O seu objetivo é permitir identificar rapidamente:

- o que existe;
- onde se encontra;
- para que serve;
- quem depende do equipamento;
- qual a sua criticidade.

Este documento complementa a SSOT e deve ser mantido atualizado.

---

# Classificação dos Ativos

Os ativos são agrupados por categoria.

---

# Infraestrutura Principal

## Lenovo ThinkCentre M710 SFF

### Estado

Ativo

### Função

Servidor principal do Homelab.

### Criticidade

Crítica

### Localização Física

A definir pela instalação atual.

### Dependências

- Docker
- Home Assistant
- Nextcloud
- Paperless
- Authentik
- PostgreSQL

---

## NAS QNAP

### Estado

Ativo

### Função

Armazenamento principal.

### Criticidade

Crítica

### Ligação

iSCSI

### Dependências

- Nextcloud
- Paperless
- Backups

---

# Equipamentos de Rede

## TP-Link ER605

### Estado

Ativo

### Função

Gateway principal.

### Criticidade

Crítica

---

## TP-Link TL-SG1008P

### Estado

Ativo

### Função

Switch principal.

### Criticidade

Elevada

---

## TP-Link EAP653

### Estado

Ativo

### Função

Access Point principal.

### Criticidade

Elevada

---

# Assistentes de Voz

## Amazon Echo

### Estado

Ativo

### Função

Interação por voz.

### Criticidade

Baixa

### Observações

Inventário detalhado pendente.

---

# Multimédia

## Fire TV

### Estado

Ativo

### Função

Integração multimédia.

### Criticidade

Baixa

---

# Segurança

## Sistema de Alarme

### Equipamento

PGST PG103

### Estado

Ativo

### Criticidade

Elevada

---

# Robôs

## Roomba #1

### Estado

Ativo

### Função

Limpeza.

---

## Roomba #2

### Estado

Ativo

### Função

Limpeza.

---

# Ecossistema Zigbee

## Objetivo

Todos os dispositivos Zigbee devem ser catalogados individualmente.

---

# Modelo de Registo

## Nome

Tomada Zigbee Sala

## Entidade

switch.tomada_sala

## Localização

Sala

## Função

Controlo da iluminação indireta.

## Data de Instalação

AAAA-MM-DD

## Criticidade

Baixa

## Dependências

Home Assistant

---

# Sensores

Cada sensor deve incluir:

- localização;
- entidade;
- tecnologia;
- utilização;
- data de instalação.

---

# Iluminação

Cada dispositivo deve incluir:

- localização;
- entidade;
- tipo;
- automações associadas.

---

# Dispositivos Experimentais

Os equipamentos em teste devem ser registados separadamente.

Estado:

```text
LAB
```

---

# Equipamentos Aposentados

Equipamentos retirados de serviço devem migrar para:

```text
docs/history/retired-assets.md
```

---

# Criticidade

## Crítica

Falha com impacto imediato.

Exemplos:

- Lenovo
- QNAP
- ER605

---

## Elevada

Falha com impacto significativo.

Exemplos:

- Home Assistant
- EAP653
- Alarme

---

## Média

Falha com impacto limitado.

---

## Baixa

Falha sem impacto estrutural.

---

# Regra Fundamental

Nenhum equipamento deve existir na infraestrutura sem estar inventariado.

Se um dispositivo não consta neste documento, deve ser considerado não documentado.

---

# Definição de Sucesso

Qualquer pessoa deve conseguir:

- localizar um equipamento;
- identificar a sua função;
- avaliar a sua criticidade;
- compreender as suas dependências;

consultando apenas este inventário.
