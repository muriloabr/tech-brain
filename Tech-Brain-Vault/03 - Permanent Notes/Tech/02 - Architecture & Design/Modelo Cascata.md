---
created: 2026-02-10 13:45
updated: 2026-02-13 16:53
type: concept
status: 🌳
area: Tech
tags:
sources: []
related:
  - "[[SDLC]]"
aliases:
  - Ciclo De Vida Clássico
  - Waterfall
  - Waterfall Model
---

## Definição
O **Modelo Cascata** (Waterfall) é uma abordagem linear e sequencial para o [[Desenvolvimento de Sistemas]] e [[Gestão de Projetos]].

É considerado o paradigma mais antigo da [[Engenharia de Software]], onde o progresso flui logicamente de uma fase para a próxima (como uma queda d'água). Neste modelo, uma etapa deve ser obrigatoriamente concluída e validada antes que a fase subsequente possa ser iniciada.

## Funcionamento
O funcionamento do modelo segue uma progressão rígida de etapas documentadas:
- **Requisitos**: Coleta extensiva de todas as necessidades do cliente. O escopo é definido integralmente antes de qualquer código ou execução.
- **Análise e Design**: Criação da arquitetura técnica, diagramas de dados e especificações de design baseadas nos requisitos aprovados.
- **Implementação**: A fase de construção ou codificação propriamente dita, onde o sistema é desenvolvido em unidades.
- **Testes**: Após a integração das partes, o sistema completo é testado para verificar se atende aos requisitos iniciais e se possui falhas.
- **Implantação**: O produto final é entregue ao cliente ou lançado no ambiente de produção.
- **Manutenção**: Fase de suporte contínuo para correção de erros e atualizações necessárias conforme o uso real.

## Comparação
Modelo Cascata vs [[Metodologias Ágeis]]

| Critério          | Modelo Cascata                                                 | [[Metodologias Ágeis]] (Ex: Scrum)                         |
| :---------------- | :------------------------------------------------------------- | :--------------------------------------------------------- |
| **Flexibilidade** | Baixa; mudanças no escopo são caras e difíceis após o início.  | Alta; abraça mudanças mesmo em estágios avançados.         |
| **Feedback**      | Ocorre principalmente no final do ciclo de desenvolvimento.    | Contínuo e constante em cada iteração (Sprint).            |
| **Documentação**  | Extensiva e rigorosa em cada fase do processo.                 | Focada no essencial e no software funcional.               |
| **Risco**         | Alto para projetos complexos devido à demora na entrega final. | Reduzido através de entregas incrementais frequentes.      |
| **Ideal para**    | Projetos com requisitos fixos, claros e sem ambiguidade.       | Projetos dinâmicos, inovadores ou com requisitos incertos. |
