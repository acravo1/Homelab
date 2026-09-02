# Hardware Atual (SSOT)

## Objetivo

Este documento descreve exclusivamente o hardware atualmente considerado em produção no Cravo Homelab.

Não inclui:

- hardware histórico;
- planos futuros;
- equipamentos retirados de serviço;
- hipóteses ou configurações ainda não verificadas.

Toda a informação presente neste documento deve possuir uma fonte de validação identificada.

---

# Estado do Documento

Classificação:

VALIDADO + PROVÁVEL

Última revisão:

2026-09-XX

---

# Servidor Principal

## Estado

VALIDADO

## Equipamento

Lenovo ThinkCentre M710 SFF

## Processador

Intel Core i5-6500T

## Memória RAM

8 GB DDR4

## Armazenamento Local

256 GB SSD

## Sistema Operativo

Ubuntu Server LTS

## Função

Servidor principal do Homelab.

Executa:

- Docker
- Home Assistant
- Nextcloud
- Paperless-ngx
- Authentik
- PostgreSQL
- AdGuard Home
- WireGuard
- Nginx Proxy Manager
- Uptime Kuma

## Evidência

Fatura de aquisição datada de 25/06/2026.

---

# Armazenamento Secundário

## Estado

VALIDADO

## Equipamento

NAS QNAP

## Função

Armazenamento massivo.

Aloja:

- documentos familiares;
- arquivo Paperless;
- armazenamento Nextcloud;
- backups;
- conteúdos multimédia.

## Ligação

iSCSI

## Observações

Substituiu uma solução anterior baseada em disco USB externo.

---

# Equipamentos de Rede

## Estado

PROVÁVEL

Necessita de futura validação através de exportação Omada.

### Router Principal

TP-Link Omada ER605

### Switch Principal

TP-Link TL-SG1008P

### Access Point Principal

TP-Link EAP653

---

# Equipamentos de Automação

## Estado

PROVÁVEL

### Robôs Aspiradores

2 x iRobot Roomba i1

### Sistema de Alarme

PGST PG103

### Ecossistema Zigbee

Sensores e atuadores diversos.

Validação detalhada pendente de inventário.

---

# Equipamentos de Voz e Multimédia

## Estado

PROVÁVEL

### Amazon Echo

- Echo Show 15
- Echo Spot
- Echo Pop

### Fire TV

Dispositivos Fire TV utilizados para integração multimédia.

Número exato de equipamentos por validar.

---

# Hardware Histórico

## Servidor

Nenhum registo histórico deve ser utilizado para descrever o estado atual.

Equipamentos identificados em documentação histórica:

- Lenovo M710s
- Lenovo M710 Tiny

Estes registos permanecem preservados em:

```text
docs/history/
```

e não devem ser considerados representativos da infraestrutura atual sem nova validação.

---

# Itens Pendentes de Auditoria

## Confirmar

- Número total de dispositivos Fire TV.
- Inventário Zigbee completo.
- Número total de tomadas inteligentes.
- Inventário completo de sensores.
- Inventário completo de dispositivos multimédia.

---

# Regra de Atualização

Qualquer alteração física de hardware deve originar:

1. Atualização deste documento.
2. Atualização do Change Log.
3. Arquivo da informação substituída no diretório histórico.

A documentação deve refletir a realidade física existente e não intenções futuras.
