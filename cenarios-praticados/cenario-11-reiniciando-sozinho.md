# Cenário 11 — Computador Reiniciando Sozinho

**Data:** Agosto 2026  
**Analista:** Matheus Grun  
**Categoria:** Hardware / Sistema  
**Nível:** N1/N2

---

## Relato do usuário

*"Meu computador está reiniciando sozinho várias vezes ao dia sem avisar. Não aparece nenhuma mensagem de erro — ele simplesmente desliga e liga novamente. Isso começou há dois dias."*

---

## Diagnóstico

| Passo | Verificação | Resultado |
|-------|-------------|-----------|
| 1 | Visualizador de Eventos — eventvwr | Logs de reinicialização identificados |
| 2 | Padrão das reinicializações | Ocorrem após 30 minutos de uso intenso |
| 3 | Temperatura do computador | Visivelmente quente ao toque |
| 4 | Histórico do Windows Update | Atualização recente — descartada como causa |
| 5 | Conclusão | Superaquecimento confirmado |

---

## Solução aplicada

Superaquecimento identificado como causa raiz. Verificadas saídas de ventilação — obstruídas. Orientado o usuário a não bloquear as grades de ventilação. Escalado para N2 para limpeza interna e verificação da ventoinha.

---

## Causa raiz

Superaquecimento — acúmulo de poeira nas saídas de ventilação impedindo a dissipação de calor do processador.

---

## Lição aprendida

Reinicialização após uso intenso com computador quente é quase sempre superaquecimento — não atualização do Windows. O Visualizador de Eventos — eventvwr — é fundamental para identificar o padrão das reinicializações antes de agir. Reinicializações aleatórias em qualquer momento indicam outras causas — driver ou hardware com defeito.

---

## Quando escalar para N2

- Limpeza interna — soprador de ar e remoção de poeira
- Troca de pasta térmica do processador
- Verificação da ventoinha
- Avaliação de substituição do equipamento

---

## Conceitos relacionados

- **Superaquecimento** — temperatura elevada causa desligamento automático como proteção do hardware
- **eventvwr** — Visualizador de Eventos — registra histórico de erros e eventos do sistema
- **Pasta térmica** — material entre processador e dissipador que facilita a troca de calor

---

## Procedimento relacionado

[Diagnóstico de Hardware](../procedimentos/hardware.md)
