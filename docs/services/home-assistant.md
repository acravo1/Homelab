# Home Assistant

## Objetivo

Este documento descreve a implementação do Home Assistant no Cravo Homelab.

O objetivo é permitir:

- compreender a função do serviço;
- administrar a plataforma;
- recuperar após desastre;
- auditar integrações;
- documentar dependências.

Este documento destina-se ao administrador da infraestrutura.

---

# Resumo

## Nome

Home Assistant

## Tipo

Plataforma de automação residencial.

## Estado

Produção.

## Criticidade

Crítica.

---

# Função

O Home Assistant constitui o cérebro operacional da habitação.

Coordena:

- automações;
- sensores;
- notificações;
- equipamentos inteligentes;
- monitorização;
- lógica doméstica.

---

# Dependências

## PostgreSQL

Utilizado para:

- histórico;
- estatísticas;
- eventos;
- telemetria.

Sem PostgreSQL o serviço continua a funcionar mas perde capacidades avançadas de histórico.

---

## Rede Local

Dependência crítica.

A maioria dos dispositivos comunica através da rede.

---

## DNS

Dependência operacional.

Utilizado para resolução de serviços internos.

---

## Energia

Dependência crítica.

O serviço é considerado de missão crítica para a habitação.

---

# Dados Armazenados

## Configuração

Exemplos:

- configuration.yaml
- packages
- scripts
- scenes
- dashboards

---

## Automações

Inclui:

- automações da habitação;
- notificações;
- rotinas;
- lógica de controlo.

---

## Dashboards

Interfaces utilizadas diariamente pelos utilizadores.

---

## Base de Dados

Armazenada em PostgreSQL.

Contém:

- estados;
- histórico;
- estatísticas;
- eventos.

---

# Integrações Principais

## Domótica

- Zigbee
- Tuya
- Tomadas inteligentes
- Sensores

---

## Assistentes de Voz

- Amazon Alexa
- Dispositivos Echo

---

## Rede

- Omada
- sensores de presença
- monitorização

---

## Multimédia

- Fire TV
- dispositivos compatíveis

---

# Área de Rega Inteligente

## Criticidade

Elevada.

Trata-se de uma das automações mais sofisticadas da infraestrutura.

---

## Funções

- monitorização da humidade;
- controlo de válvulas;
- compensação dinâmica;
- notificações;
- proteção contra rega excessiva.

---

## Observação

Qualquer alteração nesta área deve ser previamente documentada.

---

# Notificações

## Função

Informar os utilizadores sobre:

- eventos;
- alertas;
- estados relevantes.

---

## Tipos

### Informativas

Sem necessidade de ação.

---

### Avisos

Merecem observação.

---

### Críticas

Requerem atenção imediata.

---

# Procedimentos Operacionais

## Atualização

Antes de atualizar:

1. Confirmar backups.
2. Confirmar estado do PostgreSQL.
3. Registar alteração no Change Log.

Após atualizar:

1. Validar dashboards.
2. Validar automações.
3. Validar notificações.

---

## Reinício

Confirmar após reinício:

- sensores;
- integrações;
- automações críticas.

---

# Recuperação

## Cenário 1

Perda de configuração.

Restaurar:

- configuração;
- scripts;
- automações.

---

## Cenário 2

Perda da base de dados.

Restaurar backup PostgreSQL.

---

## Cenário 3

Perda total do serviço.

Seguir:

```text
docs/operations/rebuild-from-zero.md
```

---

# Auditoria Anual

Confirmar:

- integrações não utilizadas;
- automações órfãs;
- dashboards abandonados;
- entidades duplicadas.

---

# Métricas Importantes

## Saúde

- CPU
- RAM
- Tempo de resposta

---

## Base de Dados

- tamanho;
- crescimento;
- desempenho.

---

## Integrações

- entidades indisponíveis;
- falhas recorrentes;
- dispositivos offline.

---

# Filosofia

O Home Assistant existe para simplificar a gestão da habitação.

Uma automação deve existir apenas quando:

- reduz trabalho;
- reduz erros;
- acrescenta conforto;
- acrescenta segurança.

Uma automação difícil de compreender deve ser considerada candidata a simplificação.

---

# Documentação Relacionada

```text
docs/ssot/services.md
docs/family/home-assistant.md
docs/operations/maintenance.md
docs/operations/rebuild-from-zero.md
```
