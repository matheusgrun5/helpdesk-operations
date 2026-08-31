# Procedimento — Diagnóstico de Conectividade

**Categoria:** Redes  
**Nível:** N1  
**Tempo médio de resolução:** 10 a 15 minutos

---

## Sintomas comuns

- Usuário sem acesso à internet
- Usuário sem acesso aos sistemas internos
- Sites não abrem mas aplicativos funcionam
- Conexão lenta ou instável

---

## Fluxo de diagnóstico

1. `ipconfig` → IP válido?
   - Não (169.254.x.x) → `ipconfig /release` + `ipconfig /renew`
   - Sim → continuar

2. `ping gateway` → rede local ok?
   - Não → verificar cabo ou switch
   - Sim → continuar

3. `ping 8.8.8.8` → internet ok?
   - Não → problema no provedor → escalar N2
   - Sim → continuar

4. `ping google.com` → DNS ok?
   - Não → `ipconfig /flushdns` ou trocar DNS
   - Sim → problema no navegador ou aplicativo

---

## Comandos utilizados

| Comando | Função |
|---------|--------|
| `ipconfig` | Verifica IP, máscara e gateway |
| `ipconfig /release` | Libera o IP atual |
| `ipconfig /renew` | Solicita novo IP ao DHCP |
| `ipconfig /flushdns` | Limpa o cache DNS |
| `ping 8.8.8.8` | Testa conexão com internet |
| `ping google.com` | Testa resolução DNS |
| `ping gateway` | Testa rede local |

---

## Soluções mais comuns

**IP inválido — 169.254.x.x**

Verificar se cabo está conectado. Se estiver ok rodar:
- `ipconfig /release`
- `ipconfig /renew`

**DNS com falha — sites não abrem**

- `ipconfig /flushdns`
- Se persistir — trocar DNS para `8.8.8.8` e `8.8.4.4`

---

## Quando escalar para N2

- IP continua inválido após /release e /renew
- ping 8.8.8.8 não responde — possível falha no provedor
- Problema afeta múltiplos usuários simultaneamente

---

## Causa raiz mais frequente

| Causa | Frequência | Indício no diagnóstico |
|-------|-----------|------------------------|
| Falha na obtenção de IP via DHCP | Alta | IP 169.254.x.x no ipconfig |
| Cache DNS corrompido | Alta | ping 8.8.8.8 responde, ping google.com falha |
| Cabo de rede desconectado ou danificado | Média | Media disconnected no ipconfig |
| Falha no navegador ou aplicativo | Média | Todos os pings respondem normalmente |
| Instabilidade do provedor | Baixa | ping 8.8.8.8 sem resposta |

A maior parte dos chamados de conectividade em N1 se resolve nas duas primeiras causas — renovação de IP e limpeza de cache DNS. Casos em que todos os testes de rede respondem indicam que o problema não está na conectividade, e sim na aplicação.

---

## Lição aprendida

O diagnóstico deve seguir a ordem do mais próximo ao mais distante: primeiro a máquina, depois a rede local, depois a internet e por último a resolução de nomes. Testar diretamente o site do usuário sem validar as camadas anteriores leva a conclusões erradas e a escalonamentos desnecessários.

---

**Analista:** Matheus Grun  
**Última atualização:** Agosto 2026
