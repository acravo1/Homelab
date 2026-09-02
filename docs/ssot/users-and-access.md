# Utilizadores e Controlo de Acessos (SSOT)

## Objetivo

Este documento descreve a política de identidade, autenticação e autorização do Cravo Homelab.

O objetivo não é armazenar credenciais.

O objetivo é documentar:

- quem utiliza o sistema;
- quais os perfis existentes;
- como ocorre a autenticação;
- que serviços dependem dessa autenticação;
- quais os princípios de segurança adotados.

---

# Princípios Fundamentais

## Identidade Única

Sempre que possível, cada utilizador deve possuir uma única identidade digital.

Deve evitar-se a criação de múltiplas contas independentes para os mesmos utilizadores em diferentes plataformas.

---

## Menor Privilégio

Cada utilizador deve possuir apenas os acessos necessários às suas funções.

Permissões excessivas aumentam o risco operacional.

---

## Centralização

A autenticação deve ser centralizada sempre que tecnicamente possível.

A existência de múltiplos mecanismos independentes deve ser evitada.

---

# Utilizadores Conhecidos

## Administrador Principal

Estado:

VALIDADO

Função:

Administração da infraestrutura.

Responsabilidades:

- gestão do sistema;
- backups;
- atualizações;
- documentação;
- recuperação de desastre.

Nível de acesso:

Administrador global.

---

## Utilizadores Familiares

Estado:

PROVÁVEL

Função:

Utilização normal dos serviços.

Exemplos:

- armazenamento;
- comunicação;
- consulta documental;
- automação doméstica.

Nível de acesso:

Utilizador standard.

---

# Modelo de Autenticação

## Princípio

Os utilizadores devem autenticar-se o menor número possível de vezes.

Sempre que possível deve existir Single Sign-On (SSO).

---

## Authentik

Estado:

PROVÁVEL

Função:

Provedor central de identidade.

Responsabilidades:

- autenticação;
- autorização;
- gestão de sessões;
- Single Sign-On.

---

# Dependências de Identidade

## Nextcloud

Método preferencial:

Authentik

Função:

Acesso à nuvem privada.

---

## Nextcloud Talk

Método preferencial:

Authentik

Função:

Mensagens e comunicações.

---

## Outros Serviços

Sempre que tecnicamente possível, novos serviços devem integrar-se com o mecanismo central de autenticação existente.

---

# Gestão de Credenciais

## Regra Fundamental

Nenhuma password deve ser armazenada na documentação.

---

## A documentação pode conter

- nomes de contas;
- descrições de acesso;
- responsabilidades;
- dependências.

---

## A documentação nunca deve conter

- passwords;
- segredos;
- chaves privadas;
- tokens;
- certificados privados;
- QR Codes de VPN.

---

# Contas Administrativas

A existência de contas administrativas locais deve ser minimizada.

Sempre que possível:

- utilizar autenticação centralizada;
- reduzir duplicações;
- documentar acessos de emergência.

---

# Acessos de Emergência

Deve existir um procedimento documentado para recuperação de acesso em caso de:

- falha do Authentik;
- perda de credenciais;
- falha de SSO.

O procedimento deve ser documentado em:

```text
docs/operations/disaster-recovery.md
```

---

# Acesso Local

Em condições normais, todos os serviços devem ser acessíveis através da rede local.

A autenticação deve permanecer funcional sem dependências cloud não essenciais.

---

# Acesso Remoto

Método oficial:

WireGuard

Qualquer método alternativo deve ser explicitamente documentado e justificado.

---

# Controlo de Alterações

Sempre que ocorrer:

- criação de utilizador;
- remoção de utilizador;
- alteração do modelo de autenticação;
- introdução de novo fornecedor de identidade;

este documento deve ser atualizado.

---

# Auditorias Futuras

Confirmar:

- utilizadores ativos;
- grupos existentes;
- permissões administrativas;
- integrações Authentik;
- acessos de emergência;
- dependências de SSO.

---

# Regra Final

A identidade é um serviço crítico.

Qualquer alteração ao sistema de autenticação deve ser tratada com o mesmo nível de cuidado que uma alteração à infraestrutura de armazenamento ou aos mecanismos de backup.
