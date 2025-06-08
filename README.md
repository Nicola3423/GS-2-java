# Controllers - Sistema de Segurança Urbana

Este repositório contém os controllers do sistema de segurança urbana, desenvolvido em Spring Boot, responsáveis por gerenciar as funcionalidades de Guarda Civil e Rotas Seguras.

## Integrantes:
- Igor Akira Bortolini Tateishi RM:554227 
- Nicola Monte Cravo Garofalo RM:553991 
- Willyam Santos Souza RM:554244 

## Link do video:
- https://youtu.be/FUXBZafpDmw


## 📋 Sobre o Projeto

O sistema permite o gerenciamento de informações da Guarda Civil e o cadastro de rotas seguras, proporcionando uma interface web para operações CRUD (Create, Read, Update, Delete).

## 🏗️ Arquitetura

### Controllers Implementados

#### 1. GuardaController
Responsável pelo gerenciamento das informações da Guarda Civil.

**Endpoints disponíveis:**
- `GET /api/guarda/cadastrar` - Exibe formulário de cadastro
- `POST /api/guarda/cadastrar` - Processa cadastro/atualização
- `GET /api/guarda/listar` - Lista todas as informações cadastradas
- `GET /api/guarda/{id}/editar` - Exibe formulário de edição
- `GET /api/guarda/{id}` - Exclui registro específico

#### 2. RotaSeguraController
Gerencia o cadastro e manutenção de rotas seguras.

**Endpoints disponíveis:**
- `GET /api/rotasegura/cadastrar` - Exibe formulário de cadastro
- `POST /api/rotasegura/cadastrar` - Processa cadastro/atualização
- `GET /api/rotasegura/listar` - Lista todas as rotas cadastradas
- `GET /api/rotasegura/editar/{id}` - Exibe formulário de edição
- `GET /api/rotasegura/{id}` - Exclui rota específica

## 🛠️ Tecnologias Utilizadas

- **Java 17+**
- **Spring Boot 3.x**
- **Spring MVC**
- **Spring Data JPA**
- **Thymeleaf** (para renderização de views)
- **JUnit 5** (testes unitários)
- **Mockito** (mocks para testes)
- **Gradle** (gerenciamento de dependências)

## 📦 Estrutura do Projeto

```
src/
├── main/java/com/fiap/gs/controller/
│   ├── GuardaController.java
│   └── RotaSeguraController.java
└── test/java/com/fiap/gs/controller/
    ├── GuardaControllerTest.java
    └── RotaSeguraControllerTest.java
```

## 🧪 Testes

O projeto inclui testes unitários abrangentes para ambos os controllers, cobrindo:

### GuardaControllerTest
- ✅ Teste de exibição do formulário de cadastro
- ✅ Teste de listagem de mensagens
- ✅ Teste de atualização de guarda civil
- ✅ Teste de exclusão de mensagem

### RotaSeguraControllerTest
- ✅ Teste de exibição do formulário de cadastro
- ✅ Teste de listagem de rotas seguras
- ✅ Teste de atualização de rota segura
- ✅ Teste de exclusão de rota segura

## 🚀 Como Executar os Testes

```bash
# Executar todos os testes
./gradlew test

# Executar testes específicos de um controller
./gradlew test --tests "GuardaControllerTest"
./gradlew test --tests "RotaSeguraControllerTest"

# Executar com relatório de cobertura
./gradlew jacocoTestReport
```

## 📋 Pré-requisitos

- Java 17 ou superior
- Gradle 7.0+
- Spring Boot 3.x

## 🔧 Configuração

### Dependências Principais

```gradle
dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-web'
    implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
    implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
    implementation 'org.springframework.boot:spring-boot-starter-validation'
    
    testImplementation 'org.springframework.boot:spring-boot-starter-test'
    testImplementation 'org.mockito:mockito-core'
    testImplementation 'org.junit.jupiter:junit-jupiter'
}
```

## 📊 Funcionalidades

### Guarda Civil
- **Cadastro**: Permite registrar informações de contato da guarda civil
- **Listagem**: Visualiza todas as informações cadastradas
- **Edição**: Atualiza informações existentes
- **Exclusão**: Remove registros do sistema

### Rota Segura
- **Cadastro**: Registra endereços de rotas seguras
- **Listagem**: Visualiza todas as rotas cadastradas
- **Edição**: Atualiza informações de rotas existentes
- **Exclusão**: Remove rotas do sistema

## 🔄 Fluxo de Dados

1. **Requisição HTTP** → Controller
2. **Controller** → Service (lógica de negócio)
3. **Service** → Repository (acesso a dados)
4. **Repository** → Banco de Dados
5. **Resposta** →
