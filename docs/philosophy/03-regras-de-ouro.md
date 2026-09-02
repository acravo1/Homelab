# As Regras de Ouro do Cravo Homelab

## Objetivo

Este documento reúne um conjunto de regras simples que resultam da experiência acumulada durante a evolução do Cravo Homelab.

Não são regras técnicas.

São regras de sobrevivência.

O seu objetivo é evitar erros que historicamente conduzem a:

- perda de dados;
- duplicação de informação;
- complexidade desnecessária;
- degradação documental;
- dependência excessiva da memória humana.

---

# Regra 1

## Nunca confiar exclusivamente na memória.

Se uma informação for importante, deve ser documentada.

Se não estiver documentada, deve assumir-se que será esquecida.

---

# Regra 2

## Nenhum serviço entra em produção sem documentação.

Antes de um serviço ser considerado oficial deve existir documentação mínima:

- finalidade;
- dependências;
- backup;
- recuperação.

---

# Regra 3

## Nenhum serviço entra em produção sem um plano de saída.

Antes de instalar um serviço deve ser possível responder:

```text
Como o removo?
```

---

# Regra 4

## A documentação é parte da infraestrutura.

Uma alteração não está concluída até a documentação ser atualizada.

---

# Regra 5

## O GitHub é a única fonte autorizada para edição.

Nenhum PDF deve ser editado.

Nenhum documento arquivado deve ser editado.

Toda a alteração começa no GitHub.

---

# Regra 6

## Os PDFs são publicações e não fontes.

A fonte é sempre:

```text
Markdown
```

O PDF é apenas uma representação.

---

# Regra 7

## O Nextcloud é a biblioteca viva.

Contém a versão atual dos documentos.

Apenas a versão mais recente.

---

# Regra 8

## O Paperless é o arquivo permanente.

Contém documentos históricos.

Nunca substitui o GitHub.

Nunca substitui o Nextcloud.

---

# Regra 9

## Duplicação é considerada dívida técnica.

Sempre que existir:

- o mesmo ficheiro em vários locais;
- a mesma configuração em vários documentos;
- credenciais repetidas;
- informação contraditória;

deve iniciar-se um processo de consolidação.

---

# Regra 10

## Automatizar apenas o que vale a pena.

Nem tudo o que pode ser automatizado merece ser automatizado.

A automação deve:

- poupar tempo;
- reduzir erros;
- simplificar tarefas.

---

# Regra 11

## A rede local vem primeiro.

Um serviço que não funciona dentro da própria casa está incompleto.

O acesso remoto é um complemento.

Não uma dependência.

---

# Regra 12

## A privacidade é a configuração por defeito.

Partilhar é uma decisão consciente.

Expor é uma exceção.

---

# Regra 13

## As decisões importantes precisam de contexto.

Sempre que uma alteração for estrutural:

- criar ADR;
- registrar motivo;
- registrar consequências.

---

# Regra 14

## Um backup não testado não é um backup.

É apenas uma esperança.

---

# Regra 15

## Um sistema simples é um sistema sustentável.

A pergunta correta não é:

```text
Posso fazer?
```

A pergunta correta é:

```text
Vale a pena fazer?
```

---

# Regra 16

## Os factos prevalecem sobre as interpretações.

Em caso de conflito:

1. Configuração real;
2. Exportações;
3. Backups;
4. GitHub;
5. Documentação histórica;
6. Memória humana;
7. Respostas de IA.

---

# Regra 17

## A evolução não apaga a história.

O passado deve ser preservado.

Mas claramente marcado como passado.

---

# Regra 18

## A tecnologia existe para servir a família.

Esta é a regra suprema.

Qualquer solução que complique desnecessariamente a vida da família deve ser reconsiderada.

---

# Cláusula Final

Sempre que existir dúvida entre duas soluções tecnicamente válidas, deve ser escolhida a que:

- respeite os princípios fundamentais;
- reduza complexidade;
- aumente a sustentabilidade;
- exija menos memória humana;
- beneficie mais a família.

Estas regras foram escritas para que o sistema sobreviva ao tempo, às mudanças tecnológicas e ao esquecimento inevitável da condição humana.
