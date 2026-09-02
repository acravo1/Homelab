# Lições Aprendidas

## Objetivo

Este documento existe para preservar conhecimento adquirido através de sucessos, falhas, erros, migrações, auditorias e decisões tomadas ao longo da evolução do Cravo Homelab.

O objetivo não é documentar configurações.

O objetivo é documentar sabedoria operacional.

Enquanto a SSOT documenta o estado atual do sistema, este documento preserva aquilo que o sistema ensinou aos seus administradores.

---

# Filosofia

Os erros são inevitáveis.

O desperdício de um erro é opcional.

Sempre que um problema exigir investigação significativa, revelar uma falha de conceção ou obrigar a alterar a arquitetura, a lição aprendida deve ser registada.

---

# Lição 001

## A memória não é uma base de dados.

### Contexto

Ao preparar a migração de Palmela para Castelo Branco surgiram descrições contraditórias sobre:

- hardware;
- armazenamento;
- arquitetura;
- serviços instalados.

### Conclusão

A memória deve ser considerada uma fonte auxiliar.

Nunca uma fonte de verdade.

### Consequência

Criação da SSOT.

---

# Lição 002

## A documentação envelhece.

### Contexto

Vários documentos inicialmente corretos deixaram de representar a realidade devido à evolução natural da infraestrutura.

### Conclusão

Todo o documento deve indicar claramente se é:

- Atual;
- Histórico;
- Obsoleto.

### Consequência

Separação formal entre:

```text
docs/ssot/
```

e

```text
docs/history/
```

---

# Lição 003

## A IA não substitui evidências.

### Contexto

Durante a auditoria documental surgiram informações plausíveis mas não suportadas por evidências diretas.

### Conclusão

Uma IA consegue organizar conhecimento.

Não consegue substituir:

- ficheiros reais;
- exportações;
- backups;
- faturas;
- configurações.

### Consequência

Criação dos níveis:

```text
VALIDADO
PROVÁVEL
HISTÓRICO
HIPÓTESE
```

---

# Lição 004

## A complexidade cobra juros.

### Contexto

Cada novo serviço introduziu:

- mais configurações;
- mais documentação;
- mais dependências.

### Conclusão

A complexidade não desaparece.

Acumula-se.

### Consequência

Cada novo serviço deve justificar a sua existência.

---

# Lição 005

## Um backup não testado é apenas uma teoria.

### Contexto

Criar backups é fácil.

Recuperar sistemas é difícil.

### Conclusão

A única forma de validar um backup é utilizá-lo.

### Consequência

A recuperação passou a fazer parte da documentação.

---

# Lição 006

## A documentação deve acompanhar a alteração.

### Contexto

Muitas discrepâncias surgiram porque alterações foram implementadas sem o respetivo registo documental.

### Conclusão

Uma alteração não está concluída até a documentação ser atualizada.

### Consequência

Introdução do Change Log.

---

# Lição 007

## Local First simplifica tudo.

### Contexto

Sempre que um serviço dependia excessivamente de terceiros surgiam limitações, dependências ou perda de controlo.

### Conclusão

Os serviços funcionam melhor quando a casa continua funcional mesmo sem Internet.

### Consequência

A filosofia Local First tornou-se um princípio fundamental.

---

# Lição 008

## A melhor automação é quase invisível.

### Contexto

As automações mais bem sucedidas são aquelas que raramente exigem intervenção humana.

### Conclusão

A automação existe para remover trabalho, não para criar sistemas complexos.

### Consequência

Qualquer nova automação deve justificar claramente o benefício obtido.

---

# Lição 009

## A tecnologia muda mais depressa do que os princípios.

### Contexto

Hardware, software e serviços mudaram repetidamente ao longo dos anos.

### Conclusão

Os princípios sobreviveram a todas as mudanças.

### Consequência

A filosofia passou a ser documentada explicitamente.

---

# Lição 010

## O conhecimento é um ativo.

### Contexto

A preparação da mudança demonstrou que reconstruir conhecimento é mais difícil do que reinstalar software.

### Conclusão

A documentação tem o mesmo valor estratégico que os dados.

### Consequência

GitHub adotado como memória permanente do projeto.

---

# Como Adicionar Novas Lições

Sempre que ocorrer:

- uma falha importante;
- uma migração;
- uma alteração estrutural;
- um incidente relevante;
- uma descoberta significativa;

deve ser considerada a criação de uma nova entrada.

---

# Regra Fundamental

Configurações explicam como.

Lições aprendidas explicam porquê.

Os dois tipos de conhecimento são igualmente importantes.

---

# Definição de Sucesso

Daqui a dez anos, uma pessoa que leia este documento deverá conseguir evitar erros que já foram cometidos anteriormente e compreender as razões que moldaram o Cravo Homelab ao longo da sua evolução.
