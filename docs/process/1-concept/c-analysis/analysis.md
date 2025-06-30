# 💡 ANALYSIS
A etapa de análise é dedicada à compreensão profunda do problema, do domínio e das necessidades dos usuários, transformando essas informações em requisitos claros, priorizados e viáveis. Ela conecta diretamente a visão estratégica (ideação e planejamento) com a solução técnica que será modelada e construída.

Nesta fase, são realizadas atividades que permitem detalhar o que o sistema deve fazer, sem ainda entrar na implementação. O foco está em identificar requisitos funcionais e não funcionais, fluxos de negócio, regras, exceções e interações com sistemas externos.

## 📘 Atividades 

| Atividade                              | Artefatos                                                                                     | Execução            |
|----------------------------------------|-----------------------------------------------------------------------------------------------|---------------------|
| Elaboração do Documento de requisitos  | Lista de Requisitos Funcionais <br> Lista de Requisitos Não Funcionais <br> Casos de uso <br> Regras de Negócio <br> Critérios de aceitação | 🧑🏽🧠 Humano com suporte de IA |
| Análise de processos existentes ou documentação legada | Avaliar uso de bases de conhecimento e RAG                                                   | 🧑🏽🧠 Humano com suporte de IA |
| Elaboração de Backlog                  | User stories                                                                                 | 🧑🏽🧠 Humano com suporte de IA |

## 🧰 Ferramentas
- LLMs
    - ChatGpt o3 | Gemini 2.5 Pro
    - NotbookLLM

## 📄 Artefatos

- [Documento de Requisitos de Software (DRS)](./artifact/analysis-document.md)
- [Backlog de Produto](./artifact/analysis-backlog.md)

## 🔗 Anexos


### Prompt para geração do Documento de Requisitos de Software (DRS)
````xml
<context>
    Você irá atuar como um especialista em projetos de software com enfase elaboração de requisitos. Seu papel é auxiliar na geração de artefatos de análise para guiar a modelagem e construção da solução técnica. Com base no {{DOCUMENTO DE CONTEXTO}} e no {{PLANO}} listados em <attachements>, elabore o Documento de Requisitos de Software (DRS). Para isso, siga as instruções defenido em <instructions>. 
<context>

<attachement>
    - ideation-context.md
    - plan-document.md
</attachement>

<instructions>
    1. Gere o Documento de Requisitos de Software (DRS) seguindo o <template> markdown
</instructions>

<template>
# 📄 Documento de Requisitos de Software (DRS)

## 1. Identificação do Projeto
- **Nome do Projeto:** 
- **Versão do Documento:** 
- **Data:** 
- **Autor(es):** 

---

## 2. Objetivo do Documento
Este documento tem como objetivo descrever, de forma clara e organizada, os requisitos funcionais e não funcionais necessários para o desenvolvimento do sistema proposto, além de apresentar as regras de negócio, casos de uso e restrições associadas ao projeto.

---

## 3. Visão Geral do Sistema
- **Descrição do Sistema:**  
  Breve visão do que o sistema irá realizar.
- **Objetivos do Sistema:**  
  Quais problemas o sistema resolve ou que valor entrega.
- **Público-alvo / Usuários Finais:**  
  Quem utilizará o sistema e para qual finalidade.
- **Escopo Funcional Geral:**  
  Quais áreas ou processos o sistema irá cobrir.

---

## 4. Requisitos Funcionais
Lista das funcionalidades que o sistema deve realizar.

| Código | Nome                   | Descrição                                            | Critérios de Aceitação                     | Prioridade |
|--------|------------------------|------------------------------------------------------|--------------------------------------------|------------|
| RF01   |                        |                                                      |                                            | Alta       |
| RF02   |                        |                                                      |                                            | Média      |

---

## 5. Requisitos Não Funcionais
Aspectos de qualidade do sistema (desempenho, segurança, usabilidade etc.).

| Código | Tipo                   | Descrição                                            | Prioridade |
|--------|------------------------|------------------------------------------------------|------------|
| RNF01  |                        |                                                      | Alta       |
| RNF02  |                        |                                                      | Média      |

---

## 6. Regras de Negócio
Conjunto de regras que definem o comportamento lógico do sistema.

| Código | Descrição |
|--------|-----------|
| RN01   |           |
| RN02   |           |

---

## 7. Casos de Uso / User Stories
Interações entre usuários e o sistema, descritas de forma narrativa ou estruturada.

### Caso de Uso Exemplo
- **Identificador:** CU01
- **Nome:** 
- **Ator Principal:** 
- **Descrição:** 
- **Fluxo Principal:**
  1. 
  2. 
- **Fluxos Alternativos / Exceções:**

---

## 8. Requisitos de Integração
Integrações com outros sistemas, serviços, APIs, ou bancos de dados.

- 
- 

---

## 9. Restrições Técnicas
Tecnologias obrigatórias, plataformas suportadas, padrões de arquitetura, ou limitações impostas por contexto do projeto.

- 
- 

---

## 10. Critérios de Aceitação Gerais
Critérios objetivos que devem ser atendidos para o sistema ser considerado pronto para entrega.

- 
- 

---

## 11. Anexos / Referências
Links, diagramas, documentos externos ou materiais complementares usados na elaboração deste DRS.

</template>

````


### Prompt para geração do Backlog de Produto
````xml
<context>
    Você irá atuar como um especialista em projetos de software com enfase elaboração de requisitos. Seu papel é auxiliar na geração de artefatos de análise para guiar a modelagem e construção da solução técnica. Com base no {{DOCUMENTO DE CONTEXTO}}, {{DOCUMENTO DE ANALISE}} e {{PLANO}} listados em <attachements>, elabore o Backlog de Produto. Para isso, siga as instruções defenido em <instructions>. 
<context>

<attachement>
    - ideation-context.md
    - analysis-document.md
    - plan-document.md
</attachement>

<instructions>
    1. Gere o Backlog de Produto seguindo o <template> markdown.
</instructions>

<template>
# 📋 Backlog de Produto

Backlog com histórias de usuário priorizadas para orientar o desenvolvimento do produto.

---

## 📌 Legenda das Colunas
- **ID**: Código identificador da história (ex: US01)
- **História do Usuário**: Desejo descrito do ponto de vista do usuário
- **Prioridade**: Alta / Média / Baixa
- **Critérios de Aceitação**: Condições mínimas para considerar a história entregue
- **Status**: A Fazer / Em Progresso / Concluído / Em Validação

---

## 📦 Backlog

| ID    | História do Usuário                                                    | Prioridade | Critérios de Aceitação                                             | Status        |
|-------|------------------------------------------------------------------------|------------|----------------------------------------------------------------------|---------------|
| US01  | Como [usuário], quero [ação/função] para [benefício/valor]             | Alta       | - [Critério 1] <br> - [Critério 2]                                   | A Fazer       |
| US02  | Como [usuário], quero [ação/função] para [benefício/valor]             | Média      | - [Critério 1] <br> - [Critério 2]                                   | Em Progresso  |
| US03  | Como [usuário], quero [ação/função] para [benefício/valor]             | Baixa      | - [Critério 1] <br> - [Critério 2]                                   | Concluído     |

---

## 🧾 Template para Nova História

### ID: USXX
**História do Usuário:**  
Como [tipo de usuário], quero [funcionalidade desejada] para [valor/benefício esperado].

**Prioridade:** Alta | Média | Baixa  
**Critérios de Aceitação:**  
- [Critério 1]  
- [Critério 2]  
- [Critério 3]  

**Status:** A Fazer | Em Progresso | Em Validação | Concluído

---

## 🔄 Observações Gerais
- As histórias devem ser compreensíveis para todos os stakeholders.
- Critérios de aceitação ajudam no alinhamento entre desenvolvimento e testes.
- O backlog é vivo: pode (e deve) ser ajustado conforme evolução do projeto.
</template>
````



## Referências
- [Prompt engineering overview](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
