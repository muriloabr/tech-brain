---
created: 2026-02-13 20:40
updated: 2026-02-18 01:19
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Memory Management]]"
aliases:
  - Coletor de Lixo
  - GC
  - Automatic Memory Management
  - Garbage Collection
---

## Definição
**Garbage Collector** (Coletor de Lixo) é um componente de execução presente em linguagens de alto nível ([[Java]], [[CSharp]], [[Python]], [[Go]]) responsável por gerenciar automaticamente a alocação e liberação de memória [[Heap Memory|Heap]]. Ele rastreia objetos que não são mais acessíveis pelo programa e recupera esse espaço para uso futuro, prevenindo a maioria dos vazamentos de memória manuais.

## Funcionamento
O algoritmo mais comum é o **Mark-and-Sweep**:
1.  **Mark (Marcar):** O GC percorre todos os objetos a partir das raízes (variáveis na Stack e globais) e marca tudo o que está "vivo" (conectado/acessível).
2.  **Sweep (Varrer):** Ele varre a memória Heap e deleta qualquer objeto que não foi marcado (ou seja, está "órfão" e inacessível).
3.  **Compact (Compactar - Opcional):** Reorganiza os objetos restantes para eliminar fragmentação.

## Comparação
| Aspecto | Gerenciamento Automático (GC) | Gerenciamento Manual (Malloc/Free) |
| :--- | :--- | :--- |
| **Facilidade** | Alta (o dev foca na lógica) | Baixa (o dev foca na memória) |
| **Performance** | Imprevisível (pausas para limpeza) | Previsível e otimizada |
| **Segurança** | Evita corrupção e ponteiros soltos | Propenso a erros humanos |
| **Exemplos** | Java, Python, JS | C, C++, Rust (Owner model) |