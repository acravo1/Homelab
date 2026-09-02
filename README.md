# Cravo Homelab

> Infraestrutura doméstica orientada para soberania digital, centralização da informação, automação inteligente e preservação do conhecimento.

---

# O Que é o Cravo Homelab?

O Cravo Homelab é uma plataforma tecnológica doméstica desenvolvida para servir as necessidades reais da família.

Não foi concebido como uma experiência tecnológica ou demonstração de competências técnicas.

Foi criado para:

- centralizar informação;
- reduzir duplicações;
- automatizar processos repetitivos;
- preservar conhecimento;
- aumentar a privacidade;
- diminuir dependências externas.

Ao longo do tempo evoluiu de um conjunto de serviços isolados para um sistema integrado de documentação, automação, armazenamento e colaboração.

---

# Missão

A tecnologia existe para servir a família.

Todas as decisões técnicas devem contribuir para:

- simplificar tarefas;
- proteger informação;
- preservar conhecimento;
- garantir continuidade;
- reduzir dependências desnecessárias.

---

# Antes de Começar

O primeiro documento que deve ser lido é:

```text
docs/philosophy/00-principios-fundamentais.md
```

Este documento constitui a base filosófica de todo o projeto.

---

# Estrutura da Documentação

## Filosofia

Porque existe o projeto.

```text
docs/philosophy/
```

Inclui:

- Princípios Fundamentais
- Regras de Ouro
- Glossário
- Visão Estratégica
- Carta do Administrador

---

## Fonte Única da Verdade (SSOT)

Estado atual da infraestrutura.

```text
docs/ssot/
```

Inclui:

- Hardware
- Rede
- Armazenamento
- Serviços
- Utilizadores
- Backups
- Inventário
- Criticidade

---

## Arquitetura

Como os sistemas se relacionam.

```text
docs/architecture/
```

Inclui:

- Princípios de Arquitetura
- Dependências de Serviços
- Fluxos de Informação

---

## Operação

Como administrar o sistema.

```text
docs/operations/
```

Inclui:

- Manutenção
- Recuperação
- Auditoria
- Pipeline Documental
- Integração de Serviços

---

## Serviços

Documentação individual de cada serviço.

```text
docs/services/
```

Inclui:

- Home Assistant
- PostgreSQL
- Nextcloud
- Paperless
- Authentik
- AdGuard
- WireGuard
- NPM

---

## Família

Documentação destinada aos utilizadores finais.

```text
docs/family/
```

Inclui:

- Guia da Família
- Nextcloud
- Paperless
- Talk
- Home Assistant
- FAQ

---

## Normas

Regras de governação.

```text
docs/standards/
```

Inclui:

- Convenções de Nomenclatura
- Classificação Documental

---

## História

Preserva a evolução do projeto.

```text
docs/history/
```

Inclui:

- Evolução Arquitetural
- Migração Palmela → Castelo Branco
- Lições Aprendidas
- Ativos Aposentados

---

# Leitura Recomendada

## Sou Utilizador da Família

Ler:

```text
docs/family/
```

---

## Sou Administrador

Ler:

```text
docs/philosophy/
docs/ssot/
docs/operations/
```

---

## Quero Recuperar a Infraestrutura

Ler:

```text
docs/ssot/
docs/operations/
docs/services/
```

---

## Quero Compreender a História

Ler:

```text
docs/history/
```

---

## Quero Fazer Auditoria

Ler:

```text
docs/standards/
docs/ssot/
docs/operations/document-audit-process.md
```

---

# Modelo de Conhecimento

O projeto segue uma hierarquia formal de confiança.

```text
VALIDADO
↓
PROVÁVEL
↓
HIPÓTESE

HISTÓRICO
```

Apenas informação validada deve ser utilizada para decisões críticas.

---

# Gestão Documental

A documentação original existe apenas no GitHub.

```text
GitHub
    ↓
Markdown
```

Todos os restantes formatos são derivados.

---

# Publicação Documental

Arquitetura prevista:

```text
Markdown
    ↓
GitHub
    ↓
GitHub Actions
    ↓
PDF
```

Destino:

```text
Nextcloud
    ↓
Biblioteca Viva
```

e

```text
Paperless
    ↓
Arquivo Histórico
```

---

# Fonte da Verdade

Em caso de conflito entre:

- memória;
- documentação antiga;
- mensagens;
- respostas de IA;

prevalece sempre:

1. configuração real;
2. evidência técnica;
3. SSOT.

---

# Objetivo Final

O sucesso do Cravo Homelab não será medido pelo número de serviços instalados.

Será medido pela capacidade de:

- servir a família;
- preservar conhecimento;
- proteger informação;
- simplificar operações;
- sobreviver ao tempo.

---

# Frase Fundadora

> Os sistemas mudam.
>
> Os equipamentos mudam.
>
> As aplicações mudam.
>
> A documentação envelhece.
>
> Os princípios permanecem.
