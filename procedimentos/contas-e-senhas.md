# Procedimento — Contas e Senhas

**Categoria:** Acesso e Identidade  
**Nível:** N1  
**Tempo médio de resolução:** 5 a 10 minutos

---

## Sintomas comuns

- Usuário não consegue fazer login
- Mensagem de conta bloqueada
- Senha expirada
- Usuário esqueceu a senha

---

## Fluxo de diagnóstico

1. Verificar causas simples primeiro
   - Caps Lock ativado?
   - Idioma do teclado correto?
   - Usuário está no sistema correto?

2. Verificar se a conta está bloqueada
   - Mensagem de bloqueio → desbloquear no Active Directory
   - Mensagem de senha expirada → forçar redefinição

3. Confirmar identidade do usuário antes de qualquer ação
   - Nome completo
   - Setor e ramal
   - E-mail corporativo

4. Acessar o Active Directory
   - Localizar o usuário
   - Desbloquear conta ou redefinir senha
   - Marcar opção de trocar senha no próximo logon se necessário

5. Confirmar acesso com o usuário
   - Funcionou → encerrar chamado
   - Não funcionou → verificar senha expirada ou escalar N2

---

## Soluções mais comuns

**Conta bloqueada**

1. Acessar Active Directory → Usuários e Computadores
2. Localizar o usuário
3. Clicar duas vezes → aba Conta
4. Desmarcar opção Conta bloqueada
5. Clicar em Aplicar

**Senha expirada**

1. Acessar Active Directory → Usuários e Computadores
2. Localizar o usuário
3. Clicar com botão direito → Redefinir senha
4. Marcar opção O usuário deve alterar a senha no próximo logon

**Usuário esqueceu a senha**

1. Confirmar identidade do usuário
2. Redefinir senha temporária no Active Directory
3. Orientar o usuário a trocar no primeiro acesso

---

## Boas práticas de segurança

- Sempre confirmar a identidade do usuário antes de redefinir senha
- Nunca informar a nova senha por e-mail sem criptografia
- Registrar no chamado quem solicitou e quem autorizou a redefinição
- Orientar o usuário a criar senha forte — mínimo 8 caracteres com letras, números e símbolos

---

## Quando escalar para N2

- Conta bloqueada mas sem tentativas erradas registradas — possível invasão
- Usuário não consegue acessar mesmo após desbloqueio
- Problema afeta múltiplos usuários simultaneamente

---

## Causa raiz mais comum

| Causa | Frequência |
|-------|-----------|
| Múltiplas tentativas com senha errada | Alta |
| Senha expirada por política | Alta |
| Caps Lock ativado | Alta |
| Idioma do teclado incorreto | Média |
| Possível tentativa de invasão | Baixa |

---

**Autor:** Matheus Grun  
**Última atualização:** Agosto 2026
