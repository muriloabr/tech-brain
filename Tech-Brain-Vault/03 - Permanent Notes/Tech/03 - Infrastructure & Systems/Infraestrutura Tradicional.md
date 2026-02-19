---
created: 2026-02-06 17:33
updated: 2026-02-13 16:42
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Cloud Computing|Cloud-Computing]]"
aliases:
  - Data Center Local
  - On-Prem
  - On-Premises
  - On-Premise Infrastructure
  - On-Premise
---

## Definição
O **modelo tradicional** é chamado de **On-Premises**, ou seja, "dentro de casa". A organização **mantém** seu **próprio** data center. 

A empresa compra, instala, configura e mantém todo o hardware e software. Logo, ela mesma é responsável pela segurança física do prédio, refrigeração, substituição de discos rígidos queimados, atualizações do sistema operacional e proteção dos dados.

Os custos seguem o modelo [[CapEx]] (Despesas de Capital) - alto custo inicial de aquisição.

**Nem todo On-Premises é uma [[Nuvem Privada]]**, mas a maioria das Nuvens Privadas roda em **On-Premises**. É comum confundir os termos. 

> Se eu modernizar essa infraestrutura instalando softwares de virtualização avançada e automação (para que meus devs criem máquinas sozinhos), eu transformei meu **On-Premises** em uma **[[Nuvem Privada]]**.

### Cenários de Uso
Mesmo com a nuvem, o **On-Premises** não morreu. Ele é escolhido quando:
- **Soberania de Dados:** Leis exigem que os dados nunca saiam do país ou da empresa (Setor Bancário/Governo).    
- **Baixa Latência:** Aplicações fabris ou hospitalares onde milissegundos de atraso na internet são inaceitáveis.    
- **Custo Previsível:** Cargas de trabalho estáticas e massivas onde comprar o hardware sai mais barato a longo prazo do que alugar (Ex: Renderização 24/7).    
- **Legado:** Sistemas antigos (Mainframes) que não rodam em x86/Cloud.

## Funcionamento
Diferente da nuvem, onde apertamos um botão e surge um servidor, no [[Infraestrutura Tradicional|On-Premises]] (Infraestrutura Tradicional) a pilha de responsabilidade é física e complexa. O funcionamento depende de camadas que **eu** preciso gerenciar:
- **Instalações (Facility):** O prédio, controle de acesso físico, refrigeração (HVAC) e combate a incêndio.    
- **Energia:** Redundância elétrica, Nobreaks (UPS) e Geradores a diesel.    
- **Rede (Networking):** Cabos de fibra/cobre, Racks, Switches, Roteadores e Firewalls físicos.    
- **Hardware Computacional:** Servidores físicos (Blades/Racks), [[CPU]], Memória RAM e Storage (SAN/NAS).    
- **Virtualização:** O [[Hypervisor]] (VMware, Hyper-V) que eu preciso licenciar e instalar.    
- **Software:** Sistemas Operacionais, Bancos de Dados e Aplicações.    

> **Nota:** Se o ar-condicionado quebrar no domingo à noite, é problema meu. Isso é On-Premises.

O ciclo de vida opera sob a lógica de **provisionamento estático** e [[CapEx]] (Capital Expenditure):
1.  **Planejamento de Capacidade:** A TI deve estimar o pico máximo de uso para os próximos 3 a 5 anos e comprar hardware suficiente para suportá-lo, o que frequentemente gera ociosidade (over-provisioning).
2.  **Implantação:** Envolve a compra física, entrega, instalação em racks, cabeamento estruturado e configuração de sistemas de energia (UPS/Geradores) e refrigeração de precisão.
3.  **Manutenção:** A equipe interna é responsável por substituir discos rígidos falhos, atualizar firmwares, aplicar patches de segurança no SO base e monitorar a temperatura do ambiente.
4.  **Escalabilidade:** É predominantemente rígida e lenta. Escalar significa adquirir fisicamente novos servidores, o que pode levar semanas ou meses (Lead Time).

**No contexto moderno**, a infraestrutura tradicional raramente opera isolada; ela frequentemente atua como o alicerce de uma estratégia de [[Nuvem Híbrida]].
Neste cenário:
1.  **O On-Premises torna-se a [[Nuvem Privada]]:** Ele hospeda dados ultrassensíveis (compliance), sistemas legados (mainframes) ou aplicações que exigem latência zero com o chão de fábrica.
2.  **Conectividade:** Ele se conecta à [[Nuvem Pública]] via links dedicados (como [[Direct Connect]] ou [[ExpressRoute]]) ou [[VPNs]] seguras.
3.  **Orquestração:** Ferramentas modernas permitem que cargas de trabalho transbordem para a [[Nuvem Pública]] apenas quando a capacidade física local se esgota ([[Cloud Bursting]]).

## Comparação
Uma analogia para entender melhor é: comprada uma casa e ser responsável por construir, mobiliar e consertar qualquer vazamento.
