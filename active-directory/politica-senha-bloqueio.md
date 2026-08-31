# Política de Senha e Bloqueio de Conta — Active Directory

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Domínio:** corptech.local

---

## Objetivo

Configurar a política de senha e de bloqueio de conta no domínio corptech.local, validar sua aplicação via linha de comando e testar o bloqueio automático em ambiente controlado — replicando o procedimento adotado em ambientes corporativos reais.

---

## Onde a política é configurada

A política de senha de domínio só tem efeito quando aplicada na **Default Domain Policy**, vinculada à raiz do domínio. Uma GPO criada e vinculada a uma OU não afeta a política de senha das contas de domínio.

Caminho: Group Policy Management → corptech.local → Default Domain Policy → Edit → Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies

---

## Password Policy — antes e depois

| Política | Padrão | Configurado |
|----------|--------|-------------|
| Enforce password history | 24 senhas | 24 senhas |
| Maximum password age | 42 dias | 90 dias |
| Minimum password age | 1 dia | 1 dia |
| Minimum password length | 7 caracteres | 10 caracteres |
| Password must meet complexity requirements | Enabled | Enabled |
| Store passwords using reversible encryption | Disabled | Disabled |

**Justificativa das alterações**

O padrão de 42 dias é considerado agressivo e induz o usuário a criar senhas sequenciais previsíveis. O intervalo de 90 dias, combinado com o aumento do tamanho mínimo para 10 caracteres, oferece proteção maior contra força bruta com menor impacto operacional.

---

## Account Lockout Policy — antes e depois

| Política | Padrão | Configurado |
|----------|--------|-------------|
| Account lockout threshold | 0 tentativas | 5 tentativas |
| Account lockout duration | Not Defined | 15 minutos |
| Reset account lockout counter after | Not Defined | 15 minutos |

**Observação sobre o padrão**

Threshold igual a 0 significa que a conta nunca bloqueia, independentemente do número de tentativas inválidas. É o padrão do Windows Server e representa exposição a ataques de força bruta.

**Diferença entre os parâmetros**

| Parâmetro | Função |
|-----------|--------|
| Account lockout duration | Tempo que a conta permanece bloqueada antes do desbloqueio automático |
| Reset account lockout counter after | Tempo até a contagem de tentativas inválidas voltar a zero |

Duração igual a 0 mantém a conta bloqueada indefinidamente, exigindo intervenção manual do administrador.

---

## Validação da política

Após configurar, a política foi forçada e verificada por linha de comando:

| Comando | Função |
|---------|--------|
| gpupdate /force | Força a aplicação imediata das políticas de grupo |
| net accounts /domain | Exibe a política vigente lida diretamente do controlador de domínio |

**Retorno obtido**

| Item | Valor |
|------|-------|
| Minimum password age (days) | 1 |
| Maximum password age (days) | 90 |
| Minimum password length | 10 |
| Length of password history maintained | 24 |
| Lockout threshold | 5 |
| Lockout duration (minutes) | 15 |
| Lockout observation window (minutes) | 15 |
| Computer role | PRIMARY |

O comando net accounts /domain confirma o estado real aplicado no domínio, e não apenas o que foi preenchido na interface gráfica.

---

## Teste de bloqueio

Teste realizado com a conta carlos.eduardo, utilizando tentativas de autenticação com senha incorreta.

Comando utilizado: runas /user:corptech\carlos.eduardo cmd

**Resultado observado**

| Tentativa | Código | Mensagem |
|-----------|--------|----------|
| 1 a 5 | 1326 | The user name or password is incorrect |
| 6 | 1909 | The referenced account is currently locked out and may not be logged on to |

A conta é bloqueada após a quinta tentativa inválida, mas a mensagem de bloqueio aparece apenas na tentativa seguinte, quando o sistema verifica o estado da conta antes de validar a senha.

---

## Códigos de erro — referência para atendimento

| Código | Significado | Ação do analista |
|--------|-------------|------------------|
| 1326 | Credencial incorreta, conta ativa | Orientar o usuário ou redefinir a senha |
| 1909 | Conta bloqueada pela política | Desbloquear a conta ou aguardar o tempo de duração |

Identificar o código evita a redefinição desnecessária de senha em casos que exigem apenas desbloqueio.

---

## Procedimento de desbloqueio

**Via interface gráfica**

1. Active Directory Users and Computers
2. Localizar o usuário na OU correspondente
3. Botão direito → Properties → aba Account
4. Marcar Unlock account
5. Apply e OK

**Via PowerShell**

Unlock-ADAccount -Identity carlos.eduardo

---

## Ajuste de conformidade identificado

Durante a validação foi identificado que as três contas do laboratório estavam com a opção **Password never expires** habilitada, o que isenta o usuário da política de expiração definida no domínio.

A configuração individual da conta prevalece sobre a política de domínio. A opção foi desmarcada nas contas carlos.eduardo, ana.lima e paula.santos, alinhando o ambiente à política estabelecida.

Esse tipo de divergência é comum em ambientes reais e costuma ser identificado apenas em auditorias de conformidade.

---

## Relação com o atendimento N1

Este procedimento é a causa raiz do caso INC-008 — conta bloqueada no sistema. A configuração da Account Lockout Policy determina quando a conta bloqueia, por quanto tempo permanece bloqueada e se o desbloqueio ocorre de forma automática ou manual.

---

## Evidências

Print 5 — Password Policy configurada  
Print 6 — Account Lockout Policy configurada  
Print 7 — Teste de bloqueio com códigos 1326 e 1909  
Print 8 — Propriedades da conta após ajuste de conformidade

---

**Analista:** Matheus Grun  
**Última atualização:** Agosto 2026
