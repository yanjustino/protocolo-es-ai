# 📘 Plano do Projeto

## 1. Identificação do Projeto
- **Nome do Projeto:** Motor de Cálculo de Regras Tributárias - MVP
- **Versão do Documento:** 1.0
- **Autor(es):** Especialista em Análise de Requisitos (Consultor Externo)
- **Data de Criação / Revisão:** 28 de junho de 2025

## 2. Objetivo do Plano
Este plano tem como propósito delinear a estratégia e as etapas iniciais para o desenvolvimento do Motor de Cálculo de Regras Tributárias, com foco na entrega de um Produto Mínimo Viável (MVP) em um prazo de 90 dias. O objetivo é estabelecer um roteiro claro, definir responsabilidades, gerenciar riscos e garantir o alinhamento com os stakeholders para alcançar os benefícios propostos de agilidade e redução de riscos na gestão de regras de impostos.

## 3. Escopo do Projeto
### Entregas previstas (MVP):
* **Serviço do Motor de Cálculo de Regras Tributárias:** Funcionalidade principal de registro e execução de funções lógicas e aritméticas para cálculo de impostos.
* **Interface de Gerenciamento de Regras (UI):** Permite à equipe de operações criar, editar, desativar e ativar regras.
* **API RESTful:** Para integração com uma aplicação legada de mainframe.
* **Mecanismo Básico de Versionamento de Regras:** Para controle das alterações.
* **Funcionalidades Essenciais de Auditoria e Log:** Registro de operações de gerenciamento de regras.
* **Documentação Inicial:** Para uso e operação do motor e da UI.

### Limites e exclusões:
* Migração completa ou refatoração de todas as regras de impostos existentes em todas as aplicações legadas.
* Integração inicial com múltiplas aplicações legadas (foco em apenas uma para o MVP).
* Desenvolvimento de um sistema de workflow complexo para aprovação de regras.
* Funcionalidades avançadas de simulação e relatórios complexos.

### Critérios de aceitação:
* O motor de cálculo deve executar as regras corretamente para o cenário de impostos selecionado para a integração inicial.
* A equipe de operações deve conseguir criar e alterar regras básicas de impostos através da UI sem intervenção de TI.
* A aplicação legada integrada deve consumir o serviço do motor de cálculo e retornar os resultados esperados.
* A API do motor deve estar funcional e documentada.
* As operações de criação/alteração de regras devem ser auditáveis.
* Alta disponibilidade do serviço do motor de cálculo (conforme o critério de 99,9%).

## 4. Cronograma (90 dias - 6 Iterações de 15 dias)

| Iteração | Duração | Responsável | Entregável da Iteração | Cerimônias de Alinhamento |
|---|---|---|---|---|
| **Iteração 1: Descoberta e Detalhamento** | 15 dias | Analista de Requisitos, Líder Técnico | Requisitos detalhados do MVP (funcionais e não-funcionais). Prototipagem da UI. | Reunião de Kick-off com Stakeholders. Review de Requisitos. |
| **Iteração 2: Design e Integração Base** | 15 dias | Líder Técnico, Desenvolvedores | Design de Arquitetura do Motor e API. Definição do contrato da API. POC de integração com Mainframe. | Review de Design e Integração. |
| **Iteração 3: Desenvolvimento Core do Motor** | 15 dias | Desenvolvedores | Módulo de execução de regras implementado e testado unitariamente. Core da API funcional. | Daily Scrums. |
| **Iteração 4: Desenvolvimento UI e Gerenciamento de Regras** | 15 dias | Desenvolvedores | Interface de usuário (UI) para criação e edição de regras (funcionalidades básicas). Módulo de persistência de regras. | Review de Funcionalidades UI. |
| **Iteração 5: Integração e Testes Iniciais** | 15 dias | Desenvolvedores, QA | Integração do motor com a aplicação legada de mainframe selecionada. Plano de testes e primeiros casos de teste executados. | Review de Integração. |
| **Iteração 6: Ajustes, Auditoria e Preparação para Implantação** | 15 dias | Desenvolvedores, QA | Funcionalidades de auditoria e versionamento completas. Testes de aceitação (UAT) com a equipe de operações. Documentação finalizada. | Demonstração e Validação do MVP com Stakeholders. |
| **Implantação do MVP** | 2 dias | Equipe de TI, Infraestrutura | Motor de Cálculo em ambiente de produção. | Reunião pós-implantação. |

## 5. Equipe e Papéis
| Nome | Papel | Responsabilidades principais |
|---|---|---|
| (A ser definido) | Gerente de Projeto | Gestão do cronograma, comunicação, riscos e recursos do projeto. |
| (A ser definido) | Líder Técnico | Definição da arquitetura, diretrizes técnicas, revisão de código. |
| (A ser definido) | Analista de Requisitos | Elicitação, análise e documentação de requisitos, alinhamento com stakeholders. |
| (A ser definido) | Desenvolvedor (s) (2-3) | Desenvolvimento do motor, API, UI e integrações. |
| (A ser definido) | QA/Testador | Elaboração de planos de teste, execução de testes, garantia de qualidade. |
| (A ser definido) | Especialista em Mainframe | Apoio na integração com sistemas legados, entendimento de dados. |

## 6. Recursos Necessários
- **Tecnológicos:**
    * **Linguagem de Programação:** C#
    * **Framework:** .NET 9
    * **Serviços em Nuvem:** AWS (EC2, Lambda, S3, RDS/DynamoDB, API Gateway, CloudWatch).
    * **Ferramentas de Desenvolvimento:** Visual Studio, Git, Jira/Trello (para gestão de tarefas).
    * **Ferramentas de Teste:** Postman, ferramentas de teste de UI (ex: Selenium).
    * **Sistema de Gerenciamento de Regras (BRMS):** Embora o projeto seja para construir um motor, considerar a análise de ferramentas de BRMS existentes para referência arquitetural ou futura avaliação. Um Business Rules Management System (BRMS) fornece aos usuários de negócios a capacidade de definir e gerenciar as regras de negócio que governam suas operações. Um BRMS ou sistema de gerenciamento de regras de negócio é um sistema de software usado para definir, implantar, executar, monitorar e manter as várias decisões de lógica de negócios que são executadas em aplicações e sistemas.
- **Humanos:**
    * 1 Gerente de Projeto
    * 1 Líder Técnico
    * 1 Analista de Requisitos
    * 2-3 Desenvolvedores C#/.NET/AWS
    * 1 QA/Testador
    * 1 Especialista em Mainframe (dedicação parcial para a integração)
- **Financeiros:** Orçamento para contratação de recursos humanos (se necessário), licenças de software (se aplicável) e consumo de serviços AWS.

## 7. Riscos e Mitigações
| Risco Identificado | Impacto | Probabilidade | Plano de Mitigação |
|---|---|---|---|
| Complexidade na extração e modelagem das regras de negócio dos sistemas legados. | Alto | Média | Dedicar analistas de negócio experientes, realizar workshops com especialistas de negócio. Iniciar com um subconjunto de regras menos complexas para o MVP. |
| Dificuldade na integração com o sistema legado de mainframe selecionado. | Alto | Média | Engajamento precoce do especialista em mainframe. Desenvolver uma Prova de Conceito (POC) de integração na Iteração 2. Definir contratos de interface claros e testá-los isoladamente. |
| Resistência à mudança por parte das equipes (desenvolvimento ou operações). | Médio | Média | Engajamento ativo dos stakeholders desde o início. Realizar demonstrações regulares e solicitar feedback. Oferecer treinamentos práticos sobre o uso da nova ferramenta. |
| Incompatibilidade ou limitações das tecnologias escolhidas (AWS, .NET 9) para certas regras complexas. | Médio | Baixa | Realizar uma análise aprofundada das regras mais complexas identificadas na fase de requisitos. Implementar POCs específicas para validar a viabilidade técnica dessas regras. |
| Atrasos na disponibilidade de recursos (humanos, infraestrutura AWS). | Médio | Média | Antecipar o planejamento de alocação de equipe. Solicitar provisionamento de recursos AWS com antecedência, considerando possíveis burocracias internas. |

## 8. Comunicação
- **Canais utilizados:**
    * E-mail para comunicações formais e registro de decisões.
    * Slack/Microsoft Teams para comunicação diária da equipe.
    * Jira/Trello para acompanhamento de tarefas e progresso.
    * Confluence/SharePoint para documentação.
- **Frequência de atualizações:**
    * **Daily Scrums:** Reuniões diárias da equipe de desenvolvimento (15 minutos).
    * **Review da Iteração:** Ao final de cada iteração (15 dias), com a equipe e stakeholders.
    * **Reunião de Alinhamento com Gerência:** Quinzenal, para status e decisões estratégicas.
    * **Demonstrações do Produto:** Ao final das iterações com entregáveis de software.
- **Responsável pela comunicação com stakeholders:** Gerente de Projeto, com apoio do Analista de Requisitos e Líder Técnico nas demonstrações.

## 9. Aprovação
- **Stakeholders responsáveis pela aprovação do plano:**

| Nome | Papel | Assinatura (se necessário) |
|---|---|---|
| (A ser definido) | Patrocinador do Projeto (Gerência da Área de Investimentos) | |
| (A ser definido) | Gerente Executivo de TI | |
| (A ser definido) | Gerente da Área de Operações de Investimentos | |

---

## 10. Referências
- Business Rules Management System (BRMS) - IBM: [https://www.ibm.com/think/topics/business-rules-management-system](https://www.ibm.com/think/topics/business-rules-management-system)
- Business Rule Management System (BRMS) - Wikipedia: [https://en.wikipedia.org/wiki/Business_rule_management_system](https://en.wikipedia.org/wiki/Business_rule_management_system)
- Documento de Contexto do Projeto "Motor de Cálculo de Regras Tributárias" (ideation-context.md)