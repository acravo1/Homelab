# Contribuição para a Documentação

## Objetivo

Este documento define as regras para criação, alteração e manutenção da documentação do Cravo Homelab.

A documentação constitui uma parte integrante da infraestrutura.

Por esse motivo, alterações documentais devem seguir princípios consistentes.

---

# Filosofia

A documentação existe para reduzir dependências da memória humana.

Cada documento deve contribuir para:

- compreensão;
- recuperação;
- operação;
- continuidade.

O objetivo não é escrever mais documentação.

O objetivo é escrever documentação útil.

---

# Antes de Criar um Documento

Perguntar:

## Esta informação já existe?

Se existir:

Atualizar o documento existente.

Não criar duplicações.

---

## Este documento terá utilização futura?

Se a resposta for:

```text
Talvez não
```

considerar se realmente deve existir.

---

## Qual é o público-alvo?

Escolher uma das categorias:

### Família

```text
docs/family/
```

---

### Estado Atual

```text
docs/ssot/
```

---

### Operação

```text
docs/operations/
```

---

### Arquitetura

```text
docs/architecture/
```

---

### Filosofia

```text
docs/philosophy/
```

---

### Histórico

```text
docs/history/
```

---

# Estrutura Recomendada

Todos os documentos devem conter:

## Objetivo

Porque existe o documento.

---

## Conteúdo

Informação principal.

---

## Relações

Quando relevante.

Exemplo:

```text
Documentação Relacionada
```

---

## Regras

Quando aplicável.

---

# Estilo de Escrita

## Deve ser

- claro;
- simples;
- objetivo;
- intemporal.

---

## Deve evitar

- jargão excessivo;
- humor contextual;
- linguagem emocional;
- dependência de conhecimento implícito.

---

# Regra do Futuro

Assumir sempre que o leitor:

- não estava presente;
- não conhece o contexto;
- não conhece o histórico;
- não conhece os serviços.

Documentar como se o leitor chegasse ao projeto pela primeira vez.

---

# Atualizações

Uma alteração técnica importante deve produzir:

## 1

Alteração da infraestrutura.

---

## 2

Atualização da SSOT.

---

## 3

Atualização do Change Log.

---

## 4

Atualização da documentação relacionada.

---

# Quando Criar um ADR

Criar ADR quando:

- houver uma decisão arquitetural;
- existir escolha entre alternativas;
- a decisão tiver impacto futuro.

Não criar ADR para:

- alterações triviais;
- correções menores;
- manutenção rotineira.

---

# Quando Criar Uma Lição Aprendida

Criar entrada em:

```text
docs/history/lessons-learned.md
```

quando ocorrer:

- incidente importante;
- erro significativo;
- descoberta relevante.

---

# Gestão de PDFs

## Regra Fundamental

Nunca editar PDFs.

Os PDFs são artefactos gerados.

---

## Fluxo Oficial

```text
Markdown
    ↓
GitHub
    ↓
PDF
    ↓
Nextcloud
    ↓
Paperless
```

---

## Fonte Única

A única fonte autorizada para alterações é:

```text
GitHub
```

---

# Critério de Qualidade

Um documento de qualidade deve responder claramente:

- O quê?
- Porquê?
- Como?
- Quando?
- Onde?

Sem necessidade de consultar o autor.

---

# Regra dos Cinco Anos

Antes de terminar um documento perguntar:

> Conseguirei compreender isto daqui a cinco anos?

Se a resposta for negativa:

O documento precisa de mais contexto.

---

# Definição de Sucesso

A documentação será considerada madura quando uma pessoa sem contacto prévio com o projeto conseguir:

- compreender a infraestrutura;
- operar os serviços;
- recuperar sistemas;
- continuar a evolução do Homelab;

utilizando apenas os documentos presentes no repositório.

Nesse momento o conhecimento deixará de depender do seu criador e passará a pertencer ao próprio sistema.
