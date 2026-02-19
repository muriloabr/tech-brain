---
created: 2026-02-13 10:49
updated: 2026-02-13 10:57
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Cloud Computing|Cloud-Computing]]"
  - "[[Kernel]]"
  - "[[Ring Protection]]"
  - "[[Emulação]]"
  - "[[03 - Permanent Notes/Tech/03 - Infrastructure & Systems/Virtualization]]"
  - "[[Hardware Abstraction]]"
  - "[[Infraestrutura de TI]]"
aliases:
  - VMM
  - Virual Machine Monitor
  - Monitor de Máquina Virtual
---

## Definição
O **Hypervisor**, ou **Monitor de Máquina Virtual (VMM)**, é a camada de software, firmware ou hardware responsável por criar, executar e gerenciar [[Máquina Virtual|Máquinas Virtuais]] (VMs).

Ele atua como um "policial de trânsito", abstraindo os recursos físicos do host (CPU, Memória, I/O) e distribuindo-os entre os diversos sistemas operacionais convidados (Guests), garantindo que um não interfira na execução do outro.

## Funcionamento
O **Hypervisor** intercepta as instruções enviadas pelo sistema operacional da [[Máquina Virtual|VM]] ao processador. Ele traduz ou repassa essas instruções para o hardware físico de forma controlada. Existem duas arquiteturas principais de funcionamento:
- **Type 1 (Bare Metal):** Instalado diretamente sobre o hardware, sem sistema operacional intermediário. É altamente performático e seguro, usado em data centers (Ex: ESXi, Hyper-V, Xen).
- **Type 2 (Hosted):** Roda como uma aplicação dentro de um sistema operacional convencional (Windows, Linux, macOS). Depende do OS hospedeiro para gerenciar o hardware, gerando maior latência (Ex: VirtualBox, VMware Workstation).

## Comparação
A distinção fundamental para arquitetura de infraestrutura é entre os tipos de implantação do Hypervisor.

| Critério | Type 1 (Bare Metal) | Type 2 (Hosted) |
| :--- | :--- | :--- |
| **Localização** | Diretamente no Hardware. | Sobre um Sistema Operacional (OS). |
| **Performance** | Alta (acesso quase direto). | Média (overhead do OS hospedeiro). |
| **Gerenciamento** | Via console remoto ou CLI. | Interface gráfica no OS desktop. |
| **Uso Ideal** | Servidores Enterprise, Cloud. | Desenvolvimento local, testes, estudos. |