# Backup e Recuperação

## Objetivo

Este documento descreve a estratégia de proteção, recuperação e continuidade operacional do Cravo Homelab.

Este documento existe para responder a uma pergunta simples:

> O que fazemos quando algo falha?

Todos os sistemas falham.

Discos avariam.

Configurações são corrompidas.

Equipamentos são substituídos.

A verdadeira medida da qualidade de uma infraestrutura não é a ausência de falhas.

É a capacidade de recuperação.

---

# Filosofia de Recuperação

O sistema foi concebido segundo os seguintes princípios:

1. Nenhum dado importante deve existir apenas numa localização.
2. A recuperação deve ser documentada.
3. Os backups devem poder ser restaurados.
4. Um backup não testado não é considerado um backup.
5. A recuperação deve ser possível sem depender da memória do administrador.

---

# Classificação dos Dados

## Dados Críticos

A perda destes dados é considerada inaceitável.

Exemplos:

- Arquivo Paperless
- Documentação GitHub
- Fotografias familiares
- Dados Nextcloud
- Bases de dados PostgreSQL
- Configuração Home Assistant

---

## Dados Importantes

A perda é aceitável mas indesejável.

Exemplos:

- Dashboards
- Templates
- Configurações secundárias

---

## Dados Recriáveis

Podem ser reconstruídos.

Exemplos:

- Contentores Docker
- Imagens Docker
- Cache
- Logs temporários

---

# Componentes que Devem Ter Backup

## Home Assistant

Deve existir cópia de:

- configuração
- automações
- blueprints
- dashboards
- integrações

---

## PostgreSQL

Deve existir cópia de:

- bases de dados
- utilizadores
- permissões

---

## Nextcloud

Deve existir cópia de:

- dados dos utilizadores
- configuração
- aplicações

---

## Paperless

Deve existir cópia de:

- documentos
- base de dados
- etiquetas
- metadados

---

## Authentik

Deve existir cópia de:

- utilizadores
- grupos
- aplicações
- providers
- fluxos

---

## AdGuard Home

Deve existir cópia de:

- configuração DNS
- reescritas
- listas
- filtros

---

## WireGuard

Deve existir cópia de:

- configuração
- peers
- chaves públicas

As chaves privadas devem ser protegidas com especial cuidado.

---

## Nginx Proxy Manager

Deve existir cópia de:

- proxy hosts
- certificados
- definições SSL

---

# Estratégia de Recuperação

## Cenário 1

### Falha de Serviço Individual

Exemplos:

- Nextcloud parado
- PostgreSQL indisponível
- AdGuard sem resposta

Procedimento:

1. Verificar logs.
2. Reiniciar serviço.
3. Validar dependências.
4. Restaurar configuração se necessário.

---

## Cenário 2

### Falha do Lenovo

Exemplos:

- SSD avariado
- Sistema operativo corrompido
- Hardware substituído

Objetivo:

Recuperar todos os serviços utilizando:

- documentação;
- backups;
- repositório Git.

---

## Cenário 3

### Falha do NAS

Objetivo:

Recuperar:

- documentos;
- fotografias;
- arquivo digital;
- armazenamento familiar.

---

## Cenário 4

### Recuperação Total

Situação extrema.

Todo o sistema necessita de ser reconstruído.

Objetivo:

A documentação deve permitir reinstalar a infraestrutura sem depender de conhecimento externo.

---

# Ordem de Recuperação

A recuperação deve seguir esta sequência:

## 1

Infraestrutura Física

- energia
- rede
- switches
- router

---

## 2

Armazenamento

- NAS
- volumes
- iSCSI

---

## 3

Servidor Base

- Ubuntu
- Docker

---

## 4

Serviços Fundamentais

- PostgreSQL
- AdGuard
- Authentik

---

## 5

Serviços Operacionais

- Nextcloud
- Paperless
- Home Assistant

---

## 6

Serviços Complementares

- WireGuard
- NPM
- Uptime Kuma
- OnlyOffice
- Talk

---

# Recovery Point Objective (RPO)

Objetivo futuro.

Determina quanta informação pode ser perdida.

Pendentes de definição:

- Home Assistant
- Nextcloud
- Paperless
- PostgreSQL

---

# Recovery Time Objective (RTO)

Objetivo futuro.

Define quanto tempo é aceitável para recuperar um serviço.

Pendente de definição.

---

# Testes de Recuperação

Deve existir um teste periódico de recuperação.

Objetivos:

- validar backups;
- validar documentação;
- validar procedimentos.

---

# Regra Fundamental

Um backup apenas existe quando:

1. Foi criado.
2. Foi armazenado.
3. Foi documentado.
4. Foi testado.

Se qualquer um destes quatro pontos falhar, o backup não deve ser considerado fiável.

---

# Definição de Sucesso

A recuperação de qualquer sistema crítico deve ser possível apenas com:

- este repositório;
- os backups disponíveis;
- acesso físico ao hardware.

Nenhuma recuperação deve depender exclusivamente da memória do administrador.
