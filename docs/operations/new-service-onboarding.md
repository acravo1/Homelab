# Introdução de Novos Serviços

## Objetivo

Este documento define o processo obrigatório para introdução de novos serviços no Cravo Homelab.

Antes de qualquer serviço ser considerado parte oficial da infraestrutura, deve cumprir os requisitos aqui definidos.

O objetivo é impedir:

- crescimento descontrolado da plataforma;
- duplicação de funcionalidades;
- dependências desnecessárias;
- perda de conhecimento;
- serviços órfãos.

---

# Filosofia

Cada serviço acrescenta:

- complexidade;
- manutenção;
- consumo de recursos;
- requisitos de backup;
- requisitos de documentação;
- risco operacional.

Por esse motivo, a pergunta inicial não deve ser:

> Posso instalar isto?

Mas sim:

> Porque devo instalar isto?

---

# Processo de Aprovação

## Etapa 1 — Identificação da Necessidade

O proponente deve responder:

### Que problema resolve?

### Quem irá utilizá-lo?

### Qual o benefício esperado?

### Existe uma solução já instalada?

Se já existir uma solução adequada, deve justificar-se porque não pode ser reutilizada.

---

# Etapa 2 — Avaliação Arquitetural

Avaliar:

### Dados

- Que dados irá armazenar?

### Identidade

- Utiliza Authentik?

### Rede

- Necessita de acesso externo?

### Segurança

- Introduz novos riscos?

### Backup

- Como será recuperado?

---

# Etapa 3 — Classificação Inicial

O serviço entra inicialmente em:

```text
LAB
```

e nunca diretamente em produção.

---

# Estados Possíveis

## LAB

Instalação experimental.

Pode ser removido sem aviso.

Sem garantias.

---

## TESTE

Funcional.

Ainda não considerado parte oficial da infraestrutura.

Documentação inicial obrigatória.

---

## PRODUÇÃO

Serviço aprovado.

Documentado.

Incluído na SSOT.

Sujeito a backup.

Sujeito a recuperação.

---

# Critérios para Promoção a Produção

Todos os seguintes critérios devem estar satisfeitos.

---

## Função definida

O serviço possui um propósito claro.

---

## Utilizador identificado

Existe pelo menos um utilizador real.

---

## Documentação criada

O serviço está documentado.

---

## Backup definido

Existe estratégia de recuperação.

---

## Dependências documentadas

Dependências técnicas identificadas.

---

## Benefício validado

O benefício foi comprovado em utilização real.

---

# Informação Mínima Obrigatória

Cada serviço deve possuir um documento próprio.

Exemplo:

```text
docs/services/
    nome-servico.md
```

---

## Estrutura mínima

### Nome

### Função

### Utilizadores

### Dependências

### Dados armazenados

### Estratégia de backup

### Estratégia de recuperação

### Estado

- LAB
- TESTE
- PRODUÇÃO

---

# Razões para Rejeição

O serviço deve ser rejeitado quando:

- duplica funcionalidades existentes;
- não possui utilizadores;
- introduz riscos injustificados;
- exige manutenção excessiva;
- não possui plano de backup;
- não respeita os Princípios Fundamentais.

---

# Processo de Remoção

Um serviço pode ser removido quando:

- deixou de ser utilizado;
- foi substituído;
- representa risco excessivo;
- deixou de justificar recursos.

---

# Antes da Remoção

Documentar:

### Data

### Motivo

### Serviço substituto

### Impacto esperado

Actualizar:

```text
docs/ssot/services.md
```

e

```text
docs/ssot/change-log.md
```

---

# Regra Fundamental

Nenhum serviço pertence oficialmente ao Homelab até estar:

1. Instalado.
2. Testado.
3. Documentado.
4. Integrado em backup.
5. Integrado em recuperação.

Se qualquer um destes pontos falhar, o serviço continua a ser considerado experimental.

---

# Definição de Sucesso

Qualquer pessoa que consulte a documentação deve conseguir responder imediatamente:

- Porque existe este serviço?
- Quem o utiliza?
- Onde estão os seus dados?
- Como fazer backup?
- Como o recuperar?

Se alguma destas respostas não existir, a integração não está concluída.
