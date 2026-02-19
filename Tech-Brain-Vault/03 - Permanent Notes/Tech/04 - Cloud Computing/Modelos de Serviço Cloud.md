---
created: 2026-02-03 12:56
updated: 2026-02-13 15:24
type: concept
status: 🌿
area: Tech
tags:
sources: []
related: []
aliases:
  - Modelo de Serviço de Nuvem
  - Modelos de Serviços de Nuvem
  - Modelo de Serviço Cloud
  - Modelos de Serviços Cloud
---

## Definição
Modelos que definem quem gerencia o que na nuvem ([[Modelo de Responsabilidade Compartilhada|Responsabilidade Compartilhada]]).
* **[[IaaS]]:** Infraestrutura como Serviço (Hardware virtual).
* **[[PaaS]]:** Plataforma como Serviço (Ambiente de dev/deploy).
* **[[SaaS]]:** Software como Serviço (Produto final).
### [[IaaS]] (Infraestrutura)
- **O que é:** O provedor entrega o hardware virtualizado (CPU, RAM, Disco).
- **Sua responsabilidade:** Instalar o SO, atualizar patches de segurança, configurar firewall, instalar dependências, o provedor gerencia somente a infra.
- **Quando usar:** Quando você precisa de controle total sobre o ambiente ou rodar softwares legados que exigem configs específicas do SO.
### [[PaaS]] (Plataforma)
- **O que é:** O provedor entrega um ambiente pronto para rodar código.    
- **Sua responsabilidade:** Escrever o código e gerenciar o banco de dados. O SO e as atualizações de segurança dele são invisíveis de responsabilidade do provedor.
- **Quando usar:** Para focar puramente em desenvolvimento e deploy rápido, sem se preocupar com manutenção de servidores.
### [[SaaS]] (Software)
- **O que é:** O produto final pronto para uso via internet.
- **Sua responsabilidade:** Criar conta, configurar permissões e usar, o provedor gerencia todo o restante.
- **Quando usar:** Para ferramentas de produtividade, CRM, email, etc.

## Funcionamento
## Comparação
