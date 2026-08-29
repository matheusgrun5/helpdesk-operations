# Cenário 12 — Sem Permissão para Instalar Software

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Categoria:** Segurança / GPO  
**Nível:** N1

---

## Relato do usuário

*"Estou tentando instalar um programa no meu computador mas aparece uma mensagem dizendo que não tenho permissão para instalar software. Preciso desse programa para trabalhar hoje."*

---

## Diagnóstico

| Passo | Verificação | Resultado |
|-------|-------------|-----------|
| 1 | Perguntado qual programa o usuário precisa | Identificado o software solicitado |
| 2 | Verificado se o software é homologado | Software aprovado pela empresa |
| 3 | Instalação com credenciais de administrador | Botão direito → Executar como administrador |
| 4 | Testado o funcionamento do programa | Software funcionando corretamente |
| 5 | Registrado no chamado | Software, versão e justificativa documentados |

---

## Solução aplicada

Software verificado e aprovado pela empresa. Instalação realizada com credenciais de administrador via botão direito → Executar como administrador. Programa instalado e funcionando corretamente.

---

## Causa raiz

Política de segurança via GPO — Group Policy Object — impede que usuários comuns instalem softwares sem permissão de administrador. Configuração padrão em ambientes corporativos para evitar instalação de softwares não autorizados e malwares.

---

## Lição aprendida

Nunca instalar software sem verificar se é autorizado pela empresa — mesmo que o usuário diga que é urgente. A urgência não substitui a política de segurança. Se o software não for homologado — orientar o usuário a abrir requisição formal e aguardar aprovação do gestor.

---

## Fluxo de decisão
