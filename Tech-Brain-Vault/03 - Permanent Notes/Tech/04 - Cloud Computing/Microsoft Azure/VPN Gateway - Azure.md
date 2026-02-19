---
created: 2026-02-03 14:30
updated: 2026-02-13 15:38
type: concept
status: 🌱
area: Tech
tags:
sources: []
related:
  - Azure Virtual Machine
---

## Definição
Um tipo específico de gateway de rede virtual usado para enviar tráfego criptografado entre uma rede virtual do Azure e um local local (on-premise) pela Internet pública.

## Funcionamento
Ele cria um "túnel" seguro (VPN **Site-to-Site** ou **Point-to-Site**). Todo o tráfego que passa por ele é criptografado.
## Comparação
* **Diferente de ExpressRoute:** O VPN Gateway usa a internet pública (criptografada). O ExpressRoute usa uma conexão de fibra ótica privada e dedicada (mais rápido, mas mais caro).
