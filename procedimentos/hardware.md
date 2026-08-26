# Procedimento — Diagnóstico de Hardware

**Categoria:** Hardware  
**Nível:** N1/N2  
**Tempo médio de resolução:** 15 a 30 minutos

---

## Sintomas comuns

- Computador não liga
- Tela preta após ligar
- Computador muito lento
- BSOD — Tela Azul da Morte
- Monitor sem imagem

---

## Fluxo de diagnóstico

1. Computador não liga
   - Verificar cabo de energia na tomada e no computador
   - Testar a tomada com outro aparelho
   - Verificar estabilizador ou nobreak
   - Se tudo ok e não ligar → suspeita de fonte queimada → escalar N2

2. Tela preta — computador ligado
   - Verificar se monitor está ligado na energia
   - Verificar cabo de vídeo — HDMI ou VGA — nas duas pontas
   - Testar outras entradas do monitor
   - Testar com outro monitor
   - Se imagem aparecer com outro monitor → defeito no monitor original

3. Computador lento
   - Abrir Gerenciador de Tarefas — `Ctrl + Shift + Esc` ou `taskmgr`
   - Verificar CPU, RAM e Disco
   - Encerrar processo causador se possível
   - Reiniciar o computador
   - Se persistir → escalar N2

4. BSOD — Tela Azul da Morte
   - Anotar o código de erro exibido na tela
   - Abrir Visualizador de Eventos — `eventvwr`
   - Verificar logs no momento do erro
   - Documentar e manter chamado em aberto para monitoramento
   - Se ocorrer novamente → escalar N2

---

## Comandos utilizados

| Comando | Função |
|---------|--------|
| `taskmgr` | Abre o Gerenciador de Tarefas |
| `eventvwr` | Abre o Visualizador de Eventos |
| `Ctrl + Shift + Esc` | Atalho para o Gerenciador de Tarefas |

---

## Soluções mais comuns

**Computador não liga**

1. Verificar cabo de energia
2. Testar a tomada com outro aparelho
3. Verificar estabilizador — botão desarmado após queda de luz
4. Se nada resolver → fonte queimada → escalar N2

**Tela preta com computador ligado**

1. Verificar energia do monitor
2. Verificar cabo HDMI ou VGA
3. Testar outras entradas do monitor
4. Testar com outro monitor
5. Se imagem aparecer → substituição temporária do monitor
6. Registrar defeito e acionar processo de manutenção

**Computador lento**

1. Abrir Gerenciador de Tarefas
2. Verificar qual recurso está no limite — CPU, RAM ou Disco
3. Encerrar processo causador
4. Reiniciar se necessário
5. Se persistir → escalar N2

**BSOD**

1. Anotar código de erro
2. Abrir Visualizador de Eventos — `eventvwr`
3. Monitorar por recorrência
4. Se persistir → reinstalação do Windows — N2

---

## Solução de contorno

Quando o problema não pode ser resolvido imediatamente o N1 aplica uma **solução de contorno** para restaurar o trabalho do usuário enquanto o problema definitivo é tratado pelo N2.

Exemplos:
- Monitor com defeito → substituição temporária por outro monitor disponível
- Computador com defeito → remanejamento para outro equipamento disponível
- Fonte queimada → empréstimo de equipamento reserva

---

## Quando escalar para N2

- Fonte de alimentação queimada
- BSOD recorrente após monitoramento
- Problema de RAM ou disco com defeito
- Qualquer intervenção física no hardware

---

## Causa raiz mais comum

| Causa | Frequência |
|-------|-----------|
| Cabo de energia solto ou com defeito | Alta |
| Cabo de vídeo solto | Alta |
| Disco em 100% — Windows Update | Alta |
| Spooler ou processo travado | Média |
| Fonte de alimentação queimada | Média |
| BSOD por driver corrompido | Média |
| Defeito físico no hardware | Baixa |

---

**Autor:** Matheus Grun  
**Última atualização:** Agosto 2026
