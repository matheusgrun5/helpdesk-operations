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
```markdown
## Fluxo de diagnóstico

    1. ipconfig → IP válido?
       → Não (169.254.x.x): ipconfig /release + ipconfig /renew
       → Sim: continuar

    2. ping gateway → rede local ok?
       → Não: verificar cabo ou switch
       → Sim: continuar

    3. ping 8.8.8.8 → internet ok?
       → Não: problema no provedor → escalar N2
       → Sim: continuar

    4. ping google.com → DNS ok?
       → Não: ipconfig /flushdns ou trocar DNS
       → Sim: problema no navegador ou aplicativo
```
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

Verificar se cabo está conectado caso o comando falhe.

**DNS com falha — sites não abrem**

Se persistir — trocar DNS para `8.8.8.8` e `8.8.4.4` nas propriedades do adaptador de rede.

---

## Quando escalar para N2

- IP continua inválido após /release e /renew
- ping 8.8.8.8 não responde — possível falha no provedor
- Problema afeta múltiplos usuários simultaneamente

---

## Causa raiz mais comum

| Causa | Frequência |
|-------|-----------|
| Cabo desconectado | Alta |
| Falha no DHCP | Alta |
| Cache DNS corrompido | Alta |
| Falha no provedor | Média |
| Problema no switch | Baixa |

---

**Autor:** Matheus Grun  
**Última atualização:** Agosto 2026
