# Configuração do Laboratório — Active Directory

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Ambiente:** VirtualBox + Windows Server 2022

---

## Objetivo

Montar um laboratório local de Active Directory para praticar administração de usuários, grupos, OUs e GPOs em ambiente simulado — desenvolvendo habilidades técnicas comprovadas para atuação em suporte N1/N2.

---

## Especificações da Máquina Virtual

| Recurso | Configuração |
|---------|-------------|
| Software de virtualização | VirtualBox |
| Sistema operacional | Windows Server 2022 Standard Evaluation |
| Memória RAM | 4096 MB |
| Processadores | 2 vCPUs |
| Disco | 50 GB |
| Rede | NAT |

---

## Etapas de Instalação

1. Download do VirtualBox em virtualbox.org
2. Download do Windows Server 2022 Evaluation em microsoft.com/evalcenter
3. Criação da máquina virtual com as especificações acima
4. Instalação do Windows Server 2022 Standard Evaluation Desktop Experience
5. Instalação do role Active Directory Domain Services via Server Manager
6. Promoção do servidor a Controlador de Domínio
7. Criação do domínio corptech.local

---

## Credenciais do Laboratório

| Conta | Usuário | Observação |
|-------|---------|------------|
| Administrador local | Administrator | Conta padrão do Windows Server |
| Domínio | CORPTECH\Administrator | Conta de administrador do domínio |

---

## Domínio criado

| Item | Valor |
|------|-------|
| Nome do domínio | corptech.local |
| NetBIOS | CORPTECH |
| Controlador de Domínio | WIN-2C7I5KSUOVG |
| Nível funcional | Windows Server 2016 |

---

## Evidência

Print 1 — Estrutura de OUs no Active Directory Users and Computers

**Analista:** Matheus Grun  
**Última atualização:** Agosto 2026
