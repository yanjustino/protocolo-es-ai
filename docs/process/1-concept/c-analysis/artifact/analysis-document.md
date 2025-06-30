# 📄 Documento de Requisitos de Software (DRS)

## 1. Identificação do Projeto
- **Nome do Projeto:** Motor de Cálculo de Regras Tributárias - MVP
- **Versão do Documento:** 1.0
- **Data:** 28 de junho de 2025
- **Autor(es):** Especialista em Análise de Requisitos (Consultor Externo)

---

## 2. Objetivo do Documento
Este documento tem como objetivo descrever, de forma clara e organizada, os requisitos funcionais e não funcionais necessários para o desenvolvimento do Produto Mínimo Viável (MVP) do Motor de Cálculo de Regras Tributárias, além de apresentar as regras de negócio, casos de uso e restrições associadas ao projeto. Ele servirá como base para a modelagem, construção e validação da solução técnica, garantindo o alinhamento com os objetivos estratégicos do Banco JUBV.

---

## 3. Visão Geral do Sistema
- **Descrição do Sistema:** O Motor de Cálculo de Regras Tributárias é um serviço centralizado que proporcionará mecanismos para o registro, gerenciamento e execução de funções lógicas e aritméticas relacionadas a cálculos de impostos sobre investimentos. Ele será projetado para desacoplar as regras de negócio das aplicações legadas do Banco JUBV.
- **Objetivos do Sistema:** Reduzir a complexidade, os riscos e o tempo de resposta nas atualizações de regras de impostos sobre investimentos, proporcionando agilidade na adaptação às constantes mudanças regulatórias. Capacitar a equipe de operações com autonomia para criar, alterar e desativar regras sem intervenção de TI. Promover a reusabilidade das regras de cálculo em diversos contextos do banco.
- **Público-alvo / Usuários Finais:**
    * **Equipe de Operações da Área de Investimentos:** Usuários primários para criação, alteração e desativação das regras.
    * **Equipe de Desenvolvimento de TI:** Responsáveis pela construção e manutenção do motor.
    * **Área de Investimentos do Banco JUBV:** Beneficiários da agilidade e redução de riscos.
- **Escopo Funcional Geral:** O sistema cobrirá as funcionalidades essenciais para o gerenciamento e execução de regras de impostos sobre investimentos, incluindo uma interface de usuário para operações, uma API para integração e mecanismos básicos de versionamento e auditoria das regras.

---

## 4. Requisitos Funcionais
Lista das funcionalidades que o sistema deve realizar para o MVP.

| Código | Nome | Descrição | Critérios de Aceitação | Prioridade |
|---|---|---|---|---|
| RF01 | Gerenciamento de Regras (Criação) | O motor deve permitir à equipe de operações criar novas regras, especificando condições e ações de cálculo (ex: cálculo de alíquota, base de cálculo, isenção). | A equipe de operações consegue adicionar uma nova regra de cálculo de imposto via UI, com os parâmetros definidos. A regra é persistida e pode ser visualizada. | Alta |
| RF02 | Gerenciamento de Regras (Edição) | O motor deve permitir à equipe de operações editar regras existentes, incluindo a modificação de suas condições e ações. | A equipe de operações consegue modificar uma regra existente via UI e salvar as alterações. As modificações são registradas com versionamento. | Alta |
| RF03 | Gerenciamento de Regras (Ativação/Desativação) | O motor deve permitir à equipe de operações ativar e desativar regras, controlando sua aplicação nos cálculos. | A equipe de operações pode alternar o status de ativação/desativação de uma regra via UI. Regras desativadas não são consideradas no cálculo. | Alta |
| RF04 | Execução de Regras de Cálculo | O motor deve ser capaz de executar as regras ativas com base em dados de entrada fornecidos pelas aplicações clientes, retornando o resultado do cálculo de imposto. | A API do motor recebe os dados de entrada, processa as regras aplicáveis e retorna o valor correto do imposto conforme as regras ativas. | Alta |
| RF05 | Interface de Programação de Aplicações (API) | O motor deve fornecer uma API RESTful para integração com outras aplicações, incluindo sistemas legados. | A API é acessível e documentada. Uma aplicação cliente consegue invocar a API com os parâmetros necessários e receber uma resposta válida. | Alta |
| RF06 | Versionamento de Regras | O motor deve manter um histórico de versões de cada regra, permitindo consultas e, se necessário, o retorno a versões anteriores. | Cada alteração em uma regra gera uma nova versão. É possível consultar o histórico de alterações de uma regra. | Média |
| RF07 | Auditoria e Log de Operações | O motor deve registrar todas as operações de criação, alteração e desativação de regras, incluindo o usuário responsável e o timestamp da operação. | Um log de auditoria é gerado para cada operação de gerenciamento de regras, contendo informações essenciais para rastreabilidade. | Alta |
| RF08 | Consulta de Regras | O motor deve permitir a consulta das regras cadastradas através da interface de gerenciamento. | A equipe de operações consegue visualizar a lista de regras, filtrar e buscar regras específicas na UI. | Média |

---

## 5. Requisitos Não Funcionais
Aspectos de qualidade do sistema (desempenho, segurança, usabilidade etc.) para o MVP.

| Código | Tipo | Descrição | Prioridade |
|---|---|---|---|
| RNF01 | Desempenho | O motor deve ser capaz de processar um alto volume de requisições de cálculo com baixa latência, visando um tempo de resposta médio inferior a 50ms para 95% das requisições. | Alta |
| RNF02 | Escalabilidade | A solução deve ser projetada para ser escalável horizontalmente, permitindo o aumento da capacidade de processamento em picos de demanda sem degradação significativa do desempenho. | Alta |
| RNF03 | Disponibilidade | O motor de cálculo deve ter alta disponibilidade, com um uptime de 99,9% ou superior, minimizando interrupções de serviço. | Alta |
| RNF04 | Segurança | O acesso à interface de gerenciamento de regras e à API do motor deve ser seguro e autenticado, protegendo contra acessos não autorizados. A solução deve proteger contra injeção de código nas regras. | Alta |
| RNF05 | Auditabilidade | O sistema deve permitir a rastreabilidade completa de todas as alterações nas regras e das execuções de cálculo, facilitando processos de auditoria interna e externa. | Alta |
| RNF06 | Usabilidade | A interface para gerenciamento de regras deve ser intuitiva e de fácil compreensão para a equipe de operações, minimizando a necessidade de treinamento extensivo. | Alta |
| RNF07 | Tolerância a Falhas | O sistema deve ser capaz de se recuperar de falhas sem perda de dados ou interrupção significativa do serviço. | Média |
| RNF08 | Manutenibilidade | O código-fonte do motor deve ser modular, bem documentado e seguir padrões de codificação para facilitar futuras manutenções e evoluções. | Média |

---

## 6. Regras de Negócio
Conjunto de regras que definem o comportamento lógico do sistema, conforme o escopo inicial do MVP.

| Código | Descrição |
|---|---|
| RN01 | Uma regra de imposto é composta por um conjunto de condições e uma ação de cálculo associada. |
| RN02 | Uma regra só pode ser executada se estiver ativa. |
| RN03 | A execução das regras deve seguir uma ordem de precedência configurável ou implícita (a ser definida com a equipe de negócio). |
| RN04 | A alteração de uma regra ativa requer a criação de uma nova versão, mantendo a versão anterior para fins de auditoria. |
| RN05 | O motor deve ser capaz de avaliar expressões lógicas e aritméticas complexas definidas nas regras. |
| RN06 | As regras devem ser capazes de acessar e utilizar os dados de entrada fornecidos pela aplicação cliente para a avaliação das condições e execução dos cálculos. |

---

## 7. Casos de Uso / User Stories
Interações entre usuários e o sistema, descritas de forma narrativa ou estruturada, com foco no MVP.

### Caso de Uso 1: Gerenciar Regras de Imposto
- **Identificador:** CU01
- **Nome:** Gerenciar Regras de Imposto (Criação, Edição, Ativação/Desativação)
- **Ator Principal:** Equipe de Operações da Área de Investimentos
- **Descrição:** Permite que a equipe de operações crie novas regras de imposto, edite regras existentes e alterne o status (ativa/desativa) de uma regra, garantindo que as modificações sejam aplicadas sem dependência da equipe de TI.
- **Fluxo Principal:**
  1. A equipe de operações acessa a interface de gerenciamento do Motor de Cálculo.
  2. O sistema exibe a lista de regras existentes.
  3. **Para Criar:**
      a. O ator seleciona a opção "Criar Nova Regra".
      b. O sistema exibe um formulário para definição da regra (nome, descrição, condições, ações de cálculo).
      c. O ator preenche o formulário e salva a nova regra.
      d. O sistema valida os dados, persiste a regra e a adiciona à lista.
  4. **Para Editar:**
      a. O ator seleciona uma regra existente na lista.
      b. O sistema exibe os detalhes da regra para edição.
      c. O ator modifica os parâmetros da regra e salva as alterações.
      d. O sistema valida os dados, persiste a nova versão da regra e atualiza a lista.
  5. **Para Ativar/Desativar:**
      a. O ator seleciona uma regra na lista e escolhe "Ativar" ou "Desativar".
      b. O sistema altera o status da regra e registra a operação.
- **Fluxos Alternativos / Exceções:**
    * **FA1.1 - Dados Inválidos:** Se os dados da regra forem inválidos, o sistema informa o erro e permite correção.
    * **FA1.2 - Regra em Uso:** Se a regra estiver sendo utilizada por uma aplicação no momento da desativação, o sistema pode alertar ou atrasar a desativação até que o cálculo atual seja finalizado (a ser refinado).
    * **FA1.3 - Erro de Persistência:** O sistema informa caso não consiga persistir a regra por algum problema técnico.

### Caso de Uso 2: Executar Cálculo de Imposto
- **Identificador:** CU02
- **Nome:** Executar Cálculo de Imposto
- **Ator Principal:** Aplicação Legada de Mainframe (ou outra aplicação cliente)
- **Descrição:** Uma aplicação cliente invoca o Motor de Cálculo para obter o valor do imposto sobre um investimento específico, fornecendo os dados necessários para a avaliação das regras.
- **Fluxo Principal:**
  1. A aplicação cliente (ex: mainframe) envia uma requisição para a API do Motor de Cálculo com os dados do investimento (valor, tipo, data, etc.).
  2. O Motor de Cálculo recebe a requisição.
  3. O Motor de Cálculo identifica as regras de imposto ativas aplicáveis aos dados fornecidos.
  4. O Motor de Cálculo executa as regras em sequência, realizando os cálculos lógicos e aritméticos.
  5. O Motor de Cálculo retorna o valor total do imposto calculado para a aplicação cliente via API.
- **Fluxos Alternativos / Exceções:**
    * **FA2.1 - Dados de Entrada Inválidos:** Se os dados de entrada forem inválidos ou incompletos, a API retorna um erro indicando o problema.
    * **FA2.2 - Nenhuma Regra Aplicável:** Se nenhuma regra ativa for aplicável aos dados de entrada, o motor retorna 0 ou um valor padrão (a ser definido).
    * **FA2.3 - Erro Interno do Motor:** Se ocorrer um erro durante a execução das regras, o motor registra o erro e retorna uma mensagem de falha para o cliente.

---

## 8. Requisitos de Integração
Integrações com outros sistemas, serviços, APIs, ou bancos de dados, com foco no MVP.

- **Integração com Aplicação Legada de Mainframe:** O Motor de Cálculo deve se integrar com uma aplicação legada de mainframe (a ser definida) via API RESTful, consumindo dados de entrada e fornecendo o resultado do cálculo.
- **Banco de Dados:** O motor precisará de um banco de dados para persistir as regras de negócio, versões, logs de auditoria e configurações. Será utilizada uma solução de banco de dados AWS (RDS ou DynamoDB, a ser definido na Sprint 2).
- **Serviços AWS:** A solução fará uso de serviços AWS para infraestrutura, computação (ex: EC2, Lambda), API Gateway, e monitoramento (CloudWatch).

---

## 9. Restrições Técnicas
Tecnologias obrigatórias, plataformas suportadas, padrões de arquitetura, ou limitações impostas por contexto do projeto.

- **Linguagem e Framework:** O desenvolvimento do motor será em C# utilizando o framework .NET (preferencialmente .NET Core).
- **Plataforma Cloud:** A solução deve ser desenvolvida e implantada na nuvem AWS.
- **Arquitetura:** O motor deve ser implementado como um serviço, preferencialmente seguindo princípios de microserviços ou serverless, para garantir reusabilidade e escalabilidade.
- **Integração com Mainframe:** A integração com o mainframe pode exigir adaptação a formatos de dados específicos ou protocolos de comunicação legados, que serão investigados na Sprint 2.
- **Segurança da Informação:** A solução deve aderir às políticas e padrões de segurança da informação do Banco JUBV.

---

## 10. Critérios de Aceitação Gerais
Critérios objetivos que devem ser atendidos para o sistema ser considerado pronto para entrega do MVP.

- **Conformidade de Cálculo:** O motor de cálculo deve executar as regras corretamente para o cenário de impostos selecionado para a integração inicial, com 100% de precisão nos cálculos em cenários de teste definidos.
- **Autonomia Operacional:** A equipe de operações deve conseguir criar, alterar e desativar regras básicas de impostos através da UI sem a necessidade de intervenção da equipe de desenvolvimento em 90% dos casos de uso previstos para o MVP.
- **Integração Bem-Sucedida:** A integração com a aplicação legada de mainframe selecionada deve estar plenamente funcional e a aplicação deve consumir o serviço do motor de cálculo e retornar os resultados esperados em ambiente de homologação.
- **Performance Aceitável:** O tempo de resposta médio das requisições de cálculo através da API deve estar abaixo do limite estabelecido nos requisitos não funcionais (ex: 50ms).
- **Auditabilidade Completa:** Todas as operações de criação, alteração e desativação de regras devem ser registradas no log de auditoria, com informações completas (usuário, data/hora, tipo de operação, detalhes da mudança).
- **Documentação Concluída:** A documentação técnica e de usuário para o MVP deve estar finalizada e aprovada.

---

## 11. Anexos / Referências
Links, diagramas, documentos externos ou materiais complementares usados na elaboração deste DRS.

- **Documento de Contexto do Projeto "Motor de Cálculo de Regras Tributárias":** `ideation-context.md`
- **Plano do Projeto "Motor de Cálculo de Regras Tributárias - MVP":** `plan-document.md`
- **Business Rules Management System (BRMS) - IBM:** [https://www.ibm.com/think/topics/business-rules-management-system](https://www.ibm.com/think/topics/business-rules-management-system)
- **Business Rule Management System (BRMS) - Wikipedia:** [https://en.wikipedia.org/wiki/Business_rule_management_system](https://en.wikipedia.org/wiki/Business_rule_management_system)
- Documentação interna do Banco JUBV sobre as regras atuais de impostos sobre investimentos (referência).
- Documentação sobre os sistemas legados de mainframe (referência).