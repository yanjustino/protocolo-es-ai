# 💡 DESIGN
A etapa de Design é responsável pela transformação dos requisitos levantados na análise em soluções técnicas concretas, que orientarão diretamente a construção do sistema. Nessa fase, são criadas as estruturas lógicas, funcionais e visuais que formarão a base da implementação. O foco está em traduzir “o que deve ser feito” (requisitos) em “como será feito” por meio de modelos, diagramas e decisões arquiteturais. Um bom design visa clareza, coesão, reutilização e manutenibilidade.

## 📘 Atividades 

| Atividade                          | Artefatos                                                                                     | Execução            |
|------------------------------------|-----------------------------------------------------------------------------------------------|---------------------|
| Aplicar Análise de Trade-offs      | Lista de cenários e atributos de qualidade. <br> Trade-offs arquiteturais                     | 🧑🏽🧠 Humano com suporte de IA |
| Definir Modelagem de dados         | Entidades, atributos, relacionamentos e restrições.                                           | 🧑🏽🧠 Humano com suporte de IA |
| Definir Arquitetura de software    | Diagramas de sistemas (integração entre sistemas). <br> Diagramas de containers (ex: camadas, microsserviços, monolito), tecnologias, frameworks e integração entre módulos. <br> Diagramas de Componentes (estrutura interna dos módulos e responsabilidades de cada parte do sistema). | 🧑🏽🧠 Humano com suporte de IA |
| Definir Fluxos de interação        | Diagramas de sequência, casos de uso, fluxogramas de atividades, etc.                         | 🧑🏽🧠 Humano com suporte de IA |
| Criar Protótipos de interface (UI) | Quando aplicável, criação de wireframes ou mockups para validar a experiência do usuário.      | 🧑🏽🧠 Humano com suporte de IA |
| Design de APIs                     | Definição de contratos, formatos de payload, autenticação e padrões de versionamento.         | 🧑🏽🧠 Humano com suporte de IA |

## 🧰 Ferramentas
- LLMs
    - claude-4-sonnet
- cursor IDE

## 📄 Artefatos

- [Modelagem de dados](./design-modelagem-dados.md)
- [Análise de Trade-offs ](./design-tradeoffs.md)
- [Arquitetura de software (Main)](./design-diagram.md)
- [Arquitetura de software (Contexto)](./design-diagram-context.md)
- [Arquitetura de software (Containers)](./design-diagram-container.md)
- [Arquitetura de software (Componentes)](./design-diagram-component.md)

## 🔗 Anexos

### Prompt para Análise de Tradeoffs
````xml
<context>
    Você irá atuar como um arquiteto de software sênior. Seu papel é auxiliar na geração de artefatos de arquitetura para guiar a construção da solução técnica. Com base no {{DOCUMENTO DE ANALYSIS}} e {{BACKLOG}} listados em <attachements>, elabore a {{Quality Attribute Utility Tree}} para o processo de análise de Tradeoffs. Para isso, siga as instruções defenido em <instructions>. 
<context>

<attachement>
    - {{DOCUMENTO DE ANALYSIS}} = analysys-document.md
    - {{BACKLOG}} = analysis-backlog.md
</attachement>

<instructions>
    1. Crie um documento de {{Quality Attribute Utility Tree}} usando o <template> como modelo
</instructions>


<template>
# 🌳 Quality Attribute Utility Tree (ATAM + arc42) – Template Genérico

Este documento organiza os atributos de qualidade do sistema em uma árvore de utilidade, detalhando os cenários segundo a estrutura recomendada pelo arc42.

---

## 📘 Legenda dos Elementos do Cenário

Cada cenário de qualidade é descrito com os seguintes elementos:

- **Atributo de Qualidade:** Categoria principal (ex: Desempenho, Segurança)
- **Subatributo / Dimensão:** Aspecto específico do atributo (ex: tempo de resposta, confidencialidade)
- **Estímulo:** Evento que aciona o cenário
- **Ambiente:** Contexto em que o estímulo ocorre
- **Artefato Afetado:** Parte do sistema impactada
- **Resposta Esperada:** Comportamento do sistema
- **Medição:** Critério de avaliação da resposta
- **Importância / Prioridade:** Alta, Média ou Baixa

---

## 🧩 Atributo de Qualidade: `<< Nome do Atributo >>`

### 🔸 Subatributo: `<< Nome do Subatributo >>`

| Estímulo                     | Ambiente                     | Artefato Afetado       | Resposta Esperada                          | Medição                        | Importância |
|-----------------------------|------------------------------|-------------------------|--------------------------------------------|--------------------------------|-------------|
| << Descreva o estímulo >>   | << Descreva o ambiente >>    | << Artefato >>          | << Comportamento esperado do sistema >>    | << Como medir a resposta >>    | Alta / Média / Baixa |
|                             |                              |                         |                                            |                                |             |

---

## 🧩 Atributo de Qualidade: `<< Outro Atributo >>`

### 🔸 Subatributo: `<< Subatributo relevante >>`

| Estímulo                     | Ambiente                     | Artefato Afetado       | Resposta Esperada                          | Medição                        | Importância |
|-----------------------------|------------------------------|-------------------------|--------------------------------------------|--------------------------------|-------------|
|                             |                              |                         |                                            |                                |             |

---

## 📝 Observações

- Um atributo pode conter múltiplos subatributos ou dimensões específicas.
- Os cenários devem ser claros, verificáveis e úteis para apoiar decisões de arquitetura.
- A prioridade auxilia na análise de trade-offs em sessões de avaliação arquitetural (ex: ATAM).
</template>
````


### Prompt para geração do Modelo Entidade Relacionamento(MER/DER)
````xml
<context>
    Você irá atuar como um engenheiro de dados sênior. Seu papel é auxiliar na geração de artefatos de arquitetura para guiar a construção da solução técnica. Com base no {{DOCUMENTO DE ANALYSIS}} e no {{BACKLOG}} listados em <attachements>, elabore o Modelo Entidade Relacionamento {{MER}} e o Diagrama Entidade Relacionamento {{DER}}. Para isso, siga as instruções defenido em <instructions>. 
<context>

<attachement>
    - analysys-document.md
    - analysis-backlog.md
</attachement>

<instructions>
    1. Gere o {{MER}} com base em <template>.
    2. Após geração do {{MER}}, gere o {{DER}}.
    3. O {{DER}} deve representar a {{MER}}
    4. Gere um {{DER}} no formato plantuml
    5. Gere um {{DER}} no formato marmeidjs como alternativa
</instructions>

<template>
# 🗂️ Modelo Entidade-Relacionamento (MER) – Template Genérico

Documentação das entidades, atributos e relacionamentos do sistema.

---

## 📘 Entidades

### 🧩 Entidade: `Entidade1`

| Atributo       | Tipo de Dado | PK | FK | Obrigatório | Observações                    |
|----------------|--------------|----|----|-------------|--------------------------------|
| id_entidade1   | INT          | ✅ |    | ✅          | Identificador único            |
| nome           | VARCHAR(100) |    |    | ✅          | Nome da entidade               |
| descricao      | TEXT         |    |    |             | Campo opcional de descrição    |

---

### 🧩 Entidade: `Entidade2`

| Atributo       | Tipo de Dado | PK | FK | Obrigatório | Observações                              |
|----------------|--------------|----|----|-------------|------------------------------------------|
| id_entidade2   | INT          | ✅ |    | ✅          | Identificador único                      |
| entidade1_id   | INT          |    | ✅ | ✅          | FK para Entidade1                        |
| status         | VARCHAR(20)  |    |    | ✅          | Domínio: ["ativo", "inativo", "pendente"]|

---

### 🧩 Entidade: `Entidade3`

| Atributo       | Tipo de Dado | PK | FK | Obrigatório | Observações           |
|----------------|--------------|----|----|-------------|-----------------------|
| id_entidade3   | UUID         | ✅ |    | ✅          | Identificador global  |
| nome_externo   | VARCHAR(80)  |    |    |             | Nome de integração    |

---

## 🔗 Relacionamentos

| Relacionamento                                                         | Tipo (Cardinalidade) | Atributos Associativos        | Observações                                           |
|------------------------------------------------------------------------|----------------------|-------------------------------|--------------------------------------------------------|
| `Entidade1` se relaciona com `Entidade2` via `entidade1_id`            | 1:N                  | —                             | Uma Entidade1 pode estar vinculada a várias Entidade2  |
| `Entidade2` se relaciona com `Entidade3` via `entidade2_entidade3`     | N:N                  | `data_associacao`, `status`   | Relacionamento muitos-para-muitos com atributos próprios |

---

## 📎 Legenda

- **PK:** Chave Primária  
- **FK:** Chave Estrangeira  
- **Tipo de Dado:** Exemplos: INT, VARCHAR(n), DATE, BOOLEAN, UUID  
- **Obrigatório:** Campo obrigatório (`NOT NULL`)  
- **Tipo (Cardinalidade):** 1:1, 1:N, N:N  

---

## 📝 Observações Gerais

- Toda entidade deve possuir uma chave primária única (PK).
- Relacionamentos do tipo N:N devem ser representados com uma tabela associativa.
- Atributos com valores fixos devem ter seus domínios documentados.

</template>

````

### Prompt para geração dos diagramas de Arquitetura
````xml
<context>
    Você irá atuar como um arquiteto de software sênior. Seu papel é auxiliar na geração de artefatos de arquitetura para guiar a construção da solução técnica. Com base no {{DOCUMENTO DE ANALYSIS}}, {{BACKLOG}}, {{TRADEOFFS}} e {{DER}} listados em <attachements>, elabore os diagramas de arquitetura dos sistemas, containeres e componentes da solução. Leve em consideração que a equipe é especializada em AWS, dotnet e C#. Além disso, a equipe deseja evitar uma complexidade inical no projeto. Nesse sentido, ela quer apostar em um monolito modular para backend. 
    Dado esse contexto, siga as instruções defenido em <instructions>. 
<context>

<attachement>
    - {{DOCUMENTO DE ANALYSIS}} = analysys-document.md
    - {{BACKLOG}} = analysis-backlog.md
    - {{TRADEOFFS}} = design-tradeoffs.md
    - {{DER}} = design-der.md
</attachement>

<instructions>
    1. Use a especificação {{C4}} Model listados em <references>
    2. Crie o diagrama {{System context diagram}} do {{C4}}
    3. Crie o diagrama {{Container diagram}} do {{C4}}
    4. Crie o diagrama {{Component diagram}} do {{C4}}
    5. Use o {{C4-PlantUML}} para gerar os diagramas {{C4}} no formato plantuml
    6. Use o MarmeidJs para gerar os diagramas {{C4}} como alternativa
</instructions>

<references>
 - {{C4}} = https://c4model.com/introduction
 - {{System context diagram}} = https://c4model.com/diagrams/system-context
 - {{Container diagram}} = https://c4model.com/diagrams/container
 - {{Component diagram}} = https://c4model.com/diagrams/component
 - {{C4-PlantUML}} = https://github.com/plantuml-stdlib/C4-PlantUML
</references>
````




## Referências
- [Prompt engineering overview](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
