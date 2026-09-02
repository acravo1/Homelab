# Pipeline de Documentação

## Objetivo

Este documento descreve o ciclo de vida da documentação do Cravo Homelab.

O objetivo é garantir que o conhecimento:

- é preservado;
- permanece acessível;
- é facilmente consultável;
- possui histórico;
- não depende da memória humana.

---

# Filosofia

A documentação é tratada como um ativo de primeira classe.

A documentação não existe para acompanhar o sistema.

A documentação faz parte do sistema.

Uma configuração não documentada deve ser considerada incompleta.

---

# Princípios Fundamentais

## Fonte Única

A documentação original existe apenas num local:

```text
GitHub
```

Toda a restante documentação é gerada ou derivada dessa fonte.

---

## Separação Entre Fonte e Publicação

A documentação deve existir em dois formatos distintos:

### Fonte

Markdown

### Publicação

PDF

---

## Separação Entre Consulta e Arquivo

A documentação utilizada diariamente não deve ser confundida com documentação histórica.

---

# Arquitetura Documental

```text
GitHub
(Documentação Fonte)

      │
      ▼

GitHub Actions
(Geração Automática)

      │
      ▼

PDF

      │
      ├──► Nextcloud
      │     Biblioteca Viva
      │
      ▼

Paperless
Arquivo Histórico
```

---

# Função de Cada Sistema

## GitHub

### Papel

Fonte Única da Verdade.

### Responsabilidades

- Markdown original;
- Histórico;
- Revisões;
- Aprovação de alterações.

### Regra

Nenhum PDF deve ser editado manualmente.

---

## GitHub Actions

### Papel

Motor de publicação.

### Responsabilidades

- compilar documentação;
- gerar PDFs;
- publicar artefactos.

---

## Nextcloud

### Papel

Biblioteca Viva.

### Responsabilidades

Disponibilizar sempre a versão mais recente dos documentos.

### Exemplos

```text
Manual da Família

Manual Técnico

SSOT Atual

Livro de Governação
```

### Regra

O Nextcloud contém sempre a versão corrente.

---

## Paperless

### Papel

Arquivo Histórico.

### Responsabilidades

Preservar versões publicadas.

### Exemplos

```text
SSOT v1.0

SSOT v2.0

Manual Família v1.0

Manual Família v2.0
```

### Regra

Paperless preserva marcos históricos.

Não substitui o Nextcloud.

---

# Artefactos Produzidos

## Manual da Família

Origem:

```text
docs/family/
```

Resultado:

```text
Manual_Familia.pdf
```

Público-alvo:

- Ana
- Francisco
- Utilizadores finais

---

## Manual Técnico

Origem:

```text
docs/ssot/
docs/operations/
```

Resultado:

```text
Manual_Tecnico_Homelab.pdf
```

Público-alvo:

- Administrador
- Recuperação
- Auditoria

---

## Livro de Governação

Origem:

```text
docs/philosophy/
docs/history/
docs/operations/decision-records.md
```

Resultado:

```text
Livro_Governacao_Cravo_Homelab.pdf
```

Público-alvo:

- Futuras auditorias
- Evolução estratégica
- Preservação do conhecimento

---

# Fluxo de Publicação

## Passo 1

Editar Markdown.

---

## Passo 2

Commit para GitHub.

---

## Passo 3

Validação automática.

---

## Passo 4

Compilação PDF.

---

## Passo 5

Publicação da versão atual.

---

## Passo 6

Arquivamento de versões históricas.

---

# Gestão de Versões

## Menor

Correções simples.

Exemplo:

```text
v1.0.1
```

---

## Intermédia

Alterações documentais significativas.

Exemplo:

```text
v1.1.0
```

---

## Maior

Mudanças estruturais.

Exemplo:

```text
v2.0.0
```

---

# Classificação dos Documentos

## Ativo

Versão atual.

Disponível no Nextcloud.

---

## Histórico

Versão substituída.

Preservada no Paperless.

---

## Obsoleto

Sem validade operacional.

Mantido apenas por valor histórico.

---

# Regra Fundamental

A documentação nunca deve ser atualizada diretamente em:

```text
PDF
Nextcloud
Paperless
```

A única localização autorizada para edição é:

```text
GitHub
```

Todo o restante conteúdo é considerado derivado.

---

# Definição de Sucesso

O sistema documental será considerado maduro quando:

- toda a documentação possuir origem rastreável;
- os PDFs forem gerados automaticamente;
- a família consultar o Nextcloud;
- o histórico estiver preservado no Paperless;
- o GitHub permanecer a Fonte Única da Verdade.

Nesse momento o conhecimento institucional do Cravo Homelab deixará de depender da memória de qualquer pessoa.
