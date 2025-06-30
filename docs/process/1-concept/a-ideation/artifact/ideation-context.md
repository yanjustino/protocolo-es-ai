# 📄 Documento de Contexto do Projeto

## 1. Identificação do Projeto
- **Nome do Projeto:** Motor de Cálculo de Regras Tributárias
- **Versão do Documento:** 1.0
- **Autor(es):** Especialista em Análise de Requisitos (Consultor Externo)
- **Data de Criação / Revisão:** 28 de junho de 2025

---

## 2. Visão Geral do Produto
- **Descrição do Produto:** O Motor de Cálculo de Regras Tributárias é um serviço centralizado que proporcionará mecanismos para o registro, gerenciamento e execução de funções lógicas e aritméticas relacionadas a cálculos de impostos sobre investimentos. Ele será projetado para desacoplar as regras de negócio das aplicações legadas do Banco JUBV, permitindo que as equipes de operação tenham autonomia para criar, alterar e desativar regras sem a necessidade de intervenção do time de desenvolvimento ou de novas implantações nas aplicações existentes.
- **Objetivo Principal:** Reduzir a complexidade, os riscos e o tempo de resposta nas atualizações de regras de impostos sobre investimentos, proporcionando agilidade na adaptação às constantes mudanças regulatórias.
- **Problemas que o produto pretende resolver:**
    - Regras de cálculo de impostos "hardcoded" em aplicações legadas (mainframe), exigindo modificações complexas e custosas a cada mudança regulatória.
    - Alto acoplamento entre as regras de negócio e o código-fonte das aplicações, dificultando a manutenção e o reuso.
    - Processo de atualização, teste e implantação demorado e propenso a erros devido à necessidade de múltiplas alterações em sistemas diferentes.
    - Falta de autonomia das equipes de operação para gerenciar as regras de negócio diretamente.
- **Público-alvo:**
    - **Equipe de Operações da Área de Investimentos:** Usuários primários para criação, alteração e desativação das regras.
    - **Equipe de Desenvolvimento de TI:** Responsáveis pela construção e manutenção do motor.
    - **Área de Investimentos do Banco JUBV:** Beneficiários da agilidade e redução de riscos.
    - **Outras áreas do Banco JUBV:** Potenciais usuários em contextos futuros que exijam gerenciamento de regras.

---

## 3. Justificativa
- **Motivação para o projeto:** A constante e urgente alteração nas regras de impostos sobre investimentos, ditadas pelo governo, impõe um desafio significativo ao Banco JUBV. A abordagem atual de incorporar essas regras diretamente no código-fonte de diversas aplicações legadas em mainframe gera um ciclo vicioso de modificações, testes e implantações demoradas e arriscadas. O projeto busca romper com esse ciclo, garantindo conformidade regulatória de forma mais eficiente e segura.
- **Benefícios esperados:**
    - **Agilidade:** Redução drástica do tempo necessário para adaptar os sistemas a novas regulamentações fiscais.
    - **Redução de Riscos:** Diminuição da probabilidade de erros na implementação das regras e de impactos negativos nas operações.
    - **Autonomia Operacional:** Capacitação da equipe de operações para gerenciar as regras de negócio de forma independente.
    - **Reusabilidade:** O motor de cálculo poderá ser reutilizado em diversos contextos dentro da área de investimentos e, potencialmente, em outras áreas do banco, otimizando o investimento em tecnologia.
    - **Manutenção Simplificada:** Desacoplamento das regras das aplicações legadas, facilitando a manutenção e evolução dos sistemas.
- **Cenários de uso:**
    - **Atualização de Alíquotas de Imposto:** Uma nova alíquota de IR sobre determinado tipo de investimento é anunciada; a equipe de operações atualiza a regra no motor, e todas as aplicações que o utilizam refletem a mudança imediatamente.
    - **Criação de Novas Regras de Isenção:** O governo cria uma nova regra de isenção fiscal para pequenos investidores; a equipe de operações modela e insere a nova regra no motor.
    - **Simulação de Cálculos:** Antes de uma regra ser ativada, a equipe de operações pode testar e simular seu impacto nos cálculos sem afetar o ambiente de produção.
    - **Auditoria e Rastreabilidade:** O motor registrará as alterações das regras, facilitando auditorias e garantindo a rastreabilidade das decisões de cálculo.

---

## 4. Escopo Inicial
- **Itens incluídos no escopo:**
    - Desenvolvimento do serviço de Motor de Cálculo de Regras Tributárias, incluindo mecanismos de registro, gerenciamento e execução de regras.
    - Interface de usuário (UI) para a equipe de operações realizar o gerenciamento (criação, edição, exclusão, ativação/desativação) das regras.
    - Integração inicial com uma das aplicações legadas de mainframe (a ser definida com base na criticidade e complexidade).
    - Mecanismo de versionamento das regras.
    - Funcionalidades básicas de auditoria e log das alterações das regras.
    - Documentação técnica e de usuário para o motor.
- **Itens fora do escopo (exclusões):**
    - Migração completa de todas as aplicações legadas do mainframe.
    - Refatoração ou reescrita de todas as regras de impostos existentes em todas as aplicações legadas.
    - Integração inicial com todas as aplicações legadas existentes (será uma integração faseada).
    - Desenvolvimento de um sistema de workflow complexo para aprovação de regras (será considerado em fases futuras, se necessário).

---

## 5. Requisitos Iniciais
- **Requisitos Funcionais (alto nível):**
    - O motor deve permitir a criação de novas regras, especificando condições e ações de cálculo.
    - O motor deve permitir a edição de regras existentes, com controle de versão.
    - O motor deve permitir a desativação e ativação de regras.
    - O motor deve ser capaz de executar as regras com base em dados de entrada fornecidos pelas aplicações clientes.
    - O motor deve fornecer uma API RESTful para integração com outras aplicações.
    - A interface de gerenciamento das regras deve ser intuitiva para usuários de negócio.
    - O motor deve registrar todas as operações de criação, alteração e desativação de regras, incluindo usuário e timestamp.
- **Requisitos Não-Funcionais:**
    - **Desempenho:** O motor deve ser capaz de processar um alto volume de requisições de cálculo com baixa latência (ex: tempo de resposta médio inferior a X ms).
    - **Escalabilidade:** A solução deve ser escalável horizontalmente para suportar picos de demanda.
    - **Disponibilidade:** Alta disponibilidade (ex: 99,9% ou superior).
    - **Segurança:** Acesso seguro e autenticado à interface de gerenciamento e à API. Proteção contra injeção de código nas regras.
    - **Auditabilidade:** Capacidade de rastrear todas as alterações nas regras e as execuções de cálculo.
    - **Tolerância a Falhas:** Capacidade de se recuperar de falhas sem perda de dados ou interrupção significativa do serviço.
    - **Usabilidade:** A interface para gerenciamento de regras deve ser fácil de usar e compreender pela equipe de operações.

---

## 6. Premissas
- **Tecnologias previstas ou preferidas:**
    - Linguagem de Programação: C#
    - Framework: .NET (Core preferencialmente, devido à flexibilidade e compatibilidade com AWS)
    - Serviços em Nuvem: AWS (Amazon Web Services) para infraestrutura, computação, banco de dados e outros serviços necessários.
- **Ambiente de execução:** Cloud AWS.
- **Disponibilidade de recursos:** Equipe de desenvolvimento de TI com conhecimento em C#, .NET e AWS disponível para o projeto. Disponibilidade da equipe de operações para colaborar na definição e validação das regras.

---

## 7. Restrições
- **Limitações técnicas ou operacionais:**
    - A integração inicial com sistemas legados em mainframe pode apresentar desafios devido à tecnologia e arquitetura antigas.
    - A necessidade de garantir a integridade e consistência dos cálculos entre o motor e as aplicações legadas existentes durante a transição.
    - Complexidade na modelagem de regras tributárias altamente específicas e aninhadas.
- **Dependências externas ou obrigatórias:**
    - Colaboração ativa e contínua da equipe de operações para a definição e validação das regras de negócio.
    - Suporte da equipe de infraestrutura para provisionamento e configuração dos serviços AWS.
    - Acesso à documentação e especialistas nos sistemas legados do mainframe para a integração.

---

## 8. Stakeholders
- **Principais interessados no projeto e seus papéis:**
    - **Patrocinador do Projeto (Gerência da Área de Investimentos):** Define a visão estratégica e aloca recursos.
    - **Gerente de Projeto (TI):** Responsável pela gestão do projeto e garantia da entrega.
    - **Líder Técnico (TI):** Responsável pela arquitetura e direção técnica do desenvolvimento.
    - **Equipe de Desenvolvimento (TI):** Desenvolvedores do motor de cálculo.
    - **Equipe de Operações da Área de Investimentos:** Futuros usuários do motor, responsáveis pela criação e gerenciamento das regras.
    - **Analistas de Negócio (Área de Investimentos):** Apoiam na elicitação e validação das regras de negócio.
    - **Área Jurídica/Regulatória:** Valida a conformidade das regras implementadas.
    - **Segurança da Informação:** Garante que a solução atenda aos padrões de segurança do banco.

---

## 9. Critérios de Sucesso
- **Critérios objetivos para considerar o projeto bem-sucedido:**
    - Redução de X% no tempo médio de adaptação a novas regras de imposto.
    - Capacidade da equipe de operações de criar e alterar regras de impostos sem intervenção da equipe de desenvolvimento em Y% dos casos.
    - Implementação bem-sucedida da integração com pelo menos uma aplicação legada de mainframe.
    - Motor de cálculo em produção com alta disponibilidade (acima de 99,9%).
    - Feedback positivo da equipe de operações sobre a usabilidade da interface de gerenciamento de regras.
- **Indicadores ou métricas de avaliação:**
    - Tempo médio de implementação de uma nova regra.
    - Número de solicitações de alteração de regras que exigem modificação de código-fonte.
    - Uptime do serviço do motor de cálculo.
    - Pesquisas de satisfação dos usuários (equipe de operações).
    - Taxa de reuso do motor por outras aplicações.

---

## 10. Riscos Iniciais
- **Riscos técnicos, operacionais ou de negócio identificados:**
    - **Risco:** Complexidade elevada na extração e modelagem das regras de negócio dos sistemas legados.
        - **Impacto:** Atrasos no projeto e regras implementadas incorretamente.
        - **Mitigação:** Dedicar analistas de negócio experientes, realizar workshops com especialistas de negócio, usar ferramentas de extração se aplicável.
    - **Risco:** Dificuldade na integração com os sistemas legados de mainframe.
        - **Impacto:** Atrasos, custos adicionais, falhas na comunicação entre sistemas.
        - **Mitigação:** Engajamento precoce de especialistas em mainframe, prototipagem da integração, uso de tecnologias de integração robustas.
    - **Risco:** Resistência à mudança por parte das equipes (desenvolvimento ou operações).
        - **Impacto:** Dificuldade na adoção da nova ferramenta, subutilização dos benefícios.
        - **Mitigação:** Engajamento ativo dos stakeholders desde o início, treinamentos, comunicação clara dos benefícios.
    - **Risco:** Incompatibilidade ou limitações das tecnologias escolhidas (AWS, .NET C#) para certas regras complexas.
        - **Impacto:** Reengenharia de partes do motor, atrasos.
        - **Mitigação:** Análise aprofundada de prova de conceito para cenários de regras mais complexos.
- **Impacto e possíveis planos de mitigação:** (Detalhado acima para cada risco)

---

## 11. Referências
- **Fontes de pesquisa, materiais de apoio ou documentação relacionada:**
    - Business Rules Management System (BRMS) - IBM: [https://www.ibm.com/think/topics/business-rules-management-system](https://www.ibm.com/think/topics/business-rules-management-system)
    - Business Rule Management System (BRMS) - Wikipedia: [https://en.wikipedia.org/wiki/Business_rule_management_system](https://en.wikipedia.org/wiki/Business_rule_management_system)
    - Documentação interna do Banco JUBV sobre as regras atuais de impostos sobre investimentos.
    - Documentação sobre os sistemas legados de mainframe.

---

Este documento serve como a base para o entendimento inicial do projeto. A medida que avançarmos, os detalhes serão refinados e novos requisitos podem surgir. Estamos prontos para iniciar as próximas etapas de elicitação e detalhamento.

Há algo mais que você gostaria de adicionar ou esclarecer neste documento de contexto?