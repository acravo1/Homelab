# Classificação de Informação

## Objetivo

Este documento define a classificação oficial utilizada na documentação do Cravo Homelab.

O objetivo é permitir que qualquer pessoa consiga avaliar rapidamente o grau de confiança de uma informação.

Nem todas as informações possuem o mesmo nível de evidência.

Nem todos os sistemas possuem o mesmo grau de maturidade.

Por esse motivo, toda a documentação deve utilizar as classificações definidas neste documento.

---

# Princípio Fundamental

Uma informação sem classificação deve ser considerada:

```text
NÃO VALIDADA
```

---

# Classificação de Confiança

Estas classificações indicam o grau de confiança da informação.

---

# VALIDADO

## Definição

Informação suportada por evidência primária.

---

## Exemplos

- ficheiros de configuração;
- exportações;
- backups;
- faturas;
- screenshots;
- código fonte;
- estado observado diretamente.

---

## Grau de Confiança

Muito Elevado

---

## Utilização

Pode ser utilizada para:

- auditorias;
- recuperação;
- tomada de decisão;
- documentação oficial.

---

# PROVÁVEL

## Definição

Informação consistente mas ainda não confirmada através de evidência primária recente.

---

## Exemplos

- documentação operacional;
- notas históricas recentes;
- documentação anteriormente validada.

---

## Grau de Confiança

Elevado

---

## Utilização

Pode orientar trabalhos futuros.

Deve ser validada sempre que possível.

---

# HIPÓTESE

## Definição

Informação que parece plausível mas que ainda não possui validação suficiente.

---

## Exemplos

- reconstruções documentais;
- interpretações;
- planos futuros;
- conclusões produzidas por IA;
- pressupostos.

---

## Grau de Confiança

Baixo

---

## Utilização

Não deve fundamentar alterações críticas.

Necessita de validação.

---

# HISTÓRICO

## Definição

Informação que foi verdadeira numa determinada época mas que pode já não representar a realidade atual.

---

## Exemplos

- arquiteturas antigas;
- hardware substituído;
- serviços removidos;
- redes anteriores.

---

## Grau de Confiança

Pode ser elevado.

Mas apenas relativamente ao passado.

---

## Utilização

Contexto e preservação histórica.

Nunca deve ser assumida como representativa do estado atual.

---

# Ciclo de Vida da Confiança

```text
HIPÓTESE
    ↓

PROVÁVEL
    ↓

VALIDADO
```

ou

```text
PROVÁVEL
    ↓
HISTÓRICO
```

---

# Classificação de Serviços

Estas classificações indicam o estado operacional de um sistema.

---

# LAB

## Definição

Sistema experimental.

---

## Características

- sem garantias;
- sem suporte;
- documentação mínima;
- sujeito a remoção.

---

## Exemplo

Serviço recentemente instalado.

---

# TESTE

## Definição

Sistema funcional mas ainda em validação.

---

## Características

- testes reais;
- documentação inicial;
- utilização limitada.

---

## Objetivo

Avaliar viabilidade.

---

# PRODUÇÃO

## Definição

Sistema oficialmente integrado no Homelab.

---

## Requisitos

- documentação;
- backup;
- estratégia de recuperação;
- utilizadores reais.

---

## Características

Alterações devem ser controladas.

---

# OBSOLETO

## Definição

Sistema abandonado ou substituído.

---

## Características

Não deve receber alterações.

Mantido apenas para referência histórica.

---

# Ciclo de Vida dos Serviços

```text
LAB
  ↓

TESTE
  ↓

PRODUÇÃO
  ↓

OBSOLETO
```

---

# Classificação de Documentos

## Ativo

Documento utilizado atualmente.

---

## Histórico

Documento preservado para consulta.

---

## Arquivado

Documento sem utilização operacional.

---

## Obsoleto

Documento mantido apenas para referência histórica.

---

# Regras de Utilização

## Regra 1

Todo o documento técnico deve indicar explicitamente a classificação da informação.

---

## Regra 2

Toda a entrada na SSOT deve procurar atingir estado:

```text
VALIDADO
```

---

## Regra 3

Informações baseadas apenas em memória nunca devem ser marcadas como:

```text
VALIDADO
```

---

## Regra 4

Informação produzida por IA deve iniciar sempre como:

```text
HIPÓTESE
```

até validação posterior.

---

## Regra 5

Documentação histórica deve permanecer separada da SSOT.

---

# Definição de Sucesso

Qualquer leitor deve conseguir responder imediatamente:

- Posso confiar nesta informação?
- Esta informação descreve o presente ou o passado?
- Este serviço está em produção ou apenas em teste?

consultando apenas a classificação atribuída.
