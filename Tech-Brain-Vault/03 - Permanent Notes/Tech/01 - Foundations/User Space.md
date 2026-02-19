---
created: 2026-02-13 16:14
updated: 2026-02-13 16:14
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Virtual Memory]]"
aliases:
  - User Mode
  - Espaço do Usuário
  - Ring 3
---

## Definição
**User Space** é a partição de memória segregada e protegida onde as aplicações de usuário, bibliotecas e serviços não essenciais são executados.

É um ambiente de "[[Sandbox]]" lógico projetado para impedir que softwares mal escritos ou maliciosos acessem diretamente o hardware ou interfiram na estabilidade do núcleo do sistema operacional.

## Funcionamento
Nesta camada, o código é executado em **Modo Usuário** (Ring 3), onde um subconjunto restrito de instruções da CPU é permitido.

O mecanismo de interação funciona da seguinte forma:
1.  **Isolamento:** Cada processo no **User Space** possui seu próprio espaço de endereçamento virtual. Ele "pensa" que possui a memória inteira, mas o [[Kernel]] mapeia isso para a RAM física.
2.  **Solicitação:** Quando uma aplicação precisa realizar uma operação privilegiada (ex: ler um arquivo, desenhar na tela, enviar pacote de rede), ela não pode fazer diretamente.
3.  **[[System Call]] (Syscall):** A aplicação invoca uma API do Kernel (geralmente via bibliotecas wrapper como `glibc`). Isso dispara uma interrupção de software, transferindo o controle para o [[Kernel]] (Ring 0), que valida a permissão, executa a tarefa e retorna o resultado para o User Space.

## Comparação
| Aspecto              | User Space (Modo Usuário)                                          | [[Kernel Space]] (Modo Supervisor)                              |
| :------------------- | :----------------------------------------------------------------- | :-------------------------------------------------------------- |
| **Acesso à Memória** | Restrito ao seu próprio espaço virtual.                            | Acesso total a toda a memória física e virtual.                 |
| **Interrupções**     | Pode ser interrompido (preemptivo) a qualquer momento pelo Kernel. | Pode desabilitar interrupções (em certas áreas críticas).       |
| **Falhas**           | Segregadas (Segmentation Fault mata apenas o processo).            | Catastróficas (Corrupção de memória ou falha total do sistema). |
| **Conteúdo Típico**  | Navegadores, Compiladores, Banco de Dados.                         | Gerenciamento de Processos, Drivers, Sistema de Arquivos.       |