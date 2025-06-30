# 🌳 Quality Attribute Utility Tree (ATAM + arc42) – Motor de Cálculo de Regras Tributárias

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

## 🧩 Atributo de Qualidade: `Desempenho`

### 🔸 Subatributo: `Latência de Cálculo`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Uma aplicação cliente (ex: mainframe) envia uma requisição de cálculo de imposto com dados de investimento. | Durante o pico de processamento de transações. | API do Motor de Cálculo, Componente de Execução de Regras | O motor deve processar a requisição e retornar o resultado do cálculo. | Tempo de resposta médio inferior a 50ms para 95% das requisições. | Alta |

### 🔸 Subatributo: `Vazão de Requisições`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Múltiplas aplicações clientes enviam requisições simultaneamente. | Ambiente de produção, sob carga máxima. | API do Motor de Cálculo, Infraestrutura AWS | O motor deve processar todas as requisições sem degradação significativa de performance. | Capacidade de processar X requisições por segundo mantendo a latência. | Alta |

---

## 🧩 Atributo de Qualidade: `Disponibilidade`

### 🔸 Subatributo: `Tempo de Atividade (Uptime)`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Falha de um componente de infraestrutura (ex: instância de servidor, serviço AWS). | Ambiente de produção. | Motor de Cálculo (serviço e infraestrutura) | O serviço deve se recuperar automaticamente ou ter um tempo mínimo de inatividade. | Uptime de 99,9% ou superior. | Alta |

### 🔸 Subatributo: `Tolerância a Falhas`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Erro durante a execução de uma regra ou persistência de dados. | Ambiente de produção. | Componente de Persistência, Componente de Execução de Regras | O sistema deve se recuperar da falha sem perda de dados e registrar o erro. | Número de transações perdidas em caso de falha (deve ser zero). Capacidade de reiniciar o serviço após falha em Y minutos. | Média |

---

## 🧩 Atributo de Qualidade: `Segurança`

### 🔸 Subatributo: `Controle de Acesso`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Tentativa de acesso não autorizado à interface de gerenciamento de regras ou à API. | Interface de usuário, API do Motor de Cálculo | Módulo de Autenticação/Autorização | O sistema deve bloquear o acesso e registrar a tentativa. | Porcentagem de tentativas de acesso não autorizado bloqueadas. | Alta |

### 🔸 Subatributo: `Proteção contra Injeção`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Tentativa de inserção de código malicioso na definição de uma regra. | Interface de gerenciamento de regras (UI), Componente de Persistência de Regras | Componente de Validação de Regras | O sistema deve detectar e impedir a persistência ou execução de código malicioso. | Número de tentativas de injeção detectadas e prevenidas. | Alta |

---

## 🧩 Atributo de Qualidade: `Usabilidade`

### 🔸 Subatributo: `Facilidade de Aprendizado e Operação`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Um novo membro da equipe de operações precisa gerenciar regras. | Ambiente de treinamento ou produção. | Interface de Gerenciamento de Regras (UI) | O usuário deve ser capaz de criar, editar e ativar/desativar regras com mínimo treinamento. | Tempo médio para um novo usuário realizar operações básicas (ex: criar uma regra simples) com sucesso. Resultado de pesquisa de satisfação dos usuários. | Alta |

---

## 🧩 Atributo de Qualidade: `Auditabilidade`

### 🔸 Subatributo: `Rastreabilidade de Alterações`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Um auditor precisa verificar quem alterou uma regra e quando. | Ambiente de produção, sistema de logs. | Módulo de Auditoria, Base de Dados de Versões | O sistema deve fornecer registros completos de todas as operações de gerenciamento de regras. | Capacidade de rastrear todas as alterações de regras e operações, incluindo usuário e timestamp. | Alta |

---

## 🧩 Atributo de Qualidade: `Manutenibilidade`

### 🔸 Subatributo: `Modularidade e Compreensibilidade`

| Estímulo | Ambiente | Artefato Afetado | Resposta Esperada | Medição | Importância |
|---|---|---|---|---|---|
| Um novo desenvolvedor precisa entender o código-fonte para implementar uma nova funcionalidade ou corrigir um bug. | Ambiente de desenvolvimento. | Código-fonte do Motor de Cálculo | O desenvolvedor deve conseguir identificar e modificar o código relevante de forma eficiente. | Tempo médio para um novo desenvolvedor se familiarizar com a base de código e realizar uma alteração simples. | Média |

---

## 📝 Observações

- Um atributo pode conter múltiplos subatributos ou dimensões específicas.
- Os cenários devem ser claros, verificáveis e úteis para apoiar decisões de arquitetura.
- A prioridade auxilia na análise de trade-offs em sessões de avaliação arquitetural (ex: ATAM).
- Este documento será a base para discussões de arquitetura e decisões de design que impactarão diretamente a capacidade do sistema de atender a esses requisitos de qualidade.