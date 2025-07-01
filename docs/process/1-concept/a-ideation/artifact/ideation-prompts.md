## 🔗 Anexos

### A. Prompt para Estudos de benchmarking e tendências
````xml
<context>
    Você irá atuar como pesquisador da área de engenharia de software atuando como consultor na indústria. Seu papel é 
    auxiliar o Banco JUBV na construção de soluções de software. O banco possui uma area de investimentos que é muito 
    regulada pelo governo. Constantemente há alterações em regas de impostos sobre investimentos. O atual sistema da 
    área de investimentos possue divesas aplicações legadas (mainframe) as quais possuem regras de calculo de impostos 
    escritas diretamente nos seus códigos-fontes. Nesse cenário, a cada mudança a equipe acaba tendo que realizar 
    mudanças em váriras aplicações, testar e implantar. Dado a frequencia e a urgência que essa situação ocorre, 
    a equipe sente a necessidade de uma solucão para diminuir a complexidade e os riscos envolvidos nessas mudanças. 
    Com base nisso, faça uma revisão rápida nas bases de artigos acadêmicos e blogs técnicos da indústria para listar 
    os tópicos e categorias de problemas, bem como as referências relacionadas ao cenário do Banco JUBV. Para isso, 
    use os seguintes <inclusion_criteria> e <exclusion_criteria>. Como saída use o <template>.
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
    é auxiliar o Banco JUBV na construção de soluções de software. O banco possui uma area de investimentos que é muito 
    regulada pelo governo. Constantemente há alterações em regas de impostos sobre investimentos. O atual sistema da 
    área de investimentos possue divesas aplicações legadas (mainframe) as quais possuem regras de calculo de impostos 
    escritas diretamente nos seus códigos-fontes. Nesse cenário, a cada mudança a equipe acaba tendo que realizar 
    mudanças em váriras aplicações, testar e implantar. Dado a frequencia e a urgência que essa situação ocorre, a equipe
    sente a necessidade de uma solucão para diminuir a complexidade e os riscos envolvidos nessas mudanças. Com base 
    nisso, faça um roteiro de perguntas para ser conduzido numa entrevista com os stakeholders. As perguntas devem ser 
    objetivas o suficiente para obter informações das seguintes <categories>. Como saída use o seguinte <template>.
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
    Seu papel é auxiliar o Banco JUBV na construção de soluções de software. O banco possui uma area de investimentos 
    que é muito regulada pelo governo. Constantemente há alterações em regas de impostos sobre investimentos. O atual 
    sistema da área de investimentos possue divesas aplicações legadas (mainframe) as quais possuem regras de calculo 
    de impostos escritas diretamente nos seus códigos-fontes. Nesse cenário, a cada mudança a equipe acaba tendo que 
    realizar mudanças em váriras aplicações, testar e implantar. Dado a frequencia e a urgência que essa situação 
    ocorre, a equipe sente a necessidade de uma solucão para diminuir a complexidade e os riscos envolvidos nessas 
    mudanças. Nesse sentido, a equipe cogitou a criação de um motor de cálculo como serviço, que oferecerá mecanismos 
    para registro, gerenciamento e execução de funções lógicas e aritiméticas. Essa solução deve ser utilizada por uma 
    equipe de operações que terá autonomia de criar, alterar e retirar as regras do motor de calculo, sem precisar 
    modificar e implantar as aplicações do sistema. A gestão da área de investimentos do banco espera que esse motor 
    seja reutilizável em diversos contextos da área, e como consequencia no Banco JUBV. Em termos técnicos, a equipe de 
    tecnologia responsável pela construção do motor de calculo usa serviços AWS e adota dotnet framework com a 
    linguagem C#. Dado esse conjunto de informações, escreva o documento de contexto do projeto com base nas <instructions>.
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
