---
created: 2026-02-06 16:52
updated: 2026-02-08 11:42
type: concept
status: 🌱
area: Tech
tags: []
sources: []
related: []
aliases:
  - Medição e cobrança por uso
  - PAYG
---

## Definição
**Pay-as-you-go** (PAYG) é um método de pagamento onde você paga apenas pelos recursos de computação que efetivamente utiliza.

É análogo a uma conta de luz ou água: não há uma taxa fixa alta inicial; o valor cobrado no final do mês é proporcional ao seu consumo.

### Características Principais
- **Sem Investimento Inicial ([[CapEx]]):** Você não precisa comprar servidores físicos ou hardware caro antecipadamente. **O custo é operacional** ([[OpEx]]).    
- Escalabilidade: Se o seu tráfego aumentar, você aloca mais recursos e paga mais. Se o tráfego cair, você reduz os recursos e a conta diminui imediatamente.
- **Medição por Unidade:** A cobrança pode ser feita por diversas métricas, como:    
    - Horas ou segundos de processamento (CPU).        
    - Quantidade de dados armazenados (GB).        
    - Volume de dados transferidos (Largura de banda).        
    - Número de requisições a uma API.

### Vantagens
- **Agilidade:** Permite testar ideias e descartá-las sem prejuízo de hardware.
- **Eficiência:** Elimina o desperdício de pagar por recursos ociosos.

### Desvantagens
- **Previsibilidade:** Se não houver monitoramento, a conta pode vir mais alta que o esperado.
- **Complexidade:** Gerenciar múltiplos serviços PAYG exige ferramentas de controle de custos.

## Funcionamento
Para quem está começando com [[Python]] ou estudos de [[Cloud Computing|Computação em Nuvem]], esse modelo é ideal para rodar scripts e pequenos projetos sem custo fixo, utilizando as "Camadas Gratuitas" ([[Free Tiers]]) oferecidas pelos provedores.

- **[[IaaS]] ([[Amazon Web Services|AWS]], [[Microsoft Azure|Azure]], [[Google Cloud Platform|Google Cloud]]):** Pagar por uma máquina virtual apenas pelas horas em que ela ficou ligada.    
- **[[SaaS]]:** Ferramentas de e-mail marketing que cobram por número de contatos ou envios.
- **[[Serverless Computing]]:** Pagar apenas pelos milissegundos em que um código (como uma função [[Python]]) é executado em resposta a um evento.

Basicamente use PAYG para testes e cargas imprevisíveis; use instâncias fixas para sistemas que nunca desligam.
## Comparação
O contraste entre a flexibilidade do PAYG e do Provisionamento Fixo:
- **Pay-as-you-go (Variável):** É ideal para demandas que mudam constantemente (ex: um site que recebe mais acessos durante o dia do que à noite). O risco é a variação no orçamento mensal, pois você paga pelo que consome.
- **Provisionamento Fixo / Instâncias Reservadas (Fixo):** Você se compromete com uma capacidade específica por um tempo determinado (ex: 1 ano). Em troca desse compromisso, o custo por hora é muito menor, mas você paga mesmo que não use o recurso.
