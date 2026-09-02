# Interpretação dos Princípios Fundamentais

Este documento explica a origem, significado e aplicação prática dos Dez Princípios do Cravo Homelab.

Os princípios não foram criados de forma teórica.

Cada um deles resulta de experiências reais, erros cometidos, problemas encontrados e soluções que se revelaram eficazes ao longo da evolução do sistema.

O objetivo deste documento não é definir regras rígidas para sempre.

O objetivo é fornecer um enquadramento lógico que permita tomar decisões consistentes ao longo dos anos, mesmo quando o hardware, software ou necessidades da família mudarem.

---

# I. A tecnologia existe para servir a família

A infraestrutura não existe para servir o administrador.

Existe para servir os seus utilizadores.

Nenhuma implementação técnica tem valor se complicar desnecessariamente a vida das pessoas que utilizam o sistema.

Uma solução tecnicamente elegante mas difícil de utilizar é inferior a uma solução simples e compreensível.

Quando existir conflito entre sofisticação técnica e utilidade prática, deve prevalecer a utilidade prática.

---

# II. A rede local é a casa natural dos serviços

A arquitetura do Homelab segue uma filosofia Local First.

Os serviços devem permanecer operacionais mesmo quando existem falhas temporárias na ligação à Internet.

O acesso remoto é uma funcionalidade complementar e não um requisito para o funcionamento normal da casa.

A rede local deve fornecer:

- acesso aos ficheiros;
- acesso à automação;
- acesso aos documentos;
- acesso aos serviços familiares;
- acesso à monitorização.

A Internet deve acrescentar conveniência.

Nunca dependência.

---

# III. Cada informação deve possuir uma única Fonte da Verdade

A duplicação de informação conduz inevitavelmente a erros.

Quando o mesmo documento existe em vários locais diferentes, torna-se impossível saber qual a versão correta.

A estratégia adotada pelo Homelab é definir uma localização oficial para cada tipo de informação.

Exemplos:

- Documentação técnica → GitHub.
- Arquivo documental → Paperless.
- Ficheiros ativos → Nextcloud.
- Configuração operacional → ficheiros de configuração versionados.

Sempre que houver conflito, apenas uma localização deve ser considerada autoritária.

---

# IV. A automatização deve eliminar trabalho

Automatizar por diversão é permitido.

Automatizar por obrigação é preferível.

Qualquer automatização introduz complexidade.

Por esse motivo, apenas devem ser implementadas automatizações que reduzam esforço humano, risco de erro ou trabalho repetitivo.

A pergunta correta não é:

"Posso automatizar isto?"

A pergunta correta é:

"Vale a pena automatizar isto?"

---

# V. A simplicidade é uma funcionalidade

A complexidade possui custos invisíveis.

Cada aplicação adicional:

- necessita de manutenção;
- necessita de backups;
- necessita de atualizações;
- necessita de documentação.

A solução mais simples que cumpra os requisitos deve ser considerada a solução preferencial.

Não existe mérito em complexidade desnecessária.

---

# VI. A privacidade é o estado por defeito

A proteção dos dados familiares deve existir desde o desenho inicial das soluções.

Privacidade não significa isolamento total.

Significa controlo consciente sobre quem pode aceder aos dados e em que circunstâncias.

Sempre que possível:

- os dados permanecem em infraestrutura própria;
- o acesso é controlado;
- os serviços externos são reduzidos ao mínimo necessário.

---

# VII. Os factos valem mais do que a memória

Este princípio tornou-se particularmente importante durante a reconstrução documental do sistema.

Ao longo do tempo surgiram:

- versões diferentes da arquitetura;
- documentos históricos;
- planos que nunca chegaram a ser implementados;
- alterações esquecidas;
- interpretações de inteligência artificial.

A memória humana é falível.

A interpretação automática também.

Sempre que existir conflito, a prioridade deve ser atribuída a evidências concretas:

- ficheiros de configuração;
- exportações;
- backups;
- documentação validada;
- registos históricos;
- comprovativos de aquisição.

Uma evidência documentada tem prioridade sobre qualquer recordação.

---

# VIII. O GitHub é a memória permanente do sistema

Os sistemas sobrevivem através da documentação.

Não através da memória dos seus administradores.

O GitHub foi escolhido como repositório central porque fornece:

- histórico;
- controlo de alterações;
- rastreabilidade;
- recuperação de versões anteriores.

O conhecimento operacional do Homelab deve residir no repositório e não exclusivamente numa pessoa.

---

# IX. A evolução não apaga a história

Uma decisão antiga pode já não ser correta.

Continua, no entanto, a ser parte da história do sistema.

A documentação deve preservar:

- o estado atual;
- os estados anteriores;
- as razões das alterações.

Eliminar o passado dificulta a compreensão do presente.

Por essa razão, os documentos históricos devem ser preservados, mas claramente marcados como históricos.

---

# X. O sistema deve sobreviver ao seu criador

O maior objetivo desta documentação é a continuidade.

Qualquer pessoa que disponha do repositório documental deve conseguir compreender:

- a arquitetura;
- os serviços;
- os dados;
- os procedimentos de recuperação;
- os objetivos do sistema.

Uma infraestrutura que depende exclusivamente da memória do seu criador contém uma falha estrutural.

O sucesso do projeto será atingido quando a documentação for suficiente para reconstruir o sistema sem necessidade de consultar o autor.

---

# Conclusão

A tecnologia utilizada pelo Homelab irá inevitavelmente mudar.

Novos equipamentos serão adquiridos.

Outros serão abandonados.

Novos serviços surgirão.

Outros desaparecerão.

Os princípios aqui descritos devem manter-se estáveis ao longo dessas mudanças.

A arquitetura pode evoluir.

A filosofia deve permanecer.
