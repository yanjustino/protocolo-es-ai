## 🔗 Anexos

### A. Prompt para Estudos de benchmarking e tendências
````xml
<context>
    Você irá atuar como pesquisador da área de engenharia de software atuando como consultor na indústria. Seu papel é 
    auxiliar na construção de soluções de software. {{DESCRIÇÃO GERAL DO PROBLEMA}}. Com base nisso, faça uma revisão 
    rápida nas bases de artigos acadêmicos e blogs técnicos da indústria para listar os tópicos e categorias de problemas, 
    bem como as referências relacionadas ao cenário descrito. Para isso, use os seguintes <inclusion_criteria> 
    e <exclusion_criteria>. Como saída use o <template>.
</context>

<inclusion_criteria> 
    1. artigos acadêmicos ou da índustria.
    2. artigos a partir de 2020.
    3. artigos publicado em revistas, sites, blogs técnicos.
    4. artigos da área de engenharia de software.
</inclusion_criteria>

<exclusion_criteria> 
    1. artigos sem autoria.
    2. artigos que não possuem casos reais.
    3. crie uma lista dos artigos seguindo o <template>
</exclusion_criteria>

<template>
    # Referencias

    | Título         | Autor        | Ano  | Referência | Link        |
    |----------------|--------------|------|------------|-------------|
    | {{TITULO}}     | {{AUTOR}}    | {{ANO}} | {{REFEÊNCIA}} | [Acessar]({{LINK}}) |
</template>
````

### B. Prompt para elaborar roteiro de entrevista
````xml
<context>
    Você irá atuar como um especialista em projetos de software com enfase elaboração e análise de requisitos. Seu papel
    é auxiliar na construção de soluções de software. {{DESCRIÇÃO DO PROBLEMA}}. Com base nisso, faça um roteiro de perguntas para ser conduzido 
    numa entrevista com os stakeholders. As perguntas devem ser objetivas o suficiente para obter informações das seguintes
    <categories>. Como saída use o seguinte <template>.
</context>

<categories> 
    - Descrição do problema
    - Lista de stakeholders
    - Documentos de referência
    - Descrição geral das funcionalidades
    - Lista de limitações e dependências
    - Lista de premissas (tecnologias, ambientes, recursos)
</categories>

<template>
    # QUESTÕES
    - #{{ID}} - {{QUESTÃO}} | {{CATEGORIA}}
</template>
````

### C. Prompt para geração do documento de contexto
````xml
<context>
    Você irá atuar como um especialista em projetos de software com enfase elaboração e análise de requisitos. 
    Seu papel é auxiliar na construção de soluções de software. {{DESCRIÇÃO GERAL DO PROBLEMA}}. Dado esse conjunto 
    de informações, escreva o documento de contexto do projeto com base nas <instructions>.
<context>

<instructions>
    1. Escreva o documento de contexto em Markdown
    2. Use o <template> como referência
    3. Use os conteúdos listados em <reference>
</instructions>

<template>
# 📄 Documento de Contexto do Projeto

## 1. Identificação do Projeto
- **Nome do Projeto:** 
- **Versão do Documento:** 
- **Autor(es):** 
- **Data de Criação / Revisão:** 

## 2. Visão Geral do Produto
- **Descrição do Produto:** 
- **Objetivo Principal:** 
- **Problemas que o produto pretende resolver:** 
- **Público-alvo:** 

## 3. Justificativa
- **Motivação para o projeto:** 
- **Benefícios esperados:** 
- **Cenários de uso:** 

## 4. Escopo Inicial
- **Itens incluídos no escopo:** 
- **Itens fora do escopo (exclusões):** 

## 5. Requisitos Iniciais
- **Requisitos Funcionais (alto nível):** 
  - Ex: Funcionalidades esperadas pelo usuário
- **Requisitos Não-Funcionais:** 
  - Ex: Desempenho, escalabilidade, usabilidade, segurança

## 6. Premissas
- **Tecnologias previstas ou preferidas:** 
- **Ambiente de execução:** 
- **Disponibilidade de recursos:** 

## 7. Restrições
- **Limitações técnicas ou operacionais:** 
- **Dependências externas ou obrigatórias:** 

## 8. Stakeholders
- **Principais interessados no projeto e seus papéis:** 
  - Ex: Usuários, desenvolvedores, patrocinadores, gestores

## 9. Critérios de Sucesso
- **Critérios objetivos para considerar o projeto bem-sucedido:** 
- **Indicadores ou métricas de avaliação:** 

## 10. Riscos Iniciais
- **Riscos técnicos, operacionais ou de negócio identificados:** 
- **Impacto e possíveis planos de mitigação:** 

## 11. Referências
- **Fontes de pesquisa, materiais de apoio ou documentação relacionada:** 
</template>

<references>
    - https://www.ibm.com/think/topics/business-rules-management-system#:~:text=A%20business%20rules%20management%20system%20(BRMS)%20provides%20business%20users%20with,their%20rules%20from%20the%20BRMS.
    - https://en.wikipedia.org/wiki/Business_rule_management_system#:~:text=A%20BRMS%20or%20business%20rule,place%20in%20applications%20and%20systems.
</references>

````
