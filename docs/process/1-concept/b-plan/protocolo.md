# 📌 Protocolo de Adoção de LLMs – Fase: PLAN
Etapa dedicada à organização estruturada do projeto, na qual se definem os principais elementos que irão guiar a execução: escopo, recursos, prazos, entregas e responsabilidades. O objetivo é transformar a ideia conceitual (gerada na ideação) em um plano viável e rastreável, com previsibilidade e alinhamento entre os envolvidos.

## 🎯 Objetivo

Converter a ideia conceitual da etapa de ideação em um plano estruturado, viável e rastreável. A LLM auxilia na organização do escopo, definição de recursos, cronograma, entregas, papéis e riscos, promovendo previsibilidade e alinhamento entre stakeholders.

---

## 📘 Atividades e Interações com LLMs

| Atividade                        | Uso da LLM                                                                   | Artefato(s)                   | Avaliação Qualitativa                                               | Avaliação Quantitativa                          |
|----------------------------------|------------------------------------------------------------------------------|-------------------------------|---------------------------------------------------------------------|--------------------------------------------------|
| Definir escopo inicial           | Sugestão de funcionalidades para o MVP com base no documento de contexto     | Plano do projeto `(prompt A)` | Aderência do escopo aos objetivos estratégicos do projeto          | Nº de funcionalidades aceitas; tempo de elaboração |
| Alocar recursos                  | Recomendar perfis, ferramentas e infraestrutura com base no contexto         | Plano do projeto `(prompt A)` | Adequação das recomendações às restrições e realidade do projeto   | Nº de ajustes necessários após proposta inicial   |
| Estimar cronograma e entregas    | Gerar cronograma de 90 dias com 6 iterações de 15 dias e entregas associadas | Plano do projeto `(prompt A)` | Clareza na definição de entregas por iteração                      | Nº de entregas válidas; tempo de revisão          |
| Mapear riscos e restrições       | Sugerir riscos com base em projetos similares e plano de mitigação           | Plano do projeto `(prompt A)` | Relevância dos riscos propostos                                     | Nº de riscos reutilizados ou aproveitados         |
| Sugerir cerimônias e rituais     | Propor cerimônias compatíveis com ágil e DevOps                              | Plano do projeto `(prompt A)` | Clareza e utilidade das cerimônias para alinhamento                | Frequência e aderência das reuniões planejadas     |
| Gerar documento de plano         | Consolidar todos os itens em um template padrão em Markdown                  | Plano do projeto `(prompt A)` | Coesão, estrutura e completude do plano                            | Nº de revisões do plano; tempo de geração total    |

---

## 📂 Artefatos Modelos
- [Plano](./artifact/plan-document.md)
  - Cronograma estruturado com entregas e rituais por iteração
  - Tabela de riscos e plano de mitigação
  - Lista de recursos humanos, técnicos e financeiros

## 🧠 Exemplos de Uso de LLMs

- **LLMs (ChatGPT ou Gemini)**:
  - Compreensão do documento de contexto e geração do plano
  - Sugestão de escopo, recursos, riscos, restrições
  - Construção automatizada de cronogramas em Markdown

- **RAG (Retrieval-Augmented Generation)**:
  - Uso de cells para entrada do documento de contexto e saída do plano
  - Comparações entre versões de plano ao longo do tempo


## 📊 Indicadores de Avaliação

### Qualitativos
- Clareza e realismo das entregas planejadas
- Cobertura adequada dos riscos e restrições
- Consistência entre escopo, recursos e cronograma
- Feedback de stakeholders sobre o plano gerado

### Quantitativos
- Tempo médio de geração do plano com LLM
- Taxa de aceitação das sugestões de escopo, riscos e equipe
- Nº de ciclos de revisão do plano
- Nº de riscos planejados vs. riscos reais ocorridos


## 🔗 Prompts

- [Prompt A - Prompt para geração do plano de projeto](./prompts.md)


## 🛠️ Instrumentação Recomendada

- Registro de prompts e outputs
- Log das interações com LLMs (aceitação/rejeição de sugestões)
- Controle de versão dos artefatos (ex: Git)
- Registro de tempo por atividade

