# Registo de Riscos

## Objetivo

Este documento identifica os principais riscos conhecidos do Cravo Homelab.

O objetivo não é eliminar todos os riscos.

Isso é impossível.

O objetivo é:

- reconhecer os riscos;
- compreender os impactos;
- definir medidas de mitigação;
- evitar surpresas previsíveis.

---

# Filosofia

Os riscos ignorados não desaparecem.

Continuam a existir.

A única diferença é que deixam de ser geridos.

---

# Classificação

## Probabilidade

### Baixa

Pouco provável.

---

### Média

Pode ocorrer.

---

### Alta

Espera-se que ocorra algures no futuro.

---

# Impacto

### Baixo

Impacto reduzido.

---

### Médio

Impacto significativo.

---

### Alto

Impacto grave.

---

### Crítico

Impacto potencialmente catastrófico.

---

# Risco 001

## Nome

Falha do servidor principal.

### Probabilidade

Média

### Impacto

Crítico

### Ativos Afetados

- Home Assistant
- Nextcloud
- Paperless
- PostgreSQL
- Authentik

### Mitigação

- Backups
- Documentação
- Procedimentos de reconstrução

### Estado

Monitorizado

---

# Risco 002

## Nome

Falha do armazenamento principal.

### Probabilidade

Média

### Impacto

Crítico

### Ativos Afetados

- Documentos
- Fotografias
- Arquivo

### Mitigação

- NAS
- Estratégia de backup
- Auditorias

### Estado

Monitorizado

---

# Risco 003

## Nome

Documentação desatualizada.

### Probabilidade

Alta

### Impacto

Alto

### Causa

Alterações não documentadas.

### Mitigação

- SSOT
- Change Log
- Auditorias

### Estado

Ativo

---

# Risco 004

## Nome

Dependência excessiva do administrador.

### Probabilidade

Alta

### Impacto

Alto

### Causa

Conhecimento não documentado.

### Mitigação

- Manual da Família
- SSOT
- Procedimentos operacionais

### Estado

Em redução

---

# Risco 005

## Nome

Perda de conhecimento histórico.

### Probabilidade

Alta

### Impacto

Médio

### Mitigação

- GitHub
- ADRs
- História
- Lições Aprendidas

---

# Risco 006

## Nome

Complexidade excessiva.

### Probabilidade

Alta

### Impacto

Alto

### Indicadores

- serviços redundantes;
- automações inúteis;
- dependências excessivas.

### Mitigação

- Auditorias
- Gestão de ciclo de vida

---

# Risco 007

## Nome

Falha da rede.

### Probabilidade

Média

### Impacto

Alto

### Componentes

- Router
- Switch
- Access Point

### Mitigação

- Documentação Omada
- Inventário
- Exportações

---

# Risco 008

## Nome

Dependência excessiva de IA.

### Probabilidade

Média

### Impacto

Médio

### Descrição

Informação produzida por IA pode parecer plausível sem ser verdadeira.

### Mitigação

- Evidências primárias
- Sistema VALIDADO/PROVÁVEL/HIPÓTESE

---

# Risco 009

## Nome

Divergência entre realidade e SSOT.

### Probabilidade

Alta

### Impacto

Alto

### Mitigação

- Auditorias periódicas
- Processo documental

---

# Risco 010

## Nome

Falha dos backups.

### Probabilidade

Desconhecida

### Impacto

Crítico

### Mitigação

- Testes periódicos
- Exercícios de recuperação

---

# Matriz de Prioridade

## Crítica

- Falha do servidor
- Falha do armazenamento
- Falha dos backups

---

## Elevada

- Dependência do administrador
- Documentação desatualizada
- Divergência da SSOT

---

## Média

- Complexidade excessiva
- Falha de rede
- Perda de conhecimento

---

# Revisão

Este documento deve ser revisto:

- após incidentes;
- após migrações;
- durante auditorias anuais;
- após alterações arquiteturais importantes.

---

# Regra Fundamental

O objetivo não é reduzir a lista de riscos.

O objetivo é aumentar a lista de riscos conhecidos.

Os riscos conhecidos podem ser geridos.

Os riscos desconhecidos são os verdadeiramente perigosos.

---

# Definição de Sucesso

Uma infraestrutura madura não é aquela que não possui riscos.

É aquela que conhece os seus riscos e possui planos razoáveis para os enfrentar.
