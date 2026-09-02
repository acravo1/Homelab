# Registo de Decisões Arquiteturais

## Objetivo

Este documento existe para registar decisões importantes tomadas ao longo da vida do Cravo Homelab.

Uma configuração sem contexto transforma-se rapidamente em arqueologia.

Uma decisão documentada continua compreensível mesmo muitos anos depois.

Este documento responde às perguntas:

- Porque foi tomada esta decisão?
- Que alternativas foram consideradas?
- Que problema estava a ser resolvido?
- Quais foram as consequências?

---

# Filosofia

As configurações são temporárias.

As decisões são permanentes.

Mesmo que uma implementação seja substituída no futuro, a razão que conduziu à sua criação continua a ter valor histórico e educativo.

---

# Formato das Decisões

Cada decisão deve seguir o seguinte modelo.

---

## ADR-XXX

### Data

AAAA-MM-DD

### Estado

- Proposta
- Aprovada
- Substituída
- Obsoleta

### Contexto

Que problema existia?

### Decisão

O que foi decidido?

### Alternativas Consideradas

Que opções foram avaliadas?

### Consequências

Quais os benefícios?

Quais os riscos?

---

# ADR-001

## Título

Adotar filosofia Local-First

### Estado

Aprovada

### Contexto

A dependência excessiva de serviços externos aumenta riscos de indisponibilidade, alterações comerciais e perda de controlo sobre os dados.

### Decisão

Priorizar serviços executados localmente.

### Alternativas Consideradas

- Dependência exclusiva de serviços cloud.
- Modelo híbrido cloud/local.

### Consequências

Benefícios:

- autonomia;
- privacidade;
- continuidade.

Custos:

- manutenção própria;
- necessidade de documentação.

---

# ADR-002

## Título

Utilizar GitHub como memória permanente

### Estado

Aprovada

### Contexto

Foram identificadas divergências entre documentação histórica, memória humana e reconstruções realizadas através de IA.

### Decisão

Centralizar o conhecimento institucional no repositório Git.

### Alternativas Consideradas

- Documentação dispersa.
- Google Docs.
- Dependência de memória.

### Consequências

Benefícios:

- histórico;
- auditoria;
- recuperação.

Custos:

- disciplina documental.

---

# ADR-003

## Título

Separar dados vivos de arquivo documental

### Estado

Aprovada

### Contexto

Misturar documentos ativos com arquivo permanente dificulta a pesquisa e organização.

### Decisão

Utilizar:

- Nextcloud para trabalho corrente.
- Paperless para arquivo permanente.

### Consequências

Redução da duplicação documental.

Melhoria da pesquisa.

---

# ADR-004

## Título

Acesso remoto exclusivamente por VPN

### Estado

Aprovada

### Contexto

Exposição direta de serviços aumenta a superfície de ataque.

### Decisão

Utilizar WireGuard como mecanismo oficial de acesso remoto.

### Alternativas Consideradas

- Exposição pública de serviços.
- Reverse Proxy exposto à Internet.
- Cloud VPN externa.

### Consequências

Maior segurança.

Maior dependência da VPN.

---

# ADR-005

## Título

Classificação formal da documentação

### Estado

Aprovada

### Contexto

A auditoria de 2026 revelou coexistência de:

- documentação atual;
- documentação histórica;
- hipóteses;
- reconstruções por IA.

### Decisão

Criar as classes:

- VALIDADO
- PROVÁVEL
- HISTÓRICO
- HIPÓTESE

### Consequências

Maior confiança na documentação.

Melhor auditoria futura.

---

# Regra Fundamental

Nenhuma decisão arquitetural importante deve existir apenas em:

- conversas;
- mensagens;
- memória do administrador;
- respostas de IA.

Quando uma decisão tiver impacto estrutural, deve receber um ADR.

---

# Definição de Sucesso

Daqui a dez anos, uma pessoa deve conseguir perceber não apenas:

- o que existe;

mas também:

- porque existe.
``
