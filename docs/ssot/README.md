# Fonte Única da Verdade (SSOT)

## Introdução

Este diretório contém a Fonte Única da Verdade (Single Source Of Truth - SSOT) do Cravo Homelab.

Toda a informação considerada atual, validada e operacional deve residir neste local.

O objetivo é garantir que o estado real do sistema possa ser compreendido sem depender:

- da memória dos utilizadores;
- da memória do administrador;
- de conversas passadas;
- de documentação histórica;
- de interpretações produzidas por sistemas de Inteligência Artificial.

Sempre que existir conflito entre múltiplas fontes de informação, prevalecerá a informação documentada e validada neste diretório.

---

# Hierarquia de Confiança

A documentação do projeto encontra-se dividida em quatro níveis de confiança.

## Nível 1 — VALIDADO

Informação suportada por evidência técnica direta.

Exemplos:

- ficheiros de configuração;
- exportações de sistemas;
- backups;
- docker-compose;
- scripts;
- capturas de configuração;
- inventário físico confirmado;
- faturas de aquisição;
- documentação produzida após validação.

Esta é a categoria que deve constituir a maioria da informação presente na SSOT.

---

## Nível 2 — PROVÁVEL

Informação suportada por documentação consistente mas sem validação técnica recente.

Exemplos:

- documentação produzida durante a operação normal;
- relatórios técnicos;
- notas de projeto;
- procedimentos anteriormente utilizados.

Deve ser considerada confiável, mas sujeita a futura verificação.

---

## Nível 3 — HISTÓRICO

Informação que representou corretamente o sistema numa determinada época.

Exemplos:

- arquiteturas anteriores;
- equipamentos substituídos;
- redes antigas;
- serviços removidos;
- migrações concluídas.

Informação histórica nunca deve ser utilizada como referência para o estado atual.

---

## Nível 4 — HIPÓTESE

Informação não validada.

Exemplos:

- inferências;
- hipóteses de trabalho;
- reconstruções documentais;
- interpretações de IA;
- planos futuros.

Não deve ser utilizada para operações, recuperação ou tomada de decisão sem validação prévia.

---

# Regra Fundamental

Nenhuma informação deve transitar para o estado VALIDADO sem evidência primária.

A evidência primária inclui:

- ficheiros de configuração;
- exportações;
- backups;
- código-fonte;
- capturas de configuração;
- registos do sistema;
- documentação produzida diretamente a partir do sistema real.

---

# Organização da SSOT

A Fonte da Verdade está dividida nas seguintes áreas:

```text
ssot/
│
├── hardware.md
├── storage.md
├── network.md
├── services.md
├── users-and-access.md
├── backup-and-recovery.md
└── change-log.md
```

Cada documento deve descrever exclusivamente o estado atual.

Não deve conter:

- notas históricas extensas;
- decisões abandonadas;
- projetos futuros.

Essas informações pertencem ao diretório:

```text
docs/history/
```

---

# Processo de Atualização

Sempre que ocorrer uma alteração relevante:

1. Atualizar a configuração real.
2. Validar o funcionamento.
3. Atualizar a documentação SSOT.
4. Registar a alteração em `change-log.md`.
5. Arquivar documentação anterior quando necessário.

A documentação deve seguir a realidade.

A realidade nunca deve ser adaptada para corresponder à documentação.

---

# Regras para Utilização de Inteligência Artificial

As ferramentas de Inteligência Artificial são consideradas auxiliares de documentação.

Podem:

- resumir;
- organizar;
- auditar;
- explicar;
- sugerir melhorias.

Não podem ser consideradas evidência primária.

Qualquer informação produzida por IA deve ser tratada como:

```text
HIPÓTESE
```

até existir validação independente.

---

# Definição de Sucesso

Uma pessoa sem contacto prévio com o projeto deve conseguir:

- compreender a arquitetura;
- identificar os equipamentos;
- recuperar os serviços;
- restaurar os backups;
- reproduzir a configuração;

utilizando apenas a documentação presente neste repositório.

Quando isso for possível, a missão desta documentação estará cumprida.
