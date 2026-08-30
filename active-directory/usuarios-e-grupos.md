# Usuários e Grupos — Active Directory

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Domínio:** corptech.local

---

## Objetivo

Criar e gerenciar usuários e grupos de segurança no Active Directory — simulando o ambiente corporativo da CorpTech com três departamentos.

---

## Usuários criados

| Nome | Logon | Departamento | OU |
|------|-------|-------------|-----|
| Carlos Eduardo | carlos.eduardo@corptech.local | TI | Departamentos/TI |
| Ana Lima | ana.lima@corptech.local | Financeiro | Departamentos/Financeiro |
| Paula Santos | paula.santos@corptech.local | RH | Departamentos/RH |

---

## Grupos de segurança criados

| Grupo | Tipo | Escopo | OU |
|-------|------|--------|----|
| GRP_TI_Acesso | Security | Global | Departamentos/TI |
| GRP_Financeiro_Acesso | Security | Global | Departamentos/Financeiro |
| GRP_RH_Acesso | Security | Global | Departamentos/RH |

---

## Membros dos grupos

| Grupo | Membro |
|-------|--------|
| GRP_TI_Acesso | Carlos Eduardo |
| GRP_Financeiro_Acesso | Ana Lima |
| GRP_RH_Acesso | Paula Santos |

---

## Procedimentos praticados

### Criar usuário
1. Active Directory Users and Computers
2. Botão direito na OU desejada → New → User
3. Preencher nome, sobrenome e logon
4. Definir senha
5. Configurar opções de conta

### Desbloquear conta
1. Botão direito no usuário → Properties
2. Aba Account
3. Desmarcar Unlock account
4. Clicar em Apply e OK

### Redefinir senha
1. Botão direito no usuário → Reset Password
2. Digitar nova senha nos dois campos
3. Marcar User must change password at next logon se necessário
4. Clicar em OK

### Adicionar usuário a grupo
1. Clicar duas vezes no grupo → aba Members
2. Clicar em Add
3. Digitar o logon do usuário → Check Names → OK
4. Clicar em Apply e OK

---

## Evidências

Print 2 — OU TI com Carlos Eduardo e GRP_TI_Acesso  
Print 3 — Propriedades da conta de Carlos Eduardo

---

**Analista:** Matheus Grun  
**Última atualização:** Agosto 2026
