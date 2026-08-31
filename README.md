# HelpDesk Operations — Matheus Grun

Repositório de operações práticas de suporte técnico — documentando procedimentos, casos resolvidos, cenários praticados e laboratório de Active Directory.

O objetivo é simular o ambiente operacional de um analista de suporte N1/N2, documentando cada atividade como faria em um helpdesk corporativo real.

---

## Estrutura

### Procedimentos
Documentação técnica de resolução dos problemas mais comuns no suporte N1/N2.

| Procedimento | Categoria |
|-------------|-----------|
| [Diagnóstico de Conectividade](procedimentos/conectividade.md) | Redes |
| [Diagnóstico de Impressoras](procedimentos/impressoras.md) | Hardware |
| [Contas e Senhas](procedimentos/contas-e-senhas.md) | Acesso |
| [Diagnóstico de Hardware](procedimentos/hardware.md) | Hardware |

### Casos Resolvidos
Registro de chamados simulados com diagnóstico, solução e lição aprendida.

| Protocolo | Descrição | Status |
|-----------|-----------|--------|
| [INC-001](casos-resolvidos/INC-001.md) | Usuário sem acesso após o almoço | ✅ Resolvido |
| [INC-002](casos-resolvidos/INC-002.md) | Sites não abrem mas sistemas internos funcionam | ✅ Resolvido |
| [INC-003](casos-resolvidos/INC-003.md) | Impressora sumiu da lista | ✅ Resolvido |
| [INC-004](casos-resolvidos/INC-004.md) | Computador muito lento | ✅ Resolvido |
| [INC-005](casos-resolvidos/INC-005.md) | BSOD ao ligar o computador | 🔄 Monitorando |
| [INC-006](casos-resolvidos/INC-006.md) | Computador não liga | ✅ Resolvido |
| [INC-007](casos-resolvidos/INC-007.md) | Tela preta com computador ligado | ✅ Resolvido |
| [INC-008](casos-resolvidos/INC-008.md) | Conta bloqueada no sistema | ✅ Resolvido |

### Cenários Praticados
Registro de 15 cenários de suporte técnico praticados em laboratório.

| Cenário | Descrição | Categoria |
|---------|-----------|-----------|
| [Cenário 9](cenarios-praticados/cenario-09-pasta-compartilhada.md) | Pasta compartilhada sem permissão | Permissões / AD |
| [Cenário 10](cenarios-praticados/cenario-10-email-servidor.md) | E-mail sem conexão ao servidor | E-mail |
| [Cenário 11](cenarios-praticados/cenario-11-reiniciando-sozinho.md) | Computador reiniciando sozinho | Hardware |
| [Cenário 12](cenarios-praticados/cenario-12-instalar-software.md) | Sem permissão para instalar software | Segurança |
| [Cenário 13](cenarios-praticados/cenario-13-teclado-errado.md) | Teclado digitando caracteres errados | Configuração |
| [Cenário 14](cenarios-praticados/cenario-14-site-nao-seguro.md) | Site com erro de conexão não segura | Certificado |
| [Cenário 15](cenarios-praticados/cenario-15-monitor-amarelado.md) | Monitor com imagem amarelada | Hardware |

### Active Directory — Laboratório Prático
Laboratório montado com VirtualBox e Windows Server 2022 — criação de domínio, OUs, usuários, grupos e GPOs.

| Documento | Descrição |
|-----------|-----------|
| [Visão Geral](active-directory/README.md) | Estrutura e evidências do laboratório |
| [Configuração do Lab](active-directory/lab-setup.md) | Instalação e configuração do ambiente |
| [Usuários e Grupos](active-directory/usuarios-e-grupos.md) | Criação e gerenciamento de usuários |
| [GPO — Painel de Controle](active-directory/gpo-painel-controle.md) | Política de bloqueio do Painel de Controle |
| [Política de Senha e Bloqueio](active-directory/politica-senha-bloqueio.md) | Configuração e teste da política de senha e lockout |

### Base de Conhecimento
| Arquivo | Conteúdo |
|---------|---------|
| [Glossário Técnico](base-de-conhecimento/glossario.md) | Definições de termos técnicos |

---

## Ambiente de Operação

Os casos e cenários registrados aqui são operados dentro do **CorpTech Manager** — ambiente corporativo simulado desenvolvido como projeto de portfolio.

[Acessar o CorpTech Manager](https://matheusgrun5.github.io/corptech-manager/)

## Sobre mim

Estudante de Gestão em TI — focado em Suporte Técnico, Active Directory, ITSM e boas práticas ITIL. Construindo experiência real através de projetos práticos e documentação técnica.

[LinkedIn](https://www.linkedin.com/in/matheus-rafael-grun) | [GitHub](https://github.com/matheusgrun5)
