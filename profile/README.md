# DataCorb - Plataforma Corporativa

## 🏢 Visão Geral da Empresa

A DataCorb é uma empresa especializada em soluções de gestão empresarial, oferecendo uma plataforma completa que permite aos clientes gerenciar seus negócios de forma eficiente e integrada.

## 🏗️ Arquitetura do Sistema

### Estrutura Geral
```
DataCorb Platform
├── License Management Server (Central)
├── Client Nodes (Distributed)
│   ├── Frontend (Flutter Web)
│   ├── Backend (Node.js)
│   └── Docker Compose Services
└── Shared Services
```

## 🔐 Sistema de Gerenciamento de Licenças

### Servidor Central de Licenças
- **Localização**: Servidor central da DataCorb
- **Função**: Controla acesso de todos os clientes ao sistema
- **Tecnologias**: Node.js, MySQL
- **Funcionalidades**:
  - Validação de licenças em tempo real
  - Controle de acesso por cliente
  - Gestão de planos e recursos
  - Monitoramento de uso

### Fluxo de Autenticação
1. Cliente acessa seu nó
2. Frontend solicita validação ao servidor de licenças
3. Servidor valida licença e retorna permissões
4. Frontend carrega recursos baseado nas permissões

## 🎯 Estrutura de Nós por Cliente

### Cada Cliente Possui:
- **Nó Dedicado**: Ambiente isolado para cada cliente
- **Frontend Flutter**: Interface web responsiva
- **Backend Node.js**: API RESTful personalizada
- **Docker Compose**: Orquestração de serviços

### Estrutura de um Nó
```
cliente-xyz/
├── frontend/          # Aplicação Flutter Web
├── backend/           # API Node.js
├── docker-compose.yml # Orquestração de serviços
├── nginx/            # Proxy reverso
└── database/         # Banco de dados isolado
```

## 🚀 Tecnologias Utilizadas

### Frontend (Flutter)
- **Framework**: Flutter Web
- **Estado**: MobX
- **UI**: Material Design 3
- **Responsividade**: Layout adaptativo
- **Funcionalidades**:
  - Dashboard interativo
  - Gestão de clientes
  - Controle de comissões
  - Sistema de mensagens
  - Gestão de produtos
  - Relatórios em tempo real

### Backend (Node.js)
- **Runtime**: Node.js
- **Framework**: Express.js
- **Banco de Dados**: MySQL
- **Autenticação**: JWT
- **APIs**:
  - RESTful APIs
  - WebSocket para tempo real
  - Integração com sistema de licenças

### Infraestrutura (Docker Compose)
- **Containerização**: Docker
- **Orquestração**: Docker Compose
- **Serviços**:
  - Nginx (Proxy reverso)
  - MySQL (Banco de dados)
  - Node.js (Backend)
  - Flutter Web (Frontend)

## 📋 Módulos da Plataforma

### Módulos Principais
1. **Dashboard**: Visão geral do negócio
2. **Clientes**: Gestão de clientes
3. **Comissões**: Controle de comissões
4. **Departamentos**: Organização interna
5. **Leads**: Gestão de leads
6. **Mensagens**: Sistema de comunicação
7. **Produções**: Controle de produção
8. **Produtos**: Catálogo de produtos
9. **Reembolsos**: Gestão financeira
10. **Usuários**: Controle de acesso
11. **Configurações**: Personalização do sistema

## 🔧 Configuração de Desenvolvimento

### Pré-requisitos
- Docker e Docker Compose
- Node.js 18+
- Flutter SDK 3.0+
- Git

## 🔒 Segurança

### Medidas Implementadas
- Autenticação JWT
- Validação de licenças em tempo real
- Isolamento por cliente (Docker)
- HTTPS obrigatório
- Rate limiting
- Logs de auditoria

### Controle de Acesso
- Validação de licença por requisição
- Controle de recursos por plano
- Sessões com timeout
- Logout automático

## 📊 Monitoramento

### Métricas Coletadas
- Uso de recursos por cliente
- Performance das APIs
- Disponibilidade dos serviços
- Logs de erro e acesso

## 📄 Licença

Este projeto é propriedade da DataCorb. Todos os direitos reservados.

---

**DataCorb** - Transformando a gestão empresarial através da tecnologia. 
