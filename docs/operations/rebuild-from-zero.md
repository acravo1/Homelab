# Reconstrução Completa da Infraestrutura

## Objetivo

Este documento descreve o processo de reconstrução integral do Cravo Homelab a partir de hardware vazio.

O objetivo é permitir recriar a infraestrutura sem depender da memória do administrador original.

Este documento assume um cenário extremo:

- novo servidor;
- novo armazenamento;
- instalação limpa;
- recuperação através da documentação e backups.

---

# Filosofia

A reconstrução deve seguir os princípios fundamentais do sistema:

1. Infraestrutura primeiro.
2. Armazenamento depois.
3. Identidade antes das aplicações.
4. Dados antes dos serviços.
5. Recuperação antes da otimização.

Nunca acelerar etapas.

---

# Fase 1 — Hardware

## Confirmar

- servidor funcional;
- alimentação elétrica;
- ligação de rede;
- armazenamento disponível.

## Validar

- BIOS;
- relógio do sistema;
- ordem de arranque;
- interface de rede.

---

# Fase 2 — Sistema Operativo

## Instalar

Ubuntu Server LTS

## Configurar

- utilizador administrativo;
- SSH;
- atualizações;
- timezone;
- hostname.

## Validar

```bash
hostnamectl
ip addr
timedatectl
```

---

# Fase 3 — Rede

## Configurar

- IP fixo;
- gateway;
- DNS;
- VLANs se aplicável.

## Validar

```bash
ping gateway
ping internet
ping dns
```

---

# Fase 4 — Armazenamento

## Ligar

NAS QNAP

## Validar

- conectividade;
- volumes;
- partilhas;
- iSCSI.

## Confirmar

Montagens persistentes.

---

# Fase 5 — Docker

## Instalar

Docker Engine

Docker Compose

## Validar

```bash
docker --version
docker compose version
```

---

# Fase 6 — Infraestrutura Base

## Restaurar

PostgreSQL

## Restaurar

AdGuard Home

## Restaurar

Authentik

---

# Justificação

Sem identidade e DNS os restantes serviços não conseguem funcionar corretamente.

---

# Fase 7 — Serviços Principais

## Restaurar

Nextcloud

## Restaurar

Paperless

## Restaurar

Home Assistant

---

# Objetivo

Garantir recuperação dos dados familiares.

---

# Fase 8 — Serviços Complementares

## Restaurar

WireGuard

## Restaurar

Nginx Proxy Manager

## Restaurar

Uptime Kuma

## Restaurar

OnlyOffice

## Restaurar

Talk

---

# Fase 9 — Validação Funcional

Confirmar:

## Utilizadores

- Login funcional

## Nextcloud

- Leitura
- Escrita

## Paperless

- Pesquisa
- Visualização

## Home Assistant

- Sensores
- Automações

## VPN

- Ligação remota

## DNS

- Resolução local

---

# Fase 10 — Auditoria Final

Conferir:

- documentação;
- backups;
- serviços;
- automações;
- acessos.

Atualizar SSOT sempre que necessário.

---

# Critério de Sucesso

A reconstrução é considerada concluída quando:

- todos os serviços críticos funcionam;
- todos os dados críticos estão acessíveis;
- todos os acessos estão operacionais;
- a documentação corresponde à realidade.

---

# Nota Histórica

Se durante a reconstrução forem encontradas diferenças entre:

- memória;
- documentação antiga;
- respostas de IA;
- estado real;

deve prevalecer a documentação SSOT e a evidência técnica observada.

Os factos prevalecem sobre as interpretações.
