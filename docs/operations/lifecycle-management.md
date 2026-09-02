# Gestão de Ciclo de Vida

## Objetivo

Este documento define como os componentes do Cravo Homelab evoluem ao longo do tempo.

Aplica-se a:

- serviços;
- hardware;
- documentação;
- automações;
- integrações;
- projetos.

O objetivo é evitar que elementos abandonados permaneçam indefinidamente na infraestrutura sem propósito definido.

---

# Filosofia

Tudo tem um ciclo de vida.

Nada deve permanecer indefinidamente apenas porque existe.

Cada componente deve estar numa das seguintes fases:

```text
Ideia
  ↓

LAB
  ↓

TESTE
  ↓

PRODUÇÃO
  ↓

OBSOLETO
  ↓

ARQUIVADO
```

---

# Fase 1 — Ideia

## Descrição

Conceito ainda não implementado.

Pode existir apenas como:

- nota;
- ADR;
- proposta;
- roadmap.

---

## Exemplos

- novos serviços;
- novas automações;
- novos equipamentos.

---

# Fase 2 — LAB

## Descrição

Implementação inicial.

Objetivo:

Aprender.

---

## Características

- experimental;
- sem garantias;
- sem dependência familiar.

---

## Pode Ser Removido?

Sim.

Sem impacto operacional.

---

# Fase 3 — TESTE

## Descrição

Sistema funcional.

Está a ser utilizado para validação.

---

## Requisitos

- documentação inicial;
- objetivo definido;
- utilizadores identificados.

---

## Pergunta-Chave

Resolve realmente um problema?

---

# Fase 4 — PRODUÇÃO

## Descrição

Sistema oficialmente adotado.

---

## Requisitos

- documentação;
- backup;
- recuperação;
- utilizadores reais;
- valor comprovado.

---

## Exemplos

- Home Assistant
- Nextcloud
- Paperless

---

# Fase 5 — OBSOLETO

## Descrição

Sistema substituído ou sem utilidade atual.

---

## Características

- não recebe novas funcionalidades;
- não deve acumular dependências;
- mantém apenas valor histórico.

---

## Regras

Documentar a razão da obsolescência.

---

# Fase 6 — ARQUIVADO

## Descrição

Elemento removido da operação diária.

Preservado apenas para consulta histórica.

---

## Localização

```text
docs/history/
```

---

# Ciclo de Vida da Documentação

## Documento Ativo

Utilizado regularmente.

---

## Documento Histórico

Representa um estado anterior.

---

## Documento Obsoleto

Já não é relevante para operação.

---

## Documento Arquivado

Mantido para consulta futura.

---

# Ciclo de Vida de Hardware

## Ativo

Em utilização.

---

## Reserva

Mantido para recuperação.

---

## Aposentado

Sem utilização operacional.

---

## Eliminado

Removido definitivamente.

---

# Ciclo de Vida de Automações

## Experimental

Teste funcional.

---

## Operacional

Produção.

---

## Desativada

Mantida para referência.

---

## Removida

Arquivada.

---

# Critérios para Remover Algo

Um componente é candidato a remoção quando:

- não possui utilizadores;
- não possui benefício claro;
- não possui documentação;
- foi substituído;
- aumenta complexidade sem valor.

---

# Regra Fundamental

Nada permanece em Produção por inércia.

A permanência em Produção deve ser continuamente justificada.

---

# Auditoria Anual

Durante a auditoria anual verificar:

### Serviços

- ainda são necessários?

### Hardware

- ainda é utilizado?

### Automações

- ainda acrescentam valor?

### Documentação

- ainda está atualizada?

### Projetos

- continuam ativos?

---

# Definição de Sucesso

A infraestrutura ideal não é a que possui mais componentes.

É a que possui apenas os componentes necessários.

Tudo o que existe deve ter:

- propósito;
- proprietário;
- documentação;
- valor.

Caso contrário deverá iniciar o seu processo de desativação.
