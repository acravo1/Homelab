# Convenções de Nomenclatura

## Objetivo

Este documento define as convenções oficiais de nomenclatura utilizadas no Cravo Homelab.

O objetivo é garantir:

- consistência;
- previsibilidade;
- facilidade de manutenção;
- facilidade de pesquisa;
- redução de ambiguidades.

As convenções aplicam-se a:

- equipamentos;
- serviços;
- sensores;
- automações;
- scripts;
- documentos;
- projetos.

---

# Princípio Fundamental

Um nome deve permitir compreender um objeto sem necessidade de contexto adicional.

Evitar:

```text
sensor1
novo_sensor
teste
coisa
```

Preferir:

```text
sensor_humidade_jardim_norte
```

---

# Idioma

## Regra

Utilizar Português (Portugal).

Exemplos:

✅

```text
rega_jardim
porta_entrada
temperatura_sala
```

❌

```text
garden_irrigation
frontdoor
livingroom_temp
```

---

# Caracteres Permitidos

Utilizar apenas:

```text
a-z
0-9
_
```

Evitar:

```text
espaços
acentos
caracteres especiais
```

---

# Home Assistant

## Sensores

Formato:

```text
sensor_<tipo>_<local>
```

Exemplos:

```text
sensor_temperatura_sala
sensor_humidade_jardim
sensor_movimento_ginasio
```

---

## Interruptores

Formato:

```text
switch_<equipamento>_<local>
```

Exemplos:

```text
switch_tomada_sala
switch_rega_horta
```

---

## Luzes

Formato:

```text
light_<zona>
```

Exemplos:

```text
light_sala
light_cozinha
light_jardim
```

---

## Scripts

Formato:

```text
script_<funcao>
```

Exemplos:

```text
script_notificacao_voz
script_rega_manual
script_boas_noites
```

---

## Automações

Formato:

```text
[Area] Descrição
```

Exemplos:

```text
[Jardim] Rega Inteligente
[Segurança] Alerta Intrusão
[Sala] Desligar Luzes
```

---

# Docker

## Contentores

Formato:

```text
servico-funcao
```

Exemplos:

```text
postgres-core
paperless-ngx
adguard-home
uptime-kuma
```

---

## Redes Docker

Formato:

```text
network_<funcao>
```

Exemplos:

```text
network_core
network_proxy
network_iot
```

---

## Volumes

Formato:

```text
volume_<servico>
```

Exemplos:

```text
volume_nextcloud
volume_postgres
volume_paperless
```

---

# Documentação

## Documentos

Formato:

```text
nome-documento.md
```

Exemplos:

```text
hardware.md
network.md
paperless.md
```

---

## Evitar

```text
Documento Final.md
Versao Nova.md
Manual Atualizado.md
```

---

# PDFs Gerados

Formato:

```text
Nome_Oficial_vX.Y.pdf
```

Exemplos:

```text
Manual_Familia_v1.0.pdf
SSOT_v1.0.pdf
Livro_Governacao_v1.0.pdf
```

---

# ADRs

Formato:

```text
ADR-XXX
```

Exemplos:

```text
ADR-001
ADR-002
ADR-003
```

---

# Projetos

Formato:

```text
NOME_MAIUSCULAS
```

Exemplos:

```text
AEGIS
CRAVO_HOMELAB
```

---

# Equipamentos

Formato:

```text
TIPO-LOCAL
```

Exemplos:

```text
EAP653-SALA
QNAP-SALA
LENOVO-HOST
```

---

# Zonas da Habitação

Nomes oficiais:

```text
Sala
Cozinha
Ginásio
Jardim
Entrada
Escritório
```

Evitar nomes alternativos para a mesma área.

---

# Regra Fundamental

Se um nome exigir explicações frequentes, o nome está errado.

Um bom nome deve ser:

- simples;
- previsível;
- único;
- compreensível.

---

# Definição de Sucesso

Qualquer elemento da infraestrutura deve poder ser identificado apenas pelo seu nome.

A nomenclatura deve reduzir a necessidade de documentação adicional e facilitar a manutenção futura do sistema.
