# Procedimento — Diagnóstico de Impressoras

**Categoria:** Hardware / Periféricos  
**Nível:** N1  
**Tempo médio de resolução:** 10 a 20 minutos

---

## Sintomas comuns

- Impressora sumiu da lista de dispositivos
- Documentos presos na fila de impressão
- Impressora aparece com erro ou offline
- Impressão não sai mas não dá erro

---

## Fluxo de diagnóstico

1. Colegas do mesmo setor conseguem imprimir?
   - Não → problema na impressora ou na rede → escalar N2
   - Sim → problema local no computador do usuário → continuar

2. Verificar em Painel de Controle → Dispositivos e Impressoras
   - Impressora não aparece → reinstalar driver
   - Impressora aparece com erro → reiniciar Spooler

3. Reiniciar o serviço de Spooler
   - `net stop spooler`
   - `net start spooler`

4. Testar impressão
   - Funcionou → encerrar chamado
   - Não funcionou → reinstalar driver ou escalar N2

---

## Comandos utilizados

| Comando | Função |
|---------|--------|
| `net stop spooler` | Para o serviço de impressão |
| `net start spooler` | Inicia o serviço de impressão |

---

## Soluções mais comuns

**Impressora sumiu da lista**

1. Painel de Controle → Dispositivos e Impressoras
2. Verificar se a impressora aparece
3. Se não aparecer → Adicionar impressora → buscar na rede
4. Se aparecer com erro → reiniciar Spooler

**Documentos presos na fila**

1. `net stop spooler`
2. Navegar até `C:\Windows\System32\spool\PRINTERS`
3. Apagar todos os arquivos dentro da pasta
4. `net start spooler`

**Impressora offline**

1. Clicar com botão direito na impressora
2. Ver o que está sendo impresso
3. Desmarcar a opção Usar impressora offline

---

## Quando escalar para N2

- Nenhum usuário do setor consegue imprimir
- Reinstalação do driver não resolve
- Impressora com defeito físico

---

## Causa raiz mais comum

| Causa | Frequência |
|-------|-----------|
| Spooler corrompido ou travado | Alta |
| Driver desatualizado ou corrompido | Alta |
| Impressora offline na rede | Média |
| Fila de impressão travada | Média |
| Defeito físico na impressora | Baixa |

---

**Autor:** Matheus Grun  
**Última atualização:** Agosto 2026
