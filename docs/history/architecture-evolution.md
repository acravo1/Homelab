# Evolução Arquitetural do Cravo Homelab

## Objetivo

Este documento descreve a evolução do Cravo Homelab ao longo do tempo.

Ao contrário da SSOT, este documento não descreve exclusivamente o estado atual.

O objetivo é preservar o contexto histórico das decisões tomadas, permitindo compreender:

- como o sistema começou;
- quais os problemas encontrados;
- porque determinadas soluções foram adotadas;
- porque determinadas soluções foram abandonadas.

A história é preservada para fins de referência e aprendizagem.

Este documento não deve ser utilizado para determinar o estado atual da infraestrutura.

Para isso deve ser consultada a documentação presente em:

```text
docs/ssot/
```

---

# Origem

O projeto nasceu da necessidade de resolver problemas concretos da vida digital da família.

Os objetivos iniciais eram:

- reduzir dependências externas;
- centralizar informação;
- eliminar duplicações;
- automatizar tarefas repetitivas;
- melhorar a organização documental;
- aumentar a soberania digital.

Desde o início ficou definido que a tecnologia deveria servir as pessoas e não o contrário.

---

# Primeira Geração

## Infraestrutura Inicial

A primeira arquitetura focava-se essencialmente em:

- Home Assistant;
- armazenamento local;
- documentação dispersa;
- automações domésticas básicas.

Nesta fase o principal objetivo era consolidar conhecimento e reduzir dependências cloud.

---

# Segunda Geração

## Consolidação dos Serviços

A infraestrutura começou a receber novos componentes:

- Paperless-ngx;
- Plex;
- Samba;
- monitorização;
- primeiras experiências com Docker.

O foco passou da automação para a centralização de serviços.

Os primeiros problemas relacionados com gestão documental começaram a ser resolvidos nesta fase.

---

# Terceira Geração

## Centralização Documental

A introdução do Paperless constituiu um dos momentos mais importantes da evolução do sistema.

Pela primeira vez passou a existir um arquivo documental centralizado, pesquisável e independente de pastas dispersas.

Objetivos alcançados:

- OCR automático;
- indexação;
- pesquisa unificada;
- redução da dependência do papel.

---

# Quarta Geração

## Infraestrutura Baseada em Serviços

A plataforma passou a ser concebida como um ecossistema integrado.

Foram introduzidos:

- PostgreSQL;
- autenticação centralizada;
- monitorização;
- gestão de serviços mais estruturada.

Durante esta fase começou a surgir a distinção entre:

- dados;
- identidade;
- serviços.

---

# Quinta Geração

## Nextcloud e Colaboração Familiar

A necessidade de uniformizar o armazenamento familiar conduziu à adoção do Nextcloud.

Objetivos:

- armazenamento centralizado;
- sincronização de ficheiros;
- colaboração documental;
- redução de duplicações.

Esta alteração representou uma mudança significativa na forma como a família interagia com os seus próprios dados.

---

# Sexta Geração

## Soberania de Identidade

A introdução do Authentik permitiu consolidar os múltiplos mecanismos de autenticação.

Objetivos:

- Single Sign-On;
- simplificação de acessos;
- redução de credenciais dispersas;
- centralização de identidade.

Pela primeira vez a autenticação passou a ser tratada como um serviço autónomo da arquitetura.

---

# Sétima Geração

## Infraestrutura de Rede Moderna

A rede foi reestruturada com foco em:

- segmentação;
- isolamento;
- DNS interno;
- VPN.

Foram introduzidos conceitos como:

- VLANs;
- AdGuard Home;
- WireGuard;
- acesso remoto seguro.

A rede passou a ser encarada como um componente ativo da segurança da infraestrutura.

---

# O Período Palmela

Palmela foi o local onde a maior parte da arquitetura moderna foi concebida e desenvolvida.

Durante este período foram definidos:

- princípios de funcionamento;
- processos de automatização;
- estrutura documental;
- plataforma de colaboração familiar;
- arquitetura de acesso remoto.

Grande parte das decisões estruturais atuais têm origem nesta fase.

---

# Migração para Castelo Branco

A mudança para Castelo Branco constituiu o primeiro grande exercício de portabilidade da infraestrutura.

Os objetivos da migração eram:

- preservar o conhecimento;
- validar a documentação;
- reduzir dependências da memória humana;
- consolidar a Fonte Única da Verdade.

Durante o processo verificou-se a existência de documentação histórica divergente, originando uma revisão completa da estratégia documental.

---

# O Nascimento da SSOT

A auditoria documental realizada durante a preparação da migração revelou uma realidade importante:

Nem toda a documentação histórica representava o estado real do sistema.

Foram identificadas:

- arquiteturas antigas;
- planos nunca implementados;
- informações contraditórias;
- decisões posteriormente revertidas.

Como consequência foi criada a política de:

```text
Fonte Única da Verdade (SSOT)
```

bem como a classificação formal de informação:

- VALIDADO
- PROVÁVEL
- HISTÓRICO
- HIPÓTESE

Esta decisão alterou profundamente a governação documental do projeto.

---

# Lições Aprendidas

Ao longo da evolução do Homelab foram identificadas várias conclusões fundamentais:

## A memória falha.

A documentação deve prevalecer sobre recordações.

---

## A documentação envelhece.

Cada documento deve indicar claramente a sua validade.

---

## A complexidade acumula-se.

Cada serviço introduz manutenção futura.

---

## A automatização tem custos.

Automatizar apenas o que vale a pena.

---

## A simplicidade é uma vantagem competitiva.

Uma infraestrutura compreensível é mais valiosa do que uma infraestrutura impressionante.

---

# Estado Atual

O estado atual da infraestrutura não é descrito neste documento.

O estado atual encontra-se documentado em:

```text
docs/ssot/
```

---

# Regra Final

Este documento preserva a história.

A SSOT preserva a verdade atual.

As duas são necessárias.

Nenhuma substitui a outra.
