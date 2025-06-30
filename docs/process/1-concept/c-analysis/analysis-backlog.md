# 📋 Backlog de Produto

Backlog com histórias de usuário priorizadas para orientar o desenvolvimento do produto.

-----

## 📌 Legenda das Colunas

  - **ID**: Código identificador da história (ex: US01)
  - **História do Usuário**: Desejo descrito do ponto de vista do usuário
  - **Prioridade**: Alta / Média / Baixa
  - **Critérios de Aceitação**: Condições mínimas para considerar a história entregue
  - **Status**: A Fazer / Em Progresso / Concluído / Em Validação

-----

## 📦 Backlog

| ID | História do Usuário | Prioridade | Critérios de Aceitação | Status |
|---|---|---|---|---|
| US01 | Como equipe de operações, quero criar novas regras de cálculo de imposto para adaptar o sistema a novas regulamentações fiscais rapidamente. | Alta | - O sistema deve apresentar um formulário com campos para nome, descrição, condições e ações de cálculo da regra.\<br\> - A regra deve ser persistida após o salvamento.\<br\> - A regra recém-criada deve aparecer na lista de regras ativas, com a opção de ser ativada ou desativada.\<br\> - O sistema deve validar os dados de entrada e exibir mensagens de erro claras em caso de dados inválidos. | A Fazer |
| US02 | Como equipe de operações, quero editar regras de cálculo de imposto existentes para corrigir erros ou ajustar as condições e ações de cálculo. | Alta | - O sistema deve permitir selecionar uma regra existente e carregar seus detalhes em um formulário de edição.\<br\> - As modificações na regra devem ser salvas como uma nova versão, mantendo o histórico.\<br\> - O sistema deve registrar o usuário e o timestamp da edição.\<br\> - O sistema deve validar os dados de entrada e exibir mensagens de erro claras em caso de dados inválidos. | A Fazer |
| US03 | Como equipe de operações, quero ativar ou desativar regras de cálculo de imposto para controlar quais regras estão em uso no sistema a qualquer momento. | Alta | - O sistema deve permitir alternar o status de ativação/desativação de uma regra via UI.\<br\> - Regras desativadas não devem ser consideradas nos cálculos de imposto.\<br\> - O sistema deve registrar o usuário e o timestamp da alteração de status. | A Fazer |
| US04 | Como uma aplicação legada de mainframe, quero invocar o motor de cálculo de regras para obter o valor do imposto sobre um investimento. | Alta | - A API RESTful do motor de cálculo deve estar disponível e responder a requisições.\<br\> - A aplicação cliente deve ser capaz de enviar dados de entrada (valor, tipo, data, etc.) para a API.\<br\> - A API deve retornar o valor correto do imposto calculado com base nas regras ativas.\<br\> - Em caso de dados de entrada inválidos, a API deve retornar um erro claro.\<br\> - Em caso de erro interno, a API deve retornar uma mensagem de falha e registrar o erro. | A Fazer |
| US05 | Como equipe de operações, quero visualizar o histórico de versões de uma regra para auditoria e rastreabilidade das mudanças. | Média | - Ao selecionar uma regra, o sistema deve exibir uma lista de todas as suas versões anteriores, incluindo data/hora da modificação e usuário.\<br\> - Deve ser possível visualizar os detalhes de cada versão da regra. | A Fazer |
| US06 | Como equipe de operações, quero consultar as regras cadastradas para encontrar e revisar informações de regras específicas. | Média | - A interface deve apresentar uma lista de todas as regras cadastradas.\<br\> - Deve ser possível filtrar e buscar regras por nome, status ou outros critérios relevantes.\<br\> - A visualização deve ser clara e de fácil leitura. | A Fazer |
| US07 | Como um auditor, quero acessar logs de auditoria das operações de gerenciamento de regras para garantir a conformidade e rastreabilidade das decisões de cálculo. | Alta | - O sistema deve registrar todas as operações de criação, alteração e desativação de regras.\<br\> - Os logs devem incluir o usuário responsável, timestamp e detalhes da operação.\<br\> - Os logs devem ser persistentes e acessíveis para consulta (formato a ser definido). | A Fazer |

-----

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

-----

## 🔄 Observações Gerais

  - As histórias devem ser compreensíveis para todos os stakeholders.
  - Critérios de aceitação ajudam no alinhamento entre desenvolvimento e testes.
  - O backlog é vivo: pode (e deve) ser ajustado conforme evolução do projeto.
  - Esta é a versão inicial do backlog para o MVP e será refinada nas próximas sprints.