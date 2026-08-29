# Cenário 10 — E-mail sem Conexão ao Servidor

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Categoria:** E-mail / Credenciais  
**Nível:** N1

---

## Relato do usuário

*"Meu e-mail parou de funcionar. Estou tentando enviar mensagens mas aparece um erro dizendo que não foi possível conectar ao servidor. Consigo acessar a internet normalmente."*

---

## Diagnóstico

| Passo | Verificação | Resultado |
|-------|-------------|-----------|
| 1 | Verificado se colegas têm o mesmo problema | Só esse usuário — problema local |
| 2 | Perguntado sobre mudanças recentes | Usuário trocou a senha no dia anterior |
| 3 | Identificada causa | Outlook usando senha antiga — credenciais desatualizadas |
| 4 | Atualizada senha no Outlook | Caixa de credenciais apareceu — nova senha digitada |
| 5 | Testado envio de e-mail | E-mail enviado com sucesso |

---

## Solução aplicada

Credenciais do Outlook estavam desatualizadas após troca de senha. Atualizada a senha diretamente na caixa de credenciais do Outlook. Caso a caixa não apareça automaticamente — acessar via Painel de Controle → Gerenciador de Credenciais → localizar o servidor de e-mail → editar e atualizar a senha.

---

## Causa raiz

Após troca de senha no sistema o cliente de e-mail continuou usando as credenciais antigas — causando falha na autenticação com o servidor.

---

## Lição aprendida

Sempre que o e-mail parar de funcionar após troca de senha — a causa é quase sempre credenciais desatualizadas no cliente. Não é necessário redefinir a senha novamente — apenas atualizar onde ela está armazenada.

---

## Conceitos relacionados

- **Gerenciador de Credenciais** — Painel de Controle → armazena senhas de sistemas e e-mails
- **Cliente de e-mail** — Outlook ou similar — precisa ser atualizado manualmente após troca de senha
- **Autenticação** — processo de validação de usuário e senha no servidor

---

## Procedimento relacionado

[Diagnóstico de Conectividade](../procedimentos/conectividade.md)
