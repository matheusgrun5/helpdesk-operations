# GPO — Bloquear Painel de Controle

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Domínio:** corptech.local

---

## Objetivo

Criar uma GPO que bloqueia o acesso ao Painel de Controle e Configurações do PC para todos os usuários dos departamentos — política de segurança comum em ambientes corporativos para evitar alterações não autorizadas nas configurações do sistema.

---

## Informações da GPO

| Item | Valor |
|------|-------|
| Nome | Bloquear_Painel_de_Controle |
| Vinculada a | OU Departamentos |
| Status | Enabled |
| Enforced | No |
| Escopo | Todos os usuários das OUs TI, Financeiro e RH |

---

## Política configurada

| Configuração | Caminho | Status |
|-------------|---------|--------|
| Prohibit access to Control Panel and PC settings | User Configuration → Policies → Administrative Templates → Control Panel | Enabled |

---

## O que essa GPO faz

Quando aplicada impede que usuários acessem o Painel de Controle e as Configurações do PC. Remove o Painel de Controle de:

- Menu Iniciar
- File Explorer
- Resultados de pesquisa

Se o usuário tentar acessar aparece a mensagem:

Esta operação foi cancelada devido a restrições em vigor neste computador. Entre em contato com o administrador do sistema.

---

## Etapas de criação

1. Abrir Group Policy Management via Server Manager → Tools
2. Expandir corptech.local → Departamentos
3. Botão direito em Departamentos → Create a GPO in this domain and Link it here
4. Nome: Bloquear_Painel_de_Controle → OK
5. Botão direito na GPO → Edit
6. Navegar até User Configuration → Policies → Administrative Templates → Control Panel
7. Clicar duas vezes em Prohibit access to Control Panel and PC settings
8. Selecionar Enabled → Apply → OK

---

## Lição aprendida

GPOs são aplicadas a OUs — todos os usuários dentro da OU Departamentos e suas sub-OUs TI, Financeiro e RH são afetados automaticamente. Adicionar um novo usuário a qualquer um desses departamentos já aplica a política sem configuração adicional.

---

## Evidência

Print 4 — GPO Bloquear_Painel_de_Controle configurada no Group Policy Management Editor

---

**Analista:** Matheus Grun  
**Última atualização:** Agosto 2026
