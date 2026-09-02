# Rede (SSOT)

## Objetivo

Este documento descreve a arquitetura de rede atualmente utilizada pelo Cravo Homelab.

O objetivo da rede não é apenas fornecer acesso à Internet.

A rede constitui a plataforma de segurança, comunicação, automação e acesso aos serviços da família.

---

# Filosofia da Rede

A arquitetura de rede segue cinco princípios fundamentais:

1. Local First.
2. Segmentação de confiança.
3. Privilégio mínimo.
4. DNS interno centralizado.
5. Acesso remoto exclusivamente através de VPN.

Sempre que estas regras entrem em conflito com conveniências temporárias, devem prevalecer os princípios.

---

# Visão Geral

```text
Internet
    │
    ▼

Operador ISP
    │
    ▼

TP-Link ER605
    │
    ├── VLAN Principal
    ├── VLAN IoT
    └── VLAN Guest

    │
    ▼

TL-SG1008P
    │
    ▼

EAP653
    │
    ▼

Clientes e Serviços
```

---

# Equipamentos de Rede

## Router Principal

Estado: PROVÁVEL

Equipamento:

TP-Link Omada ER605

Funções:

- Gateway principal
- Firewall
- DHCP
- VLANs
- Encaminhamento
- VPN

---

## Switch Principal

Estado: PROVÁVEL

Equipamento:

TP-Link TL-SG1008P

Funções:

- Distribuição Ethernet
- PoE
- Interligação dos sistemas

---

## Access Point Principal

Estado: PROVÁVEL

Equipamento:

TP-Link EAP653

Funções:

- Rede Wi-Fi
- Segmentação de SSIDs
- Acesso móvel

---

# Endereçamento Principal

## Rede Principal

Estado: PROVÁVEL

```text
192.168.168.0/23
```

Função:

Rede principal do Homelab.

Contém:

- Lenovo Host
- QNAP
- Serviços centrais
- Computadores
- Dispositivos familiares

---

## Lenovo Host

Estado: PROVÁVEL

```text
192.168.168.168
```

Função:

Nó principal da infraestrutura.

---

## NAS QNAP

Estado: PROVÁVEL

```text
192.168.168.200
```

Função:

Armazenamento central.

---

# Segmentação

## VLAN Principal

Função:

Serviços críticos e equipamentos de confiança.

Exemplos:

- Lenovo
- QNAP
- Computadores
- Administração

---

## VLAN IoT

Função:

Isolamento dos equipamentos de automação.

Exemplos:

- Sensores
- Tomadas Inteligentes
- Relés
- Equipamentos Tuya
- Infraestrutura de automação

Princípio:

A IoT não deve iniciar comunicações para a rede principal.

---

## VLAN Guest

Função:

Visitantes.

Princípio:

Os visitantes devem ter acesso apenas à Internet.

Sem acesso à rede interna.

---

# DNS

## Princípio

Todos os dispositivos devem utilizar DNS interno.

A resolução de nomes internos é considerada uma funcionalidade crítica.

---

## Serviço Principal

AdGuard Home

Funções:

- DNS da rede local
- Reescrita de nomes
- Filtragem
- Gestão de domínios internos

---

## Zona Local

```text
*.lenovo
```

*til*zação:

- nextcloud.lenovo
- paper*ess.lenovo
- homeassistant.lenovo
* outros serviços internos

---

# *i-Fi

## Objetivo

Separar*dispositivos de confiança dos disp*sitivos IoT.

---

## Rede Princip*l

SSID:

```text
CRAVO_HOMELAB
``*

Destinada a:

- computadores
- t*lemóveis
- tablets
- administração*
---

## Rede Io*

SSID:

```text
CRAVO_IOT
```

De*tinada a:

- sensores
- tomadas
- *ontroladores
- equipamentos de aut*mação

---

# Segurança

## Regra *undamental

Nenhum serviço interno*deve estar diretamente exposto à I*ternet.

---

## UPnP

Estado espe*ado:

DESATIVADO

Motivo:

Impedir*a abertura automática de portas.

*--

## Port Forwarding

Estado esp*rado:

Mínimo possível.

A*enas as*regras estr*tamente necessárias devem existir.*
---

## Firewall

Princípio:

Neg*r por defeito.

Permitir apenas o *ecessário.

---

# Acesso Remoto

*# Método Oficial

WireGuard

Não e*istem métodos alternativos oficial*ente suportados.

---

## Objetivo*

Permitir:

- acesso à documentaç*o
- acesso ao Nextcloud
- acesso a* Paperless
- acesso ao Home Assist*nt

sem exposição direta dos servi*os à Internet.

---

# Dependência* Críticas

A rede suporta diretame*te:

- AdGuard Home
- Nextcloud
- *aperless
- Home Assistant
- WireGu*rd
- Authentik
- PostgreSQL
- Ngin* Proxy Manager

Qualquer alteração*estrutural da rede deve considerar*o impacto nestes serviços.

---

#*Auditorias Futuras

Validar atravé* de exportação Omada:

- VLANs rea*s
- ACLs
- Reservas DHCP
- DNS*- Port Forwards
- Re*ras de Firewall
- SSIDs
- Pot*ncias Wi-Fi
* Configurações de roaming

---

* Regra de Atualização

Sempre que*ocorrer alteração*

- de endereçamento;
- de VLANs;
* de Wi-Fi;
- de*ACLs;
- de DNS;
- de VPN;

este do*umento deve ser atualizado antes d* alteração ser considerada concluí*a.
