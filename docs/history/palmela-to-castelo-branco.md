# Migração Palmela → Castelo Branco

## Objetivo

Este documento regista a migração física e lógica do Cravo Homelab de Palmela para Castelo Branco.

Mais do que uma simples mudança de localização, esta migração representou um momento de revisão arquitetural, consolidação documental e validação da maturidade operacional da infraestrutura.

---

# Contexto

Durante vários anos o Homelab evoluiu progressivamente em Palmela.

Ao longo desse período foram sendo adicionados:

- equipamentos;
- serviços;
- automações;
- armazenamento;
- documentação;
- procedimentos.

Grande parte desse conhecimento encontrava-se distribuído por:

- ficheiros individuais;
- documentos históricos;
- notas técnicas;
- documentação produzida por IA;
- memória do administrador.

A preparação da migração revelou que nem toda a informação permanecia consistente.

---

# Objetivos da Migração

A mudança para Castelo Branco tinha cinco objetivos principais.

## Objetivo 1

Transferir a infraestrutura física sem perda de dados.

---

## Objetivo 2

Garantir continuidade dos serviços familiares.

Exemplos:

- Nextcloud;
- Paperless;
- Home Assistant;
- WireGuard;
- DNS interno.

---

## Objetivo 3

Validar a capacidade de recuperação da infraestrutura.

---

## Objetivo 4

Auditar a documentação existente.

---

## Objetivo 5

Criar uma Fonte Única da Verdade (SSOT).

---

# Descobertas Durante a Auditoria

A revisão documental revelou vários casos de divergência entre documentos produzidos em épocas diferentes.

Foram identificadas referências contraditórias relativamente a:

- hardware;
- armazenamento;
- topologias de rede;
- serviços ativos;
- arquiteturas antigas.

Estas divergências não representavam erros operacionais.

Representavam a evolução natural do sistema ao longo do tempo.

No entanto, dificultavam a identificação do estado atual.

---

# Lições Aprendidas

## A documentação histórica não é a realidade atual

Um documento pode ter sido correto no passado e estar desatualizado no presente.

---

## A memória degrada-se

Mesmo decisões importantes tornam-se difíceis de recordar após vários anos.

---

## A Inteligência Artificial não substitui evidências

Ferramentas de IA podem ajudar a organizar informação mas não devem ser tratadas como fontes primárias.

Sempre que possível devem existir provas documentais.

---

## As faturas e ficheiros reais possuem elevado valor histórico

Faturas, exportações, backups e configurações demonstraram ser fontes mais fiáveis do que recordações ou resumos posteriores.

---

## O GitHub deve ser a memória permanente

A decisão mais importante resultante da migração foi transformar o GitHub na localização oficial do conhecimento institucional do Homelab.

---

# Decisões Arquiteturais Confirmadas Durante a Migração

## Filosofia Local-First

Mantida.

---

## Centralização documental

Mantida.

---

## DNS interno

Mantido.

---

## VPN como método de acesso remoto

Mantido.

---

## Eliminação de duplicações documentais

Reforçada.

---

## Introdução formal da SSOT

Implementada.

---

# Nascimento da Estrutura Documental Moderna

Durante esta fase foi adotada a divisão formal:

```text
docs/

├── philosophy/
├── ssot/
├── history/
├── operations/
└── family/
```

A partir deste momento cada documento passa a possuir um propósito definido.

---

# Estado da Infraestrutura no Final da Migração

A infraestrutura entra em Castelo Branco com os seguintes objetivos estratégicos:

- aumentar a qualidade da documentação;
- reforçar a auditoria aos serviços;
- validar configurações reais;
- melhorar os processos de recuperação;
- reduzir dependência da memória humana.

---

# Significado Histórico

A migração Palmela → Castelo Branco marca o fim da fase experimental do Homelab.

Representa a transição para uma infraestrutura documentada, auditável e governada segundo princípios formais.

É neste momento que nasce oficialmente a Fonte Única da Verdade do Cravo Homelab.

---

# Conclusão

A mudança de localização foi apenas o evento físico.

A verdadeira transformação ocorreu ao nível da documentação e da governação do conhecimento.

O sistema deixou de depender principalmente da memória do administrador e passou a depender de documentação estruturada, versionada e auditável.

Este é o principal legado da migração para Castelo Branco.
