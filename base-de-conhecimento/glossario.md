# Glossário Técnico — Suporte N1/N2

Definições dos principais termos técnicos utilizados no dia a dia do suporte técnico.

---

## A

**APIPA (Automatic Private IP Addressing)**
IP atribuído automaticamente pelo Windows quando o servidor DHCP não é encontrado. Faixa: 169.254.x.x. Indica que o computador está isolado da rede.

**Active Directory (AD)**
Sistema da Microsoft usado por empresas para gerenciar usuários, senhas, permissões e computadores da rede. Uma das ferramentas mais utilizadas em ambientes corporativos.

---

## B

**BSOD (Blue Screen of Death)**
Tela Azul da Morte. Erro crítico do Windows que exibe um código de falha e reinicia o sistema. Causas comuns: driver corrompido, problema na RAM, disco defeituoso ou superaquecimento.

**Backup**
Cópia de segurança dos dados. Fundamental para recuperação em caso de falha ou perda de informações.

---

## C

**Cache DNS**
Histórico local de sites visitados guardado pelo Windows. Pode ficar desatualizado e causar falhas de acesso. Limpado com o comando `ipconfig /flushdns`.

---

## D

**DHCP (Dynamic Host Configuration Protocol)**
Serviço que distribui endereços IP automaticamente para os dispositivos da rede. Quando falha — computadores recebem IP 169.254.x.x e ficam sem acesso à rede.

**DNS (Domain Name System)**
Traduz nomes de sites como google.com em endereços IP. Quando falha — sites não abrem mas sistemas internos e aplicativos continuam funcionando.

**Driver**
Software que permite o sistema operacional se comunicar com um hardware. Quando corrompido ou desatualizado pode causar falhas em dispositivos como impressoras e placas de vídeo.

---

## E

**Escalonamento**
Processo de transferir um chamado para um nível superior de suporte — N2 ou N3 — quando o N1 não consegue resolver. Prática fundamental do ITIL.

---

## F

**Fonte de alimentação**
Componente responsável por converter a energia da tomada em energia utilizável pelo computador. Quando queima — o computador não liga. Principal componente afetado por quedas de energia.

---

## G

**Gateway**
Endereço do roteador. Todo tráfego que sai da rede local passa por ele. Se não responder — ninguém acessa a internet mesmo com IP válido.

**GPO (Group Policy Object)**
Política de grupo aplicada pelo Active Directory. Define configurações de segurança, restrições e comportamentos para usuários e computadores da rede.

---

## I

**IP (Internet Protocol)**
Endereço único de cada dispositivo na rede. Funciona como o CEP de uma casa — sem ele o computador não existe na rede.

**IP Privado**
Endereço usado dentro da rede local. Faixas mais comuns: 192.168.x.x, 10.0.x.x e 172.16.x.x. Não sai para a internet.

**IP Público**
Endereço único no mundo inteiro. É o endereço da empresa ou residência na internet.

**ITIL (Information Technology Infrastructure Library)**
Framework de boas práticas para Gestão de Serviços de TI. Define processos como Gestão de Incidentes, Gestão de Problemas, Gestão de Mudanças e Gestão de SLA.

---

## M

**Máscara de sub-rede**
Define quantos dispositivos podem existir na rede. O valor 255.255.255.0 é o mais comum e permite até 254 dispositivos na mesma rede.

---

## N

**Nobreak / UPS**
Dispositivo que fornece energia elétrica ao computador em caso de queda de luz. Após quedas intensas pode desarmar e precisar ser religado manualmente.

---

## S

**SLA (Service Level Agreement)**
Acordo de Nível de Serviço. Define o tempo máximo para atendimento e resolução de chamados conforme a prioridade. Fundamental no ITIL.

**Spooler de impressão**
Serviço do Windows que gerencia filas de impressão. Quando
