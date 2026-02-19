---
created: 2026-02-10 11:49
updated: 2026-02-13 15:36
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Automation]]"
  - "[[Drivers]]"
  - "[[User Experience]]"
aliases:
  - Ligar e Usar
  - PnP
---

## Definição
**Plug-and-Play** (PnP) é um padrão de tecnologia que permite conectar um dispositivo a um computador ou sistema e tê-lo funcionando imediatamente, sem a necessidade de configuração física complexa ou instalação manual de drivers pelo usuário.

## Funcionamento
- **Detecção:** Ao conectar o hardware, o sistema operacional identifica o ID do dispositivo.
- **Alocação:** O sistema aloca recursos (como endereços de I/O e IRQs) automaticamente, evitando conflitos com outros hardwares.
- **Instalação:** O SO busca em sua base de dados o driver apropriado e o carrega.
- **Prontidão:** O dispositivo fica disponível para uso em questão de segundos.

## Comparação
Plug-and-Play vs [[Configuração Manual]]

| Característica | Plug-and-Play            | Configuração Manual (Legado)              |
| :------------- | :----------------------- | :---------------------------------------- |
| **Instalação** | Automática.              | Exige jumpers físicos e discos de driver. |
| **Conflitos**  | Gerenciados pelo SO.     | Comuns (ex: conflito de IRQ).             |
| **Usuário**    | Leigo consegue instalar. | Exige conhecimento técnico.               |
| **Exemplo**    | USB, HDMI.               | Placas ISA antigas, Impressoras Serial.   |