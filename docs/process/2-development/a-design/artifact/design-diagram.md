# 🏗️ Arquitetura C4 - Motor de Cálculo de Regras Tributárias

## 📋 Visão Geral

Este documento apresenta a arquitetura completa do Motor de Cálculo de Regras Tributárias utilizando o modelo C4, seguindo as especificações dos requisitos funcionais e não funcionais definidos para o MVP.

---

## 🎯 Decisões Arquiteturais

### 🏛️ Padrão Arquitetural: Monolito Modular
- **Justificativa**: Evitar complexidade inicial conforme solicitado pela equipe
- **Benefícios**: Facilita desenvolvimento, teste e deploy inicial
- **Evolução**: Pode ser refatorado para microserviços no futuro

### 🛠️ Stack Tecnológica
- **Backend**: .NET 9/C# (especialização da equipe)
- **Frontend**: .NET 9 MVC (simplicidade e integração)
- **Database**: PostgreSQL/RDS (robustez e recursos avançados)
- **Cloud**: AWS (requisito do projeto)

### 🔧 Padrões de Design
- **Clean Architecture**: Separação clara de responsabilidades
- **Repository Pattern**: Abstração de acesso a dados
- **Dependency Injection**: Inversão de controle
- **CQRS**: Separação de comandos e consultas (para evolução futura)

---

## 📊 Diagramas C4

### 1. System Context Diagram
**Arquivo**: `c4-system-context.md`

**Foco**: Interações do sistema com usuários e sistemas externos
- Equipe de Operações (usuários primários)
- Aplicação Legada Mainframe (sistema cliente)
- Infraestrutura AWS (plataforma)

### 2. Container Diagram
**Arquivo**: `c4-container-diagram.md`

**Foco**: Containers principais e suas responsabilidades
- Web Application (.NET 9 MVC)
- API Gateway (.NET 9 Web API)
- Rule Engine (.NET 9 Library)
- Authentication Service (.NET 9 Library)
- Audit Service (.NET 9 Library)
- Database (PostgreSQL/RDS)

### 3. Component Diagram
**Arquivo**: `c4-component-diagram.md`

**Foco**: Componentes internos dos containers principais
- API Gateway: Controllers, Validators, Middleware
- Rule Engine: Parser, Evaluator, Executor, Orchestrator

---

## 🔗 Fluxos Principais

### 1. Gerenciamento de Regras
```
Usuário → Web App → API Gateway → Authentication → Audit → Database
```

### 2. Execução de Cálculos
```
Mainframe → API Gateway → Rule Engine → Database → Audit → Response
```

---

## 🎯 Atributos de Qualidade Atendidos

### ⚡ Performance
- **Latência**: < 50ms para 95% das requisições
- **Cache**: Regras compiladas em memória
- **Otimização**: Expression Engine otimizado

### 🔒 Segurança
- **Autenticação**: Service dedicado
- **Autorização**: Controle de acesso por operação
- **Auditoria**: Logging completo de todas as operações

### 📈 Escalabilidade
- **Horizontal**: Containers podem ser replicados
- **Vertical**: Recursos podem ser aumentados
- **Cache**: Reduz carga no database

### 🛡️ Disponibilidade
- **Uptime**: 99.9% (requisito atendido)
- **Tolerância a Falhas**: Recuperação automática
- **Backup**: Estratégias de backup e recovery

### 🔍 Auditabilidade
- **Rastreabilidade**: Logs completos de todas as operações
- **Versionamento**: Histórico de alterações nas regras
- **Relatórios**: Geração de relatórios de auditoria

---

## 🏗️ Estrutura de Projeto Recomendada

```
MotorCalculoRegras/
├── src/
│   ├── MotorCalculoRegras.API/           # API Gateway
│   ├── MotorCalculoRegras.Web/           # Web Application
│   ├── MotorCalculoRegras.Engine/        # Rule Engine
│   ├── MotorCalculoRegras.Auth/          # Authentication Service
│   ├── MotorCalculoRegras.Audit/         # Audit Service
│   └── MotorCalculoRegras.Shared/        # Shared Libraries
├── tests/
│   ├── MotorCalculoRegras.API.Tests/
│   ├── MotorCalculoRegras.Engine.Tests/
│   └── MotorCalculoRegras.Integration.Tests/
├── docs/
│   └── architecture/
└── infrastructure/
    └── aws/
```

---

## 🔧 Tecnologias e Ferramentas

### Backend
- **.NET 9**: Framework principal
- **Entity Framework Core**: ORM para acesso a dados
- **AutoMapper**: Mapeamento de objetos
- **FluentValidation**: Validação de dados
- **Serilog**: Logging estruturado

### Frontend
- **ASP.NET Core MVC**: Framework web
- **Bootstrap**: UI framework
- **jQuery**: Manipulação DOM
- **DataTables**: Tabelas interativas

### Database
- **PostgreSQL**: SGBD principal
- **Entity Framework Core**: Migrations
- **Dapper**: Micro-ORM para queries complexas

### AWS
- **RDS**: Database gerenciado
- **EC2**: Instâncias de aplicação
- **Load Balancer**: Distribuição de carga
- **CloudWatch**: Monitoramento
- **S3**: Armazenamento de logs

---

## 🚀 Estratégia de Deploy

### Ambiente de Desenvolvimento
- Docker Compose para serviços locais
- Database local (SQLite/PostgreSQL)
- Hot reload para desenvolvimento

### Ambiente de Homologação
- AWS com configuração similar à produção
- Dados de teste
- Monitoramento básico

### Ambiente de Produção
- AWS com alta disponibilidade
- Load balancer
- Monitoramento completo
- Backup automático

---

## 📈 Roadmap de Evolução

### Fase 1: MVP (Atual)
- Monolito modular funcional
- Interface básica de gerenciamento
- API REST para integração
- Auditoria completa

### Fase 2: Melhorias
- Interface avançada com drag-and-drop
- Dashboard de métricas
- Relatórios avançados
- Performance otimizada

### Fase 3: Microserviços
- Decomposição em microserviços
- API Gateway dedicado
- Event-driven architecture
- Escalabilidade horizontal

---

## 🎯 Próximos Passos

1. **Implementação**: Desenvolver baseado nos diagramas C4
2. **Testes**: Criar testes unitários e de integração
3. **Infraestrutura**: Configurar ambiente AWS
4. **Deploy**: Pipeline de CI/CD
5. **Monitoramento**: Configurar observabilidade

---

## 📚 Referências

- [C4 Model](https://c4model.com/)
- [C4-PlantUML](https://github.com/plantuml-stdlib/C4-PlantUML)
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [.NET 9 Documentation](https://docs.microsoft.com/en-us/dotnet/core/)
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/) 