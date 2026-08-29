# Cenário 14 — Site com Erro de Conexão Não Segura

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Categoria:** Certificado / Data e Hora  
**Nível:** N1

---

## Relato do usuário

*"Estou tentando acessar o sistema da empresa pelo navegador mas aparece um erro dizendo que a conexão não é segura e o site está bloqueado. Outros colegas conseguem acessar normalmente."*

---

## Diagnóstico

| Passo | Verificação | Resultado |
|-------|-------------|-----------|
| 1 | Verificado se colegas acessam | Colegas acessam — problema isolado no usuário |
| 2 | Verificado data e hora do computador | Data configurada para 2023 — incorreta |
| 3 | Corrigido para data atual | Configurações → Hora e Idioma → Hora automática |
| 4 | Testado o acesso ao site | Site abriu normalmente |
| 5 | Confirmado com usuário | Acesso ao sistema restaurado |

---

## Solução aplicada

Data e hora do computador estavam configuradas para 2023. Corrigido para data atual ativando a opção de hora automática. O navegador voltou a validar o certificado de segurança do site corretamente.

---

## Causa raiz

Data e hora incorretas no computador — o navegador não conseguiu validar o certificado de segurança do site pois a data estava fora do período de validade do certificado.

---

## Lição aprendida

Data e hora incorreta é uma das causas mais subestimadas em suporte. Causa erros de certificado, falhas de autenticação e problemas em sistemas. Sempre verificar antes de partir para causas mais complexas.

---

## Quando o problema seria diferente

| Situação | Causa |
|----------|-------|
| Só esse usuário com erro | Data/hora errada ou cache |
| Todos os usuários com erro | Certificado do site expirado — escalar N2 |
| Erro em site específico | URL incorreta ou antivírus bloqueando |

---

## Conceitos relacionados

- **Certificado de segurança** — valida a identidade de um site — falha quando a data do PC está incorreta
- **Cache do navegador** — dados temporários — limpar com Ctrl + Shift + Delete

---

## Procedimento relacionado

[Diagnóstico de Conectividade](../procedimentos/conectividade.md)
