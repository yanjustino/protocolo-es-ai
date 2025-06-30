# 🎨 Protocolo de Adoção de LLMs – Fase: DESIGN

## 🎯 Objetivo

Transformar os requisitos levantados na análise em representações técnicas detalhadas e viáveis para orientar a construção da solução. LLMs são utilizados para apoiar decisões arquiteturais, modelagem de dados, criação de diagramas e documentação de APIs, garantindo clareza, coesão e manutenibilidade.

---

## 📘 Atividades e Interações com LLMs

| Atividade                          | Papel da LLM                                                                                 | Artefato(s)                                                              | Avaliação Qualitativa                                               | Avaliação Quantitativa                                  |
|------------------------------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------|
| Aplicar Análise de Trade-offs      | Sugestão e estruturação de árvores de atributos de qualidade (ATAM + arc42)                 | `design-tradeoffs.md`                                                   | Clareza dos cenários, alinhamento com atributos do negócio         | Nº de atributos priorizados corretamente                |
| Definir Modelagem de dados         | Geração de entidades, atributos, relacionamentos e DER/MER com base em requisitos            | `design-modelagem-dados.md`, `design-der.md`                            | Correção estrutural do modelo; normalização adequada                | Nº de entidades geradas com reutilização                 |
| Definir Arquitetura de software    | Geração dos diagramas C4 (sistema, containers, componentes)                                  | `design-diagram-context.md`, `design-diagram-container.md`, `design-diagram-component.md` | Coesão entre camadas, clareza nas fronteiras de componentes         | Nº de iterações até arquitetura estável                  |
| Definir Fluxos de interação        | Geração de diagramas de sequência, fluxogramas ou atividades                                | `design-fluxos.md` (opcional)                                           | Completude dos fluxos; identificação de exceções e eventos          | Nº de fluxos aceitos sem revisão                         |
| Criar Protótipos de interface (UI) | Geração de wireframes, sugestões de interface, descrição de jornada do usuário              | `design-ui.md` (opcional)                                               | Usabilidade, consistência visual, aderência ao domínio              | Nº de elementos reaproveitados no front-end              |
| Design de APIs                     | Definição de endpoints, payloads, autenticação, versionamento                               | `design-apis.md`                                                         | Conformidade com boas práticas REST; compatibilidade com integração | Nº de endpoints aceitos; tempo médio por definição       |

## 📂 Artefatos Modelos

- [Modelo de entidades e relacionamentos](./artifact/design-modelagem-dados.md)
- [Árvore de atributos de qualidade](./artifact/design-tradeoffs.md)
- [Diagrama de Contexto (C4)](./artifact/design-diagram-context.md)
- [Diagrama de Containers (C4)](./artifact/design-diagram-container.md)
- [Diagrama de Componentes (C4)](./artifact/design-diagram-component.md)

## 🧠 Exemplos de Aplicações com LLMs

- **Claude 4 Sonnet**:
  - Organização de cenários para análise de trade-offs
  - Elaboração de modelos de dados baseados em regras de negócio
  - Geração automática de diagramas (PlantUML e MermaidJS)

- **Cursor IDE + LLM**:
  - Geração de contratos de API inline
  - Sugestões estruturadas para modularização e dependências


## 📊 Indicadores para Avaliação

### Qualitativos
- Clareza dos artefatos técnicos
- Grau de reutilização do design em fases posteriores
- Aderência a boas práticas arquiteturais (ex. SOLID, C4, REST)

### Quantitativos
- Nº de artefatos gerados por tempo
- Tempo médio para gerar e revisar diagramas
- Taxa de aceitação de sugestões de arquitetura do LLM
- Nº de alterações nas decisões de design ao longo do projeto

## 🔗 Prompts

- [Prompt A - Análise de Tradeoffs](./prompts.md)
- [Prompt B - Modelo Entidade Relacionamento(MER/DER)](./prompts.md)
- [Prompt C - Diagramas de Arquitetura](./prompts.md)

## 🛠️ Instrumentação Recomendada

- Registro de prompts e outputs
- Log das interações com LLMs (aceitação/rejeição de sugestões)
- Controle de versão dos artefatos (ex: Git)
- Registro de tempo por atividade


