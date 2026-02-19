---
created: 2026-02-08 19:49
updated: 2026-02-13 15:36
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Firebase]]"
  - "[[Supabase]]"
  - "[[API Economy]]"
aliases:
  - Backend as a Service
  - Backend como Serviço
---

## Definição
**BaaS (Backend as a Service)** é um [[Modelos de Serviço Cloud|Modelo de Serviço de Nuvem]] que automatiza o desenvolvimento do lado do servidor([[Back-end]]), fornecendo APIs e SDKs prontos para uso. Ele permite que desenvolvedores front-end e mobile conectem suas aplicações a serviços de infraestrutura sem escrever código de [[Back-end]] personalizado para tarefas comuns.
## Funcionamento
O **BaaS** atua como uma ponte entre o frontend da aplicação e os [[Recursos de Nuvem]]. Em vez de criar um servidor para autenticar usuários ou gerenciar um banco de dados, o desenvolvedor consome esses serviços via biblioteca (SDK) diretamente no cliente.

**Componentes Comuns em BaaS:**
- **Gerenciamento de Usuários:** Autenticação (OAuth, Email, Social Login).
- **Database Real-time:** Sincronização de dados instantânea.    
- **Push Notifications:** Envio de alertas para dispositivos móveis.
- **File Storage:** Armazenamento de imagens e documentos.

## Comparação

| **Característica**        | **BaaS (Backend as a Service)**                            | **[[FaaS]] (Function as a Service)**                            |
| ------------------------- | ---------------------------------------------------------- | --------------------------------------------------------------- |
| **Foco do Desenvolvedor** | Integração de serviços prontos ([[Out-of-the-box]]).       | Escrita de lógica customizada (Código puro).                    |
| **Customização**          | Limitada às funcionalidades oferecidas pelo provedor.      | Total liberdade para escrever qualquer lógica de negócio.       |
| **Uso Comum**             | Apps mobile, [[MVP\|MVPs]] rápidos e aplicações web ricas. | Processamento de dados, automação e integrações específicas.    |
| **Gerenciamento**         | O provedor cuida da arquitetura completa do backend.       | O desenvolvedor escreve a função, o provedor cuida da execução. |
