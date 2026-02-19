---
created: 2026-02-10 10:42
updated: 2026-02-13 15:29
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Cache]]"
  - "[[]]"
  - "[[Session Management]]"
aliases:
  - Com Estado
---

## Definição
**Stateful** refere-se a um sistema, protocolo ou aplicação que mantém o registro das interações anteriores com um usuário ou cliente. O sistema "lembra" do estado atual e dos dados processados, utilizando essas informações para influenciar o processamento de requisições futuras.

## Funcionamento
-  **Conexão Inicial:** O cliente se conecta ao servidor.
- **Criação de Contexto:** O servidor aloca memória ou armazenamento para salvar os dados dessa sessão específica (variáveis, login, histórico).
- **Dependência:** As requisições subsequentes dependem da informação armazenada no servidor. Se o servidor reiniciar, os dados da sessão ativa podem ser perdidos, a menos que haja persistência em disco.
- **Encerramento:** O estado é mantido até que a sessão seja explicitamente fechada ou expire (timeout).

## Comparação
Stateful vs [[Stateless]]:

| Característica     | Stateful (Com Estado)                          | [[Stateless]] (Sem Estado)                           |
| :----------------- | :--------------------------------------------- | :--------------------------------------------------- |
| **Memória**        | Servidor armazena dados da sessão.             | Servidor não guarda dados entre requisições.         |
| **Escalabilidade** | Mais complexa (precisa de "sticky sessions").  | Alta (qualquer servidor atende qualquer requisição). |
| **Exemplo**        | Carrinho de compras (em memória), FTP, Telnet. | API REST, DNS, HTTP (nativo).                        |
| **Falha**          | Perda de sessão se o servidor cair.            | Transparente, basta reenviar a requisição.           |
