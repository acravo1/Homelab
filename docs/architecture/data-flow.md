# Fluxos de Informação

## Objetivo

Este documento descreve a forma como a informação circula dentro do ecossistema Cravo Homelab.

O objetivo é compreender:

- origem dos dados;
- transformação dos dados;
- armazenamento;
- consumo;
- dependências.

Enquanto o documento de dependências descreve a relação entre serviços, este documento descreve a relação entre os dados.

---

# Filosofia

Os dados são o ativo mais importante da infraestrutura.

Os serviços existem para:

- receber dados;
- processar dados;
- armazenar dados;
- apresentar dados.

A arquitetura deve sempre privilegiar:

- rastreabilidade;
- simplicidade;
- recuperação;
- preservação.

---

# Fluxo 1

## Fotografias da Família

### Origem

```text
Telemóvel
```

### Fluxo

```text
Telemóvel
      ↓

Nextcloud

      ↓

NAS QNAP
```

### Destino Final

```text
Nextcloud
```

### Objetivo

Preservação e acesso familiar.

---

# Fluxo 2

## Documento Recebido

### Origem

```text
Email
PDF
Digitalização
Download
```

### Fluxo

```text
Receção

    ↓

Verificação

    ↓

Utilização

    ↓

Arquivo
```

### Implementação

```text
Documento

    ↓

Nextcloud

    ↓

Paperless

    ↓

Arquivo Permanente
```

### Destino Final

```text
Paperless
```

---

# Fluxo 3

## Conhecimento Técnico

### Origem

```text
Experiência
Configuração
Projeto
Incidente
```

### Fluxo

```text
Conhecimento

    ↓

Markdown

    ↓

GitHub
```

### Publicação

```text
GitHub

    ↓

PDF
```

### Consulta

```text
Nextcloud
```

### Arquivo Histórico

```text
Paperless
```

---

# Fluxo 4

## Sensores Domésticos

### Origem

```text
Sensores
```

Exemplos:

- temperatura;
- humidade;
- movimento;
- energia;
- segurança.

### Fluxo

```text
Sensor

    ↓

Home Assistant

    ↓

PostgreSQL

    ↓

Dashboard
```

### Consumidores

- Utilizadores
- Automações
- Notificações

---

# Fluxo 5

## Sistema de Rega

### Origem

```text
Sensores de Humidade
```

### Fluxo

```text
Sensor

    ↓

Home Assistant

    ↓

Lógica de Rega

    ↓

Atuador

    ↓

Jardim
```

### Resultado

Rega automatizada.

---

# Fluxo 6

## Comunicação Familiar

### Origem

```text
Utilizador
```

### Fluxo

```text
Talk

    ↓

Nextcloud

    ↓

Base de Dados
```

### Destino

Outro utilizador.

---

# Fluxo 7

## Acesso Remoto

### Origem

```text
Telemóvel
Portátil
```

### Fluxo

```text
Internet

    ↓

WireGuard

    ↓

Rede Interna

    ↓

Serviços
```

### Objetivo

Extensão segura da rede doméstica.

---

# Fluxo 8

## Resolução de Nomes

### Origem

Pedido de um utilizador.

Exemplo:

```text
nextcloud.lenovo
```

### Fluxo

```text
Cliente

    ↓

AdGuard

    ↓

IP Interno

    ↓

Serviço
```

### Benefício

Eliminar dependência de IPs e portas.

---

# Fluxo 9

## Autenticação

### Origem

Utilizador.

### Fluxo

```text
Utilizador

    ↓

Authentik

    ↓

Serviço

    ↓

Acesso
```

### Objetivo

Identidade única.

---

# Fluxo 10

## Monitorização

### Origem

Serviços.

### Fluxo

```text
Serviço

    ↓

Uptime Kuma

    ↓

Alerta

    ↓

Administrador
```

### Objetivo

Deteção precoce de falhas.

---

# Fluxos Críticos

Consideram-se críticos:

```text
Documentos
```

```text
Fotografias
```

```text
Base de Dados
```

```text
Autenticação
```

```text
DNS
```

```text
Backups
```

---

# Dependência dos Dados

Os dados possuem prioridade superior aos serviços.

Exemplo:

```text
Nextcloud pode ser substituído.

Fotografias não.
```

---

# Regra Fundamental

Ao introduzir um novo serviço deve ser possível responder:

1. De onde vêm os dados?
2. Para onde vão os dados?
3. Quem consome os dados?
4. Como são recuperados?

Se alguma destas respostas não existir, o fluxo está incompleto.

---

# Definição de Sucesso

Qualquer pessoa deve conseguir seguir o percurso de uma informação desde a sua origem até ao seu destino final.

Se um fluxo não puder ser explicado, o sistema ainda não está completamente documentado.
