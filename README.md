# 📘 Protocolo Técnico para Adoção de LLMs no Ciclo de Desenvolvimento de Software

## 🧭 Finalidade

Este protocolo define diretrizes estruturadas e métricas de avaliação para adoção de modelos de linguagem (LLMs) em atividades ao longo do ciclo de desenvolvimento de software. Ele visa apoiar equipes técnicas e estratégicas na tomada de decisões fundamentadas quanto ao uso de IA generativa, com foco em:

- Produtividade
- Qualidade técnica dos artefatos
- Rastreabilidade e adaptabilidade do processo

## 🧱 Estrutura Metodológica

A organização do protocolo segue três níveis complementares:

1. **Framework** – Fases do processo de desenvolvimento (Ideate, Develop, Release & Operate)
2. **Processo** – Práticas contínuas de engenharia de software e DevOps
3. **AI-Enabled Activities** – Atividades assistidas por IA ao longo das fases

![img.png](img.png)


## 🧩 Contexto de Aplicação

Este protocolo é aplicado em um cenário real de transformação digital em um grande banco brasileiro, com foco na área de investimentos. A principal motivação é a complexidade da manutenção de regras tributárias codificadas em sistemas legados (mainframe), frequentemente impactadas por alterações regulatórias.


## 🎯 Objetivos Estratégicos

- **Automatizar e agilizar a produção de artefatos** ao longo do ciclo de desenvolvimento
- **Rastrear e medir o impacto da IA** na evolução de sistemas reais


## 🧰 Aplicações Práticas por Etapa

| Fase / Etapa                                                  | Atividades Principais                                                        | Aplicações de LLMs                                                                                                 |
|---------------------------------------------------------------|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [🧠 Ideation](docs/process/1-concept/a-ideation/protocolo.md) | Benchmarking, entrevistas, contexto inicial                                  | - Extração automatizada de tendências <br> - Roteiros de entrevistas por categoria <br> - Documento de contexto assistido por IA |
| [📋 Plan](docs/process/1-concept/b-plan/protocolo.md)              | Escopo, cronograma, riscos, plano de MVP                                     | - Geração automatizada de planos <br> - Alocação de recursos com base em padrões <br> - Sugestão de riscos e mitigações         |
| [🔎 Analysis](docs/process/1-concept/c-analysis/protocolo.md)  | Requisitos, regras de negócio, backlog                                       | - Extração de requisitos de documentos e código legado <br> - Geração de user stories e critérios de aceitação              |
| [🏗️ Design](docs/process/2-development/a-design/protocolo.md)   | Arquitetura, modelagem, APIs, protótipos                                     | - Geração de diagramas C4 <br> - Modelagem ER (MER/DER) <br> - Análise de atributos de qualidade <br> - Geração de contratos de API |


## 🗂️ Organização da Documentação

A documentação do protocolo está organizada por fase e artefato, no seguinte padrão:

## 📂 Estrutura da Documentação

A estrutura dos diretórios reflete as fases e artefatos do processo:

```
docs/
└── process/
    ├── 1-concept/
    │   ├── ideation/
    │   ├── plan/
    │   └── analysis/
    └── 2-development/
        └── design/
```

Cada subdiretório contém:

- Artefatos gerados com apoio de LLMs
- Prompts utilizados para geração assistida
- Templates reutilizáveis


## 🧪 Extensibilidade e Pesquisa

Este protocolo está embasado em pesquisa científica e pode ser estendido para avaliação longitudinal de impacto dos LLMs em:

- **Modularidade e acoplamento**
- **Produtividade de times técnicos**
- **Qualidade de requisitos e arquitetura**
- **Evolução de sistemas e ciclos de manutenção**

Aplicações futuras incluem análises comparativas (com vs. sem LLM), avaliações heurísticas e estudos de caso longitudinais.


## 📎 Recursos de Apoio

- 🔗 [Projeto SPReaD](https://aserg.org/project/spread/)
- 🔗 [Artigo: SPReaD – Service-Oriented Process for Reengineering and DevOps](https://link.springer.com/article/10.1007/s11761-021-00329-x)
- 📂 Documentação detalhada por fase: `docs/process/`
- 💬 Base de prompts estruturados e templates de automação com IA

---

## 👨‍🔬 Autor e Contribuição

Desenvolvido por **Yan Justino**, especialista em engenharia de software e doutorando na área de granularidade de microsserviços. Este protocolo integra pesquisa aplicada com evidências reais da indústria bancária brasileira.

Contribuições, experimentações e adaptações são bem-vindas para evolução contínua deste protocolo.

