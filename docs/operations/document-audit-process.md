# Processo de Auditoria Documental

## Objetivo

Este documento define o processo oficial de auditoria documental do Cravo Homelab.

O objetivo é garantir que a documentação continua alinhada com a realidade observável da infraestrutura.

A documentação só possui valor quando reflete corretamente o sistema que descreve.

---

# Filosofia

Toda a documentação tende a divergir da realidade ao longo do tempo.

As razões incluem:

- alterações não documentadas;
- memória humana imperfeita;
- documentação desatualizada;
- projetos abandonados;
- mudanças de arquitetura;
- reconstruções incompletas.

A auditoria documental existe para corrigir essa deriva.

---

# Princípio Fundamental

A realidade tem sempre prioridade sobre a documentação.

Nunca alterar o sistema para coincidir com a documentação.

Corrigir a documentação para refletir o sistema real.

---

# Frequência

## Auditoria Contínua

Sempre que uma alteração relevante ocorre.

---

## Auditoria Trimestral

Revisão dos sistemas críticos.

---

## Auditoria Anual

Revisão integral da infraestrutura.

---

# Fontes de Evidência

As auditorias devem utilizar preferencialmente:

## Nível 1

Evidências primárias.

Exemplos:

- ficheiros de configuração;
- docker-compose;
- exportações;
- backups;
- inventários;
- capturas de configuração;
- comandos executados.

---

## Nível 2

Evidências secundárias.

Exemplos:

- documentação operacional;
- notas técnicas;
- relatórios.

---

## Nível 3

Evidências auxiliares.

Exemplos:

- memória humana;
- mensagens;
- respostas de IA.

Estas nunca devem ser consideradas suficientes por si só.

---

# Processo de Auditoria

## Passo 1

Selecionar área.

Exemplos:

- Hardware
- Rede
- Serviços
- Armazenamento
- Automações

---

## Passo 2

Comparar:

```text
Estado Real
      vs
SSOT
```

---

## Passo 3

Registar divergências.

---

## Passo 4

Classificar cada divergência.

### Erro Documental

A realidade está correta.

A documentação está errada.

---

### Configuração Obsoleta

A documentação descreve um estado antigo.

---

### Hipótese Não Confirmada

Existe informação sem evidência suficiente.

---

### Desvio Operacional

A infraestrutura alterou-se sem atualização documental.

---

# Tratamento de Divergências

## Regra 1

Identificar evidência.

---

## Regra 2

Atualizar classificação.

Exemplo:

```text
PROVÁVEL
    ↓
VALIDADO
```

---

## Regra 3

Atualizar documentação.

---

## Regra 4

Registar no Change Log.

---

# Auditoria de Hardware

Validar:

- equipamentos;
- RAM;
- discos;
- interfaces de rede.

---

# Auditoria de Rede

Validar:

- VLANs;
- ACLs;
- DHCP;
- DNS;
- VPN;
- SSIDs.

---

# Auditoria de Serviços

Validar:

- serviços ativos;
- versões;
- dependências;
- utilizadores.

---

# Auditoria de Armazenamento

Validar:

- NAS;
- volumes;
- montagens;
- backups.

---

# Auditoria de Documentação

Validar:

- documentos duplicados;
- documentos órfãos;
- documentos obsoletos.

---

# Sinais de Alerta

Os seguintes indicadores sugerem necessidade de auditoria:

- "Tenho ideia que..."
- "Penso que..."
- "Julgo que..."
- "Deve estar..."
- "Antigamente era..."

Sempre que estas expressões surgirem, deve procurar-se evidência objetiva.

---

# Papel da Inteligência Artificial

A IA pode:

- identificar inconsistências;
- relacionar documentos;
- sugerir hipóteses;
- apoiar auditorias.

A IA não substitui evidência técnica.

Toda a informação produzida por IA inicia-se como:

```text
HIPÓTESE
```

até validação independente.

---

# Critério de Qualidade

Uma área é considerada auditada quando:

- existe documentação;
- existe evidência;
- não existem contradições conhecidas.

---

# Indicador de Maturidade

Um sistema documental maduro apresenta:

- pouca informação classificada como HIPÓTESE;
- elevada percentagem de informação VALIDADA;
- histórico preservado;
- documentação atualizada.

---

# Definição de Sucesso

Uma auditoria é considerada concluída quando:

1. A realidade foi observada.
2. A documentação foi corrigida.
3. As divergências foram explicadas.
4. As evidências ficaram registadas.

Nesse momento a Fonte Única da Verdade recupera a sua integridade.
