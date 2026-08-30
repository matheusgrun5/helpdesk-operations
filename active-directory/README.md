# Active Directory — Laboratório Prático

Documentação do laboratório de Active Directory montado com VirtualBox e Windows Server 2022 — simulando um ambiente corporativo real para desenvolvimento de habilidades técnicas em administração de identidades e acessos.

---

## Ambiente do Laboratório

| Item | Configuração |
|------|-------------|
| Virtualização | VirtualBox |
| Sistema Operacional | Windows Server 2022 Standard Evaluation |
| Domínio | corptech.local |
| Controlador de Domínio | WIN-2C7I5KSUOVG |
| RAM alocada | 4096 MB |
| Processadores | 2 |
| Disco | 50 GB |

---

## Estrutura do Domínio

- corptech.local
  - Departamentos
    - TI — Carlos Eduardo (usuário) — GRP_TI_Acesso (grupo de segurança)
    - Financeiro — Ana Lima (usuário) — GRP_Financeiro_Acesso (grupo de segurança)
    - RH — Paula Santos (usuário) — GRP_RH_Acesso (grupo de segurança)

---

## O que foi praticado

- Instalação e configuração do Active Directory Domain Services
- Promoção do servidor a Controlador de Domínio
- Criação de Unidades Organizacionais — OUs
- Criação de usuários e grupos de segurança
- Adição de usuários a grupos
- Desbloqueio de contas
- Redefinição de senhas
- Criação e configuração de GPO

---

## Documentação

| Documento | Descrição |
|-----------|-----------|
| [Configuração do Lab](lab-setup.md) | Instalação e configuração do ambiente |
| [Usuários e Grupos](usuarios-e-grupos.md) | Criação e gerenciamento de usuários |
| [GPO — Painel de Controle](gpo-painel-controle.md) | Política de bloqueio do Painel de Controle |

---

**Analista:** Matheus Grun  
**Última atualização:** Agosto 2026
