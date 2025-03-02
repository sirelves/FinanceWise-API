# 💰 FinanceWise API - Gestão Financeira Pessoal

### 🚀 Sobre o Projeto
A **FinanceWise API** é uma aplicação desenvolvida em **Java + Spring Boot** para ajudar usuários a controlarem suas finanças pessoais. Com ela, é possível registrar receitas, despesas, visualizar relatórios gráficos e importar extratos bancários para um melhor planejamento financeiro.

---

## 📌 Funcionalidades

- ✅ Cadastro e login de usuários (JWT Authentication)
- ✅ Registro de receitas e despesas
- ✅ Categorização automática de transações
- ✅ Dashboard financeiro com gráficos
- ✅ Importação de extratos bancários (CSV)
- ✅ Alertas por e-mail para vencimentos
- ✅ API documentada com Swagger
- ✅ Containerização com Docker e Kubernetes

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Java 21
- **Framework:** Spring Boot (Spring Web, Spring Security, Spring Data JPA)
- **Banco de Dados:** PostgreSQL
- **Autenticação:** JWT + Spring Security
- **Armazenamento de Arquivos:** AWS S3 / MinIO
- **Mensageria:** RabbitMQ
- **Testes:** JUnit + Mockito
- **Deploy:** Docker + Kubernetes

---

## 🎯 Estrutura do Banco de Dados (Simplificada)

### **Usuários (`users`):**
- `id` (UUID)
- `nome` (String)
- `email` (String, único)
- `senha_hash` (String)
- `data_criacao` (Timestamp)

### **Transações (`transactions`):**
- `id` (UUID)
- `user_id` (UUID, FK para users)
- `tipo` (Enum: RECEITA ou DESPESA)
- `valor` (Decimal)
- `categoria` (String)
- `data` (Date)

### **Arquivos de Extrato (`files`):**
- `id` (UUID)
- `user_id` (UUID, FK para users)
- `caminho_arquivo` (String)
- `data_upload` (Timestamp)

---

## 🏗️ Roadmap do Desenvolvimento

### **✅ Fase 1 - MVP (Produto Mínimo Viável)** *(Foco na funcionalidade básica e estabilidade)*
- [ ] Criar estrutura do projeto Spring Boot
- [ ] Configurar integração com PostgreSQL
- [ ] Implementar autenticação e autorização com JWT
- [ ] Criar endpoints para CRUD de usuários
- [ ] Criar endpoints para CRUD de transações financeiras (receitas e despesas)
- [ ] Implementar Swagger para documentação da API
- [ ] Criar testes unitários básicos para principais serviços

### **🔄 Fase 2 - Recursos Avançados** *(Foco em usabilidade e valor agregado)*
- [ ] Implementar categorização automática de despesas com IA
- [ ] Criar dashboard financeiro com gráficos interativos
- [ ] Desenvolver importação de extratos bancários via CSV
- [ ] Implementar notificações de vencimentos via e-mail
- [ ] Criar sistema de controle de orçamento e metas financeiras
- [ ] Implementar suporte a múltiplas contas bancárias
- [ ] Melhorar cobertura de testes unitários e criar testes de integração

### **🚀 Fase 3 - Escalabilidade e Deploy** *(Foco em performance, escalabilidade e segurança)*
- [ ] Implementar cache com Redis para otimizar performance
- [ ] Implementar logging e monitoramento com Prometheus e Grafana
- [ ] Implementar filas assíncronas para processamento pesado (RabbitMQ ou Kafka)
- [ ] Containerização com Docker e Kubernetes para escalabilidade
- [ ] Deploy contínuo em ambiente Cloud (AWS, Azure ou GCP)
- [ ] Criar testes de carga e stress para otimizar desempenho
- [ ] Configurar autenticação OAuth2 para integração com serviços terceiros

---

## 🏁 Como Executar o Projeto

### Pré-requisitos:
- Java 21+
- PostgreSQL
- Docker (opcional para containerização)

### Passos:
1. Clone o repositório:
   ```sh
   git clone https://github.com/sirelves/FinanceWise-API.git
   ```
2. Configure o banco de dados no `application.properties`
3. Execute o projeto com:
   ```sh
   mvn spring-boot:run
   ```
4. Acesse a documentação da API no Swagger:
   ```
   http://localhost:8080/swagger-ui.html
   ```

---

## 📄 Licença
Este projeto é open-source e está disponível sob a licença MIT.

💡 Contribuições são bem-vindas! Caso tenha sugestões ou melhorias, fique à vontade para abrir uma issue ou PR. 🚀

