# Princípios de Arquitetura

## Objetivo

Este documento define os princípios arquiteturais que orientam a evolução técnica do Cravo Homelab.

Estes princípios complementam os Princípios Fundamentais do projeto.

Enquanto os Princípios Fundamentais explicam "porquê", este documento explica "como".

---

# Princípio 1

## Local First

Os serviços devem funcionar localmente sempre que possível.

A rede local é considerada a localização natural dos serviços.

O acesso remoto é um complemento.

Não uma dependência.

---

# Princípio 2

## Single Source of Truth

Cada informação deve possuir uma única localização autoritativa.

Exemplos:

```text
Documentação Técnica
    ↓
GitHub

Documentos Ativos
    ↓
Nextcloud

Arquivo Permanente
    ↓
Paperless
```

A duplicação é considerada dívida técnica.

---

# Princípio 3

## DNS Antes de Endereços IP

Os serviços devem ser acedidos por nome.

Exemplos:

```text
nextcloud.lenovo
paperless.lenovo
homeassistant.lenovo
```

e não por:

```text
192.168.x.x
```

ou

```text
:portas
```

---

# Princípio 4

## Segurança por Segmentação

A rede deve assumir que nem todos os dispositivos são confiáveis.

Sempre que possível:

- separar dispositivos;
- limitar acessos;
- reduzir privilégios.

---

# Princípio 5

## Menor Privilégio

Cada utilizador, dispositivo ou serviço deve possuir apenas os acessos necessários para cumprir a sua função.

---

# Princípio 6

## Serviços Especializados

Cada serviço deve ter uma responsabilidade principal.

Exemplos:

```text
Nextcloud
    ↓
Documentos ativos

Paperless
    ↓
Arquivo

Authentik
    ↓
Identidade

PostgreSQL
    ↓
Dados
```

Evitar sistemas com responsabilidades excessivamente abrangentes.

---

# Princípio 7

## Dados Antes dos Serviços

Os dados são mais importantes do que as aplicações.

Uma aplicação pode ser substituída.

Os dados não.

Qualquer decisão deve privilegiar:

- preservação dos dados;
- portabilidade;
- recuperação.

---

# Princípio 8

## Infraestrutura Como Código

Sempre que possível:

- configurações;
- documentação;
- scripts;
- automações;

devem existir sob controlo de versão.

O estado da infraestrutura não deve depender exclusivamente de interfaces gráficas.

---

# Princípio 9

## Recuperação Acima da Instalação

Instalar um serviço é fácil.

Recuperá-lo após desastre é o verdadeiro teste.

Sempre que um novo componente for introduzido deve existir um plano de recuperação documentado.

---

# Princípio 10

## Falhar de Forma Elegante

A falha de um componente não deve provocar a falha de toda a infraestrutura.

Sempre que possível:

- isolar dependências;
- segmentar responsabilidades;
- reduzir pontos únicos de falha.

---

# Princípio 11

## Observabilidade

Tudo o que é importante deve poder ser observado.

Exemplos:

- disponibilidade;
- armazenamento;
- rede;
- bases de dados;
- automações.

O que não pode ser observado dificilmente pode ser administrado.

---

# Princípio 12

## Simplicidade Sustentável

A arquitetura mais impressionante nem sempre é a melhor.

A arquitetura mais sustentável é aquela que:

- pode ser explicada;
- pode ser mantida;
- pode ser recuperada;
- pode ser documentada.

---

# Princípio 13

## Compatibilidade com a Família

Qualquer decisão técnica deve ser avaliada também do ponto de vista dos utilizadores finais.

A melhor solução técnica não é necessariamente a melhor solução operacional.

---

# Princípio 14

## Evolução Incremental

Evitar reescritas completas.

Preferir:

```text
Pequenas melhorias contínuas
```

em vez de:

```text
Grandes revoluções periódicas
```

---

# Princípio 15

## Conhecimento Preservado

Uma decisão que não foi documentada terá de ser redescoberta.

O custo dessa redescoberta é frequentemente superior ao custo de documentar a decisão inicialmente.

---

# Definição de Sucesso

Uma alteração arquitetural será considerada adequada quando:

- respeitar os princípios fundamentais;
- respeitar estes princípios arquiteturais;
- simplificar a operação;
- preservar dados;
- melhorar a sustentabilidade futura do sistema.

Quando existir dúvida entre duas soluções tecnicamente válidas, deve ser escolhida a solução que melhor respeite estes princípios.
