# Operação e Manutenção

## Objetivo

Este documento descreve as atividades regulares necessárias para manter o Cravo Homelab estável, atualizado e operacional.

O objetivo é reduzir a dependência da memória do administrador e garantir consistência operacional ao longo do tempo.

---

# Filosofia

A manutenção deve ser:

- previsível;
- documentada;
- repetível;
- auditável.

A infraestrutura deve ser cuidada de forma preventiva e não apenas quando surge uma falha.

---

# Frequências de Manutenção

## Diária

Verificações rápidas.

### Confirmar

- Serviços críticos operacionais.
- Alertas recebidos.
- Espaço livre suficiente.
- Estado geral do Home Assistant.

### Ferramentas

- Uptime Kuma
- Home Assistant
- Dashboards principais

---

## Semanal

Validação básica da infraestrutura.

### Confirmar

- Serviços Docker ativos.
- Utilização de disco.
- Estado do NAS.
- Atualizações pendentes.

### Rever

- Logs críticos.
- Alertas recorrentes.
- Comportamentos anómalos.

---

## Mensal

Auditoria operacional.

### Confirmar

- Estado dos backups.
- Utilização de armazenamento.
- Crescimento da base documental.
- Funcionamento da VPN.

### Validar

- Pesquisa no Paperless.
- Acesso ao Nextcloud.
- Login Authentik.
- Resolução DNS.

---

## Trimestral

Auditoria técnica.

### Rever

- Docker Compose.
- Utilizadores.
- Integrações.
- Serviços experimentais.

### Confirmar

- Serviços sem utilização.
- Serviços sem documentação.
- Dependências desnecessárias.

---

## Anual

Auditoria completa.

### Rever

- Hardware.
- Rede.
- Armazenamento.
- Serviços.
- Documentação.

### Atualizar

- SSOT.
- ADRs.
- Inventários.
- Histórico.

---

# Manutenção por Serviço

## Home Assistant

### Verificar

- Automações com erro.
- Sensores indisponíveis.
- Integrações degradadas.

### Confirmar

- Bases de dados.
- Dashboards.
- Notificações.

---

## Nextcloud

### Verificar

- Espaço disponível.
- Utilizadores.
- Aplicações instaladas.

### Confirmar

- Upload.
- Download.
- Partilhas.

---

## Paperless

### Verificar

- OCR.
- Correspondentes.
- Etiquetas.

### Confirmar

- Pesquisa.
- Indexação.

---

## PostgreSQL

### Verificar

- Crescimento das bases.
- Consumo de espaço.
- Integridade dos backups.

---

## WireGuard

### Confirmar

- Ligação remota.
- Perfis ativos.
- Resolução DNS.

---

## AdGuard Home

### Verificar

- Regras DNS.
- Estatísticas.
- Logs anómalos.

---

# Critérios de Saúde

## Verde

Funcionamento normal.

Nenhuma intervenção necessária.

---

## Amarelo

Anomalia ligeira.

Requer observação.

---

## Vermelho

Intervenção necessária.

Pode existir impacto na família ou nos serviços.

---

# Lista de Verificação Pós-Alteração

Sempre que ocorrer uma alteração relevante:

## Validar

- Nextcloud
- Paperless
- Home Assistant
- Authentik
- DNS
- VPN

---

## Atualizar

```text
docs/ssot/change-log.md
```

---

## Atualizar

Documentação relacionada.

---

# Indicadores Importantes

## Infraestrutura

- Espaço livre.
- Utilização RAM.
- Utilização CPU.
- Temperaturas.

---

## Dados

- Crescimento documental.
- Crescimento de fotografias.
- Crescimento das bases de dados.

---

## Serviços

- Disponibilidade.
- Tempo de resposta.
- Alertas.

---

# O Que Não Fazer

❌ Atualizar vários componentes críticos ao mesmo tempo.

❌ Apagar serviços sem documentação.

❌ Alterar configurações sem registo.

❌ Assumir que um backup funciona sem o testar.

❌ Assumir que nos vamos lembrar mais tarde.

---

# Regra Fundamental

Sempre que uma alteração parecer pequena mas afetar:

- dados;
- segurança;
- armazenamento;
- autenticação;
- rede;

essa alteração deve ser documentada.

---

# Definição de Sucesso

Uma infraestrutura bem mantida é aquela que:

- raramente falha;
- recupera rapidamente;
- possui documentação atualizada;
- não depende da memória do administrador.

A melhor manutenção é aquela que evita incidentes antes de eles acontecerem.
