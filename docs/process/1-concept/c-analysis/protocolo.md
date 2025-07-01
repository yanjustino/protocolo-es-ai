# 📌 Protocolo de Adoção de LLMs – Fase: ANALYSIS
A etapa de análise é dedicada à compreensão profunda do problema, do domínio e das necessidades dos usuários, transformando essas informações em requisitos claros, priorizados e viáveis. Ela conecta diretamente a visão estratégica (ideação e planejamento) com a solução técnica que será modelada e construída.

## 🎯 Objetivo

Compreender profundamente o problema, o domínio e as necessidades dos usuários, transformando essas informações em requisitos funcionais e não funcionais claros, priorizados e viáveis. LLMs auxiliam na análise de bases de conhecimento, na elaboração de requisitos e na construção inicial do backlog do produto.

## 📘 Atividades e Interações com LLMs

| Atividade                              | Papel da LLM                                                                                     | Artefato(s)                                                                 | Avaliação Qualitativa                                                           | Avaliação Quantitativa                                |
|----------------------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------|
| Elaboração do Documento de Requisitos  | Auxílio na estruturação e detalhamento de requisitos com base em contexto e plano                 | Documento de Requisitos de Software (DRS) (`analysis-document.md`)          | Clareza, completude e coerência entre os requisitos                              | Nº de requisitos aceitos; tempo de geração             |
| Elaboração de backlog                  | Apoio à criação e refinamento de user stories com critérios de aceitação                          | Backlog de Produto (`analysis-backlog.md`)                                   | Clareza dos critérios de aceitação; cobertura do escopo                          | Nº de histórias geradas por tempo; % aprovadas         |


````mermaid
flowchart TD
    A[Elaboração do Documento de Requisitos]
    B[Elaboração de backlog]

    A --> B
````

## 📂 Artefatos Modelos

- [Documento de Requisitos de Software (DRS)](./artifact/analysis-document.md)
- [Backlog de Produto](./artifact/analysis-backlog.md)

## 🧠 Exemplos de Uso de LLMs

- **LLMs (ChatGPT ou Gemini)**:
  - Geração estruturada do DRS a partir do documento de contexto e plano
  - Sugestão de requisitos não funcionais com base em domínio e tecnologias
  - Proposição inicial de user stories a partir de regras de negócio

- **RAG (Retrieval-Augmented Generation)**:
  - Análise de documentos legados para extração de regras ou termos técnicos
  - Geração incremental de requisitos por módulo ou funcionalidade

## 📊 Indicadores de Avaliação

### Qualitativos
- Clareza dos requisitos e user stories gerados
- Consistência com o planejamento e escopo definidos
- Grau de alinhamento dos requisitos com as necessidades do negócio

### Quantitativos
- Nº de requisitos gerados com LLM vs. manualmente
- Taxa de aproveitamento das histórias sugeridas pela LLM
- Tempo médio por requisito/story
- Nº de revisões por artefato

## 🔗 Prompts

- [Prompt A - Documento de Requisitos de Software (DRS)](./prompts.md)
- [Prompt B - Backlog de Produto](./prompts.md)


## 🛠️ Instrumentação Recomendada

- Registro de prompts e outputs
- Log das interações com LLMs (aceitação/rejeição de sugestões)
- Controle de versão dos artefatos (ex: Git)
- Registro de tempo por atividade
