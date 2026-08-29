# Cenário 9 — Pasta Compartilhada sem Permissão

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Categoria:** Permissões / Active Directory  
**Nível:** N1/N2

---

## Relato do usuário

*"Estou tentando acessar uma pasta compartilhada na rede que sempre usei, mas hoje apareceu uma mensagem dizendo que não tenho permissão para acessar. Ontem funcionava normalmente."*

---

## Diagnóstico

| Passo | Verificação | Resultado |
|-------|-------------|-----------|
| 1 | Verificado se colegas acessam normalmente | Colegas acessam — problema isolado no usuário |
| 2 | Verificado tipo de mensagem | "Sem permissão" — pasta existe mas acesso negado |
| 3 | Confirmado com gestor se deve ter acesso | Gestor confirmou que deve ter acesso |
| 4 | Verificado grupo de acesso no Active Directory | Usuário havia sido removido do grupo |
| 5 | Readicionado ao grupo correto | Acesso restaurado |

---

## Solução aplicada

Usuário foi removido do grupo de acesso no Active Directory. Confirmada autorização com o gestor e readicionado ao grupo correto. Acesso à pasta restaurado.

---

## Causa raiz

Remoção do usuário do grupo de segurança no Active Directory — possivelmente por mudança de cargo ou ajuste de política de segurança.

---

## Lição aprendida

Nem todo acesso negado deve ser reativado imediatamente. Confirmar com o gestor antes de agir é uma boa prática de segurança fundamental. Mensagem de "sem permissão" indica que a pasta existe — diferente de "pasta não encontrada" que indica remoção ou renomeação.

---

## Conceitos relacionados

- **Active Directory** — sistema que gerencia usuários, grupos e permissões na rede corporativa
- **Grupo de segurança** — controla quem tem acesso a pastas e recursos compartilhados
- **GPO** — políticas que podem alterar permissões automaticamente

---

## Procedimento relacionado

[Contas e Senhas](../procedimentos/contas-e-senhas.md)
