# 💡 PLAN
Etapa dedicada à organização estruturada do projeto, na qual se definem os principais elementos que irão guiar a execução: escopo, recursos, prazos, entregas e responsabilidades. O objetivo é transformar a ideia conceitual (gerada na ideação) em um plano viável e rastreável, com previsibilidade e alinhamento entre os envolvidos.

## 📘 Atividades 
| Atividade                          | Artefatos                                                                                     | Execução            |
|------------------------------------|-----------------------------------------------------------------------------------------------|---------------------|
| Definição do escopo inicial        | Levantamento e alocação de recursos (equipe, ferramentas, infraestrutura) <br> Estimativas de esforço e cronograma de entregas <br> Identificação de dependências e restrições <br> Mapeamento de riscos e plano de mitigação <br> Alinhamento com stakeholders e validação do plano | 🧑🏽🧠 Humano com suporte de IA |

## 🧰 Ferramentas
- LLMs
    - ChatGpt o3 | Gemini 2.5 Pro

## 📄 Artefatos

- [Plano](./plan-document.md)

## 🔗 Anexos

### Prompt para geração do plano de projeto
````xml
<context>
    Você irá atuar como um especialista em projetos de software com enfase elaboração e análise de requisitos. Seu papel é auxiliar na geração de um planejamento para guiar a execução do projeto. Com base no {{DOCUMENTO}} de contexto em <attachement>, defina o escopo inicial do projeto. Além disso sugira, ferramentas, equipe e infraestrutura necessária. Siga as instruções defenido em <instructions>. Dado que este é um planajemento inical antes da análise dos requisitos, só planeje as macro-atividades e seus potênciais entregáveis. Planeje conforme o contexto no {{DOCUMENTO}} anexado. Ao construir o plano, fique atento as dependências e restrições; mapeie os riscos e como mitiga-los. 
<context>

<attachement>
  - ideation-context.md
</attachement>

<instructions>
  1. Defina um escopo para um MVP.
  2. Defina apenas features e não stories.
  3. Defina um cronograma de 90 dias.
  4. Sugira iterações de 15 dias.
  5. Inclua cerimônias de alinhamento com os stakeholders.
  6. Cada iteração deve conter uma uma entrega, não necessariamente software.
  7. Gere um documento de plano no formato markdown seguindo o <template>.
</instructions>

<template>
# 📘 Plano do Projeto

## 1. Identificação do Projeto
- **Nome do Projeto:** 
- **Versão do Documento:** 
- **Autor(es):** 
- **Data de Criação / Revisão:** 

---

## 2. Objetivo do Plano
Descreve o propósito geral do plano, os objetivos principais do projeto, e os resultados esperados, incluindo o escopo de atuação e metas iniciais.

---

## 3. Escopo do Projeto

### Entregas previstas (MVP ou Iteração Inicial):
- [ ] **Funcionalidade 1:** 
- [ ] **Funcionalidade 2:** 
- [ ] **Integrações previstas:** 
- [ ] **Componentes auxiliares:** 
- [ ] **Documentação essencial:** 

### Limites e exclusões:
- [ ] Itens fora do escopo neste momento:
  - Ex: Integração com múltiplos sistemas legados
  - Ex: Funcionalidades avançadas não essenciais para o MVP

### Critérios de aceitação:
- [ ] O sistema deve funcionar corretamente para os principais casos de uso.
- [ ] Usuários-chave devem operar a solução sem apoio técnico.
- [ ] Integrações funcionais e testadas com sistemas existentes.
- [ ] Documentação básica entregue e validada.
- [ ] Disponibilidade mínima de operação definida.

---

## 4. Cronograma (Exemplo: 90 dias com 6 Iterações)

| Iteração | Duração | Responsável | Entregável da Iteração | Cerimônias de Alinhamento |
|----------|---------|-------------|-------------------------|----------------------------|
| Iteração 1: Nome                        | xx dias | [Responsável] | [Resultado esperado]                 | [Kick-off, review etc.]       |
| Iteração 2: Nome                        | xx dias | [Responsável] | [Resultado esperado]                 |                                |
| Iteração 3: Nome                        | xx dias | [Responsável] | [Resultado esperado]                 |                                |
| Iteração 4: Nome                        | xx dias | [Responsável] | [Resultado esperado]                 |                                |
| Iteração 5: Nome                        | xx dias | [Responsável] | [Resultado esperado]                 |                                |
| Iteração 6: Nome                        | xx dias | [Responsável] | [Resultado esperado]                 |                                |
| Implantação do MVP                      | x dias  | [Equipe]      | Sistema entregue                     | Reunião pós-implantação        |

---

## 5. Equipe e Papéis

| Nome                | Papel                | Responsabilidades principais                                  |
|---------------------|----------------------|---------------------------------------------------------------|
| (A ser definido)    | Gerente de Projeto   | Planejamento, cronograma, comunicação, gestão de riscos       |
| (A ser definido)    | Líder Técnico        | Arquitetura, tecnologia, diretrizes técnicas, revisão de código|
| (A ser definido)    | Analista de Requisitos | Levantamento, análise e validação com stakeholders            |
| (A ser definido)    | Desenvolvedor(es)    | Implementação técnica das soluções                            |
| (A ser definido)    | QA / Testador        | Garantia de qualidade, planos de teste, validação funcional   |
| (A ser definido)    | Especialista(s)      | Apoio técnico especializado, integração com sistemas externos |

---

## 6. Recursos Necessários

### Tecnológicos
- Linguagens e frameworks: 
- Ferramentas de desenvolvimento:
- Infraestrutura (cloud, servidores, APIs, etc.):
- Ferramentas de testes:
- Outras dependências técnicas:

### Humanos
- Equipe base:
  - [ ] Gerente de Projeto
  - [ ] Desenvolvedores
  - [ ] QA/Testador
  - [ ] Especialistas específicos

### Financeiros
- Orçamento estimado
- Licenças de software (se aplicável)
- Infraestrutura (consumo, serviços)

---

## 7. Riscos e Mitigações

| Risco Identificado                              | Impacto | Probabilidade | Plano de Mitigação                                     |
|--------------------------------------------------|---------|----------------|--------------------------------------------------------|
| [Descrever o risco]                              | Alto    | Média          | [Plano para mitigar ou reduzir o risco]                |
|                                                  |         |                |                                                        |

---

## 8. Comunicação

- **Canais utilizados:**
  - E-mail, Slack, Teams, etc.
  - Ferramentas de acompanhamento: Jira, Trello, etc.
  - Repositório de documentação: Confluence, SharePoint

- **Frequência de atualizações:**
  - Daily Scrums
  - Review de Iterações
  - Reuniões quinzenais com liderança
  - Demonstrações periódicas

- **Responsável pela comunicação com stakeholders:**
  - [Nome do responsável principal]

---

## 9. Aprovação

| Nome                | Papel                          | Assinatura (se necessário) |
|---------------------|---------------------------------|-----------------------------|
| (A ser definido)    | Patrocinador do Projeto         |                             |
| (A ser definido)    | Gerente Executivo de TI         |                             |
| (A ser definido)    | Gestor de Área / Produto        |                             |

---

## 10. Referências

- [Referência 1 ou link externo relevante]
- [Documentos relacionados: contexto, requisitos, etc.]</template>
````


## Referências
- [Prompt engineering overview](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
