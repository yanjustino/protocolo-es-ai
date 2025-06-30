O cenário do Banco JUBV, com suas **aplicações legadas em mainframe e regras de cálculo de impostos embutidas no código-fonte**, que precisam ser alteradas e testadas frequentemente devido a **mudanças regulatórias**, aponta para diversos problemas clássicos de engenharia de software e soluções modernas.

---

## Tópicos e Categorias de Problemas

O problema central do Banco JUBV pode ser categorizado nos seguintes tópicos, com foco nas dificuldades enfrentadas:

* **Manutenção de Sistemas Legados (Legacy System Maintenance):** A dificuldade de modificar e testar aplicações em mainframe é um desafio comum.
* **Acoplamento Forte e Monolitos (Tight Coupling & Monoliths):** As regras de negócio estarem "hardcoded" no código-fonte das aplicações representa um alto acoplamento, dificultando a separação e a reutilização da lógica de cálculo de impostos.
* **Agilidade e Tempo de Resposta (Agility & Time-to-Market):** A frequência e urgência das mudanças regulatórias colidem com a complexidade e o tempo necessários para as alterações nos sistemas legados.
* **Riscos de Mudança e Qualidade (Change Risks & Quality):** Mudar várias aplicações simultaneamente aumenta o risco de introduzir erros e a complexidade dos testes.
* **Conformidade Regulatória (Regulatory Compliance):** A necessidade constante de adaptação a novas regras fiscais é um desafio fundamental para instituições financeiras.
* **Gerenciamento de Regras de Negócio (Business Rule Management):** A falta de um mecanismo para gerenciar e externalizar as regras de negócio de forma centralizada e dinâmica.

---

## Referências

Abaixo estão algumas referências relevantes que abordam os problemas e potenciais soluções para o cenário do Banco JUBV, seguindo os critérios de inclusão e exclusão:

# Referências
- Legacy Software Modernization: A Guide to Unlocking Scalability | Baytech Consulting (2025) | Legacy Software Modernization: A Guide to Unlocking Scalability ([https://www.baytechconsulting.com/blog/legacy-software-modernization-a-guide-to-unlocking-scalability](https://www.baytechconsulting.com/blog/legacy-software-modernization-a-guide-to-unlocking-scalability))
- Navigating Tax Law Changes with Global Tax Compliance Software | Global People Strategist (2025) | Navigating Tax Law Changes with Global Tax Compliance Software ([https://globalpeoplestrategist.com/navigating-tax-law-changes-with-global-tax-compliance-software/](https://globalpeoplestrategist.com/navigating-tax-law-changes-with-global-tax-compliance-software/))
- Business rules extraction for mainframe applications | Infosys (N/A) | Business rules extraction for mainframe applications ([https://www.infosys.com/modernization/documents/business-rules-extraction.pdf](https://www.infosys.com/modernization/documents/business-rules-extraction.pdf))
- Optimising regulatory change management with FinregE | FinregE (N/A) | Regulatory Change Management Software | FinregE ([https://finreg-e.com/optimising-regulatory-change-management/](https://finreg-e.com/optimising-regulatory-change-management/))
- The Role of Microservices in Modernizing Core Banking Systems | DataVSN (2025) | The Role of Microservices in Modernizing Core Banking Systems ([https://www.datavsn.com/the-role-of-microservices-in-modernizing-core-banking-systems/](https://www.datavsn.com/the-role-of-microservices-in-modernizing-core-banking-systems/))
- Best Business Rules Management Solutions for 2025 | PeerSpot (2025) | Best Business Rules Management Solutions for 2025 ([https://www.peerspot.com/categories/business-rules-management](https://www.peerspot.com/categories/business-rules-management))
- Event-Driven Architecture: How Enterprises Manage Billions of Events | Ahamed Safnaj (2025) | Event-Driven Architecture: How Enterprises Manage Billions of Events | by Ahamed Safnaj | Sysco LABS Sri Lanka | Medium ([https://medium.com/sysco-labs/event-driven-architecture-how-enterprises-manage-billions-of-events-b21646384528](https://medium.com/sysco-labs/event-driven-architecture-how-enterprises-manage-billions-of-events-b21646384528))

Essas referências abordam desde a modernização de sistemas legados e a extração de regras de negócio de mainframes, até a aplicação de sistemas de gerenciamento de regras de negócio (BRMS), microserviços e arquiteturas orientadas a eventos para lidar com a dinamicidade das regulamentações. O ideal seria explorar a **externalização das regras de negócio**, possivelmente para um **Sistema de Gerenciamento de Regras de Negócio (BRMS)**, que permitiria que as regras de impostos fossem configuradas e atualizadas sem a necessidade de modificar e reimplantar o código-fonte das aplicações. Além disso, a adoção de uma arquitetura baseada em **microserviços** ou **event-driven** para as novas funcionalidades ou para a refatoração das existentes poderia isolar as regras de cálculo, facilitando futuras alterações.

Qual dessas abordagens você gostaria de explorar mais a fundo?