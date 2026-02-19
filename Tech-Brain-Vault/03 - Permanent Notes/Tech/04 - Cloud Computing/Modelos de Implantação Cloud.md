---
created: 2026-02-05 22:38
updated: 2026-02-06 22:05
type: concept
status: 🌿
area: Tech
tags:
sources: []
related: []
aliases:
  - Modelos de Implantação
  - Deployment Models
  - DM
---

## Definição
Os modelos de implantação definem **quem tem o controle** sobre a infraestrutura e onde os dados residem fisicamente.

### [[Nuvem Pública]] ([[Nuvem Pública|Public Cloud]])
Recursos de computação (como servidores e armazenamento) que pertencem a um provedor terceirizado e são operados por ele.
- **[[Multi-tenancy]]:** Você compartilha o mesmo hardware com outros "inquilinos", mas seus dados são isolados logicamente.    
- **Foco:** Baixo custo e escalabilidade rápida.
- **Vantagem:** Controle total, privacidade máxima e conformidade com leis rígidas.    
- **Exemplo:** [[Microsoft Azure]], [[Amazon Web Services|AWS]], [[Google Cloud]].
### [[Nuvem Privada]] ([[Nuvem Privada|Private Cloud]])
Infraestrutura dedicada exclusivamente a uma única empresa ou organização.
- **Diferencial:** Pode estar fisicamente no seu datacenter local (**[[Infraestrutura Tradicional|On-Premises]]**) ou hospedada em um provedor externo em hardware dedicado (**[[Single-tenant]]**).    
- **Foco:** Segurança máxima, controle total e conformidade estrita.
- **Vantagem:** Controle total, privacidade máxima e conformidade com leis rígidas.
- **Exemplo:** Um banco operando seu próprio mainframe ou usando o _Azure Stack_ localmente.
### [[Nuvem Híbrida]] ([[Nuvem Híbrida|Hybrid Cloud]])
Um ambiente que utiliza uma mistura de nuvens públicas e privadas.
- **Conectividade:** Permite que dados e aplicações sejam compartilhados entre os dois ambientes via conexões seguras ([[VPN]] ou [[ExpressRoute]]).    
- **Caso de Uso:** Manter dados sensíveis na privada e usar a pública para processamento pesado em picos de demanda (**[[Cloud Bursting]]**).
### [[Multi-Cloud]]
A estratégia de utilizar **dois ou mais provedores de nuvem pública** diferentes (ex: AWS para processamento e Azure para Active Directory).
- **Objetivo:** Evitar o **[[Vendor Lock-in]]** (dependência de um único fornecedor) e aumentar a resiliência (se um provedor cair, o outro assume).    

### [[Nuvem Comunitária | Community Cloud]]
Uma infraestrutura compartilhada por diversas organizações que possuem interesses em comum (como requisitos de segurança, missão ou conformidade legal).
- **Exemplo:** Várias universidades compartilhando uma nuvem para pesquisa, ou órgãos do governo federal dividindo uma infraestrutura segura.
## Funcionamento

| **Modelo**      | **Usuários**     | **Hardware**      | **Controle**  | **Modelo Econômico** |
| --------------- | ---------------- | ----------------- | ------------- | -------------------- |
| **Pública**     | Vários (Público) | Provedor          | Mínimo        | **[[OpEx]]**         |
| **Privada**     | Único (Privado)  | Próprio/Dedicado  | Máximo        | **[[CapEx]]**        |
| **Híbrida**     | Misto            | Misto             | Médio         | Misto                |
| **Multi-Cloud** | Misto (Públicas) | Vários Provedores | Médio         | **[[OpEx]]**         |
| **Comunitária** | Grupo Específico | Compartilhado     | Compartilhado | Misto                |

## Comparação
> [!TIP] Multi-Cloud vs Hybrid Cloud > Não confunda!
> * **Híbrida:** Mistura Pública + Privada. 
> * **Multi-Cloud:** Mistura Pública + Pública 
> 	* (Ex: Usar Azure para o Banco de Dados e AWS para os Servidores).

#### Esses termos definem o modelo econômico de cada nuvem:
> [!NOTE] CapEx (Capital Expenditure) 
> >*  **Despesas de Capital.** É o gasto inicial em infraestrutura física. Você paga "na frente" antes de usar. 
> > * **Típico de: Nuvem Privada** (Comprar servidores, ar condicionado, cabos). > * *Contabilidade:* O valor do ativo deprecia ao longo do tempo. 

> [!NOTE] OpEx (Operational Expenditure)
> >* **Despesas Operacionais.** É o gasto recorrente pelo uso de um serviço ou produto. Você paga "conforme usa" (mensal/anual). 
> >* **Típico de: Nuvem Pública** (Fatura do Azure/AWS no fim do mês). > * *Contabilidade:* Dedutível de impostos no mesmo ano.