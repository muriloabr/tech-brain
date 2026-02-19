---
created: 2026-02-03 12:54
updated: 2026-02-13 16:33
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Infraestrutura de TI]]"
  - "[[Engenharia de Software]]"
aliases:
  - Computação em Nuvem
  - Cloud
  - Cloud-Computing
---

## Definição
**Cloud Computing** é um modelo de entrega de **recursos computacionais pela internet** sob demanda através da internet, com pagamento conforme o uso, como:
- servidores (computação).
- armazenamento.
- bancos de dados.
- redes.
- softwares.
- inteligência artificial.
- segurança.
- ferramentas de desenvolvimento.

Em vez de comprar e manter hardware físico, você **usa recursos da nuvem sob demanda**, pagando apenas pelo que consome, sendo estas suas principais características:
- [[On-Demand Self-Service]]:
	- Você mesmo cria recursos quando quiser — sem pedir para TI ou fornecedor.
- **Acesso amplo pela rede**:
	- Acessível de qualquer lugar, por internet.
- [[Elasticidade em Nuvem|Elasticidade]]:
	- Aumenta ou reduz capacidade automaticamente conforme sua necessidade.
- [[Escalabilidade em Nuvem|Escalabilidade]]:
	- Consegue suportar projetos desde pequenos sites até aplicações globais escalando tanto em vertical quanto horizontal.
- [[Pay-as-you-go|Medição e cobrança por uso]]:
	- Você paga só pelo que utiliza ([[Pay-as-you-go]]).
- **Gerenciamento pelo provedor**:
	- Atualizações, segurança física e manutenção são responsabilidade do provedor.

### Pilares de Estruturação de Nuvem
Para entender a nuvem, é preciso distinguir como ela é **entregue** (serviço) e onde ela é **hospedada** (implantação).
#### [[Modelos de Serviço Cloud|Modelos de Serviço]] - O que é entregue
Define o nível de controle e a "camada" da pilha tecnológica que você está contratando:
- [[IaaS]] (Infraestrutura):
	- Aluguel de servidores e redes.
	- Você gere o SO.
- [[PaaS]] (Plataforma): 
	- Foco no desenvolvimento.
	- O provedor gere o SO e o runtime.
- [[SaaS]] (Software):
	- Produto pronto para uso final (ex: Gmail, Office 365).
- [[Serverless Computing|Serverless]]: 
	- Abstração total; você paga apenas pela execução do código.

#### [[Modelos de Implantação Cloud|Modelos de Implantação]] - Onde está hospedado
Define o ambiente e o isolamento dos seus dados:
- **[[Nuvem Pública]]**: Recursos compartilhados entre vários clientes (multitenancy). Ótimo custo-benefício.    
- **[[Nuvem Privada]]**: Recursos dedicados a uma única organização. Maior controle e segurança.    
- **[[Nuvem Híbrida]]: Combina pública e privada, permitindo que dados e apps transitem entre elas. 
- **[[Multi-Cloud]]**: Uso de dois ou mais provedores de nuvem pública (ex: AWS + Azure) para evitar dependência única.    
- **[[Nuvem Comunitária | Community Cloud]]**: Compartilhada por organizações com missões ou requisitos comuns.

### Segurança e Responsabilidade
A segurança é regida pelo **[[Modelo de Responsabilidade Compartilhada]]**:
- **Provedor ([[Security of the Cloud]]):** Cuida da segurança física, hardware e rede global.    
- **Cliente ([[Security in the Cloud]]):** Cuida dos dados, identidades (IAM), configurações e criptografia.

Descrevendo a "Escada de Responsabilidade":
- **Tendo exclusivamente uma infra [[Infraestrutura Tradicional|On-Premises]] (Local):** 
	- Você é responsável por tudo, do cabo de rede aos dados.
- **Trabalhando com [[IaaS]] (Ex: VMs):**
	- O provedor cuida do Hardware. Você cuida do Sistema Operacional (patching), Aplicações e Dados.
- **Trabalhando com [[PaaS]] (Ex: SQL DB):**
	- O provedor cuida do Hardware e do Sistema Operacional. Você cuida das Aplicações e Dados.
- **Consumindo [[SaaS]] (Ex: Office 365):**
	- O provedor cuida de quase tudo. Você foca apenas na **Identidade** (quem acessa) e nos **Dados**.

### Modelo de Gastos e Economia
A nuvem promove a transição de **[[CapEx]] vs [[OpEx]]**:
- **Sem [[CapEx]]:**
	- Você não gasta fortunas comprando servidores antes de começar o projeto.    
- **Puro [[OpEx]]:**
	- Gastos operacionais variáveis conforme o uso.    
- **[[Economia de Escala]]**:
	- Como os provedores compram bilhões em hardware, o custo unitário cai, e esse desconto é repassado ao cliente.

### Diferenciais Técnicos
Conceitos fundamentais que diferenciam a nuvem de um servidor local simples:
- **[[Alta Disponibilidade]] (HA):** O sistema permanece online mesmo com falhas de componentes.    
- **[[Tolerância a Falhas]] (FT):** Redundância total que evita qualquer interrupção.    
- **[[Recuperação de Desastres]] (DR):** Plano para restaurar tudo após uma falha catastrófica.    
- **Agilidade:** Capacidade de testar e lançar recursos em minutos, não semanas.

### Desafios
- **[[Vendor Lock-in]]**: O risco de ficar "preso" a um fornecedor devido a tecnologias proprietárias.
- **[[FinOps]]**: A necessidade de gerir custos rigorosamente para evitar surpresas na fatura.
- **Latência**: A dependência da conexão de rede para performance.

## Funcionamento
Ao adotar a Cloud Computing, uma organização precisa tomar duas decisões estratégicas:
- Primeira, deve escolher um dos **[[Modelos de Implantação Cloud|Modelos de Implantação]]**, escolhendo assim o ambiente (Público, Privado ou Híbrido) com base em requisitos de segurança e conformidade.
- Segunda, deve definir também os **[[Modelos de Serviço Cloud|Modelos de Serviço]]**, definindo se a equipe gerenciará a infraestrutura ([[IaaS]]), focará apenas no código ([[PaaS]]) ou consumirá software pronto ([[SaaS]]).

Serviços mais usados na nuvem:
- **Computação**
	- [[Máquina Virtual|VMs]], [[Container]], [[Kubernetes]], [[Serverless]] ([[Função FaaS]]).
- **Armazenamento**
	- Blobs, objetos, arquivos, discos, backups.
- **Rede**
	- [[VNet]], [[VPN]], [[CDN]], [[Load Balancer]].
- **Banco de Dados**
	- [[SQL]], [[NoSQL]], [[PostgreSQL]] gerenciado
- **IA e Machine Learning**
	- [[Vision]], [[NLP]], Modelos pré-treinados
- **DevOps**
	- [[Pipelines CI-CD|Pipelines CI/CD]], automações
- **Segurança**
	- Identity and Access (IAM)
    - Firewalls, [[WAF]]
    - Key Vault

## Comparação
### Vantagens sobre a [[Infraestrutura Tradicional]]
- Economia (custo variável, sem investimento inicial)
- Disponibilidade global
- Alta confiabilidade e redundância
- Desempenho superior
- Segurança de nível corporativo
- Redução de trabalho operacional
- Rapidez para lançar produtos


### Principais Provedores
- **[[Microsoft Azure]]**
- [[Amazon Web Services]]
- [[Google Cloud Platform]]    
- [[Google Cloud Platform]]
- [[Oracle Cloud]]    
- [[IBM Cloud]]    
- [[Alibaba Cloud]]