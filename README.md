# Java Selenium TestNG Web Tests

[![Build Status](https://dev.azure.com/saymonoliveira/Templates%20Pipelines/_apis/build/status/Templates%20Pipelines-Maven-CI?branchName=headless)](https://dev.azure.com/saymonoliveira/Templates%20Pipelines/_build/latest?definitionId=2&branchName=headless)

## 📋 Descrição

Este projeto é um template para automação de testes web utilizando **Java**, **Selenium WebDriver** e **TestNG**. Ele foi projetado para ser modular, reutilizável e fácil de manter, seguindo boas práticas de desenvolvimento de software e automação de testes.

## 🛠️ Tecnologias e Ferramentas

- **Linguagem**: [Java](https://www.java.com/pt-BR/)
- **Gerenciador de Dependências**: [Maven](https://maven.apache.org)
- **Framework de Automação Web**: [Selenium WebDriver](https://www.selenium.dev/)
- **Orquestrador de Testes**: [TestNG](https://testng.org/doc/)
- **Relatórios de Testes**: [ExtentReports](http://www.extentreports.com/docs/versions/4/java/index.html)
- **Outras Dependências**:
  - [Apache Commons Lang3](https://commons.apache.org/proper/commons-lang/)
  - [Apache Commons IO](https://commons.apache.org/proper/commons-io/)

## 📂 Estrutura do Projeto

```plaintext
src/
├── test/
│   ├── java/
│   │   └── com/
│   │       └── javaseleniumtemplate/
│   │           ├── bases/          # Classes base para páginas e testes
│   │           ├── dbsteps/        # Interações com o banco de dados
│   │           ├── flows/          # Fluxos de ações comuns
│   │           ├── pages/          # Page Objects
│   │           ├── queries/        # Consultas SQL
│   │           ├── tests/          # Classes de testes
│   │           └── utils/          # Utilitários e helpers
│   └── resources/
│       └── files/                  # Arquivos de suporte (ex.: anexos)
```

## 🚀 Configuração do Ambiente

### Pré-requisitos

1. **Java JDK 1.8** ou superior: [Download](https://www.oracle.com/br/java/technologies/javase/javase-jdk8-downloads.html)
2. **Maven**: [Download](https://maven.apache.org/download.cgi)
3. **Google Chrome**: Última versão instalada ([Download](https://www.google.com/chrome/))
4. **Chromedriver**: Compatível com a versão do Chrome ([Download](https://chromedriver.chromium.org/downloads))

### Passos para Configuração

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```

2. Configure as dependências do Maven:
   ```bash
   mvn dependency:resolve
   ```

3. Atualize o arquivo `globalParameters.properties` com os valores adequados para o ambiente de execução.

4. Execute os testes:
   ```bash
   mvn test
   ```

## 🧪 Estrutura de Testes

### Classes Base

- **[`PageBase`](src/test/java/com/javaseleniumtemplate/bases/PageBase.java)**: Contém métodos genéricos para interação com elementos da página.
- **[`TestBase`](src/test/java/com/javaseleniumtemplate/bases/TestBase.java)**: Configurações e hooks para os testes.

### Page Objects

- **[`LoginPage`](src/test/java/com/javaseleniumtemplate/pages/LoginPage.java)**: Representa a página de login.
- **[`MainPage`](src/test/java/com/javaseleniumtemplate/pages/MainPage.java)**: Representa a página principal.
- **[`BugReportPage`](src/test/java/com/javaseleniumtemplate/pages/BugReportPage.java)**: Representa a página de relatório de bugs.

### Fluxos

- **[`LoginFlows`](src/test/java/com/javaseleniumtemplate/flows/LoginFlows.java)**: Contém o fluxo de login.

### Testes

- **[`LoginTests`](src/test/java/com/javaseleniumtemplate/tests/LoginTests.java)**: Testes relacionados ao login.
- **[`ReportIssueTests`](src/test/java/com/javaseleniumtemplate/tests/ReportIssueTests.java)**: Testes relacionados ao cadastro de issues.

## 📊 Relatórios de Testes

Os relatórios são gerados automaticamente após a execução dos testes e podem ser encontrados no diretório `target/reports/`. O relatório inclui capturas de tela (se configurado) e informações detalhadas sobre cada teste.

### Configuração de Captura de Tela

No arquivo `globalParameters.properties`, configure o parâmetro `get.screenshot.for.each.step` para `true` ou `false` conforme necessário.

## 🧩 Padrões de Código

- **Pastas**: Iniciam com letra minúscula (ex.: `pages`, `flows`).
- **Classes**: Iniciam com letra maiúscula e terminam com o tipo (ex.: `LoginPage`, `LoginTests`).
- **Métodos e Variáveis**: Iniciam com letra minúscula (ex.: `efetuarLoginComSucesso`).
- **Objetos**: Nomeados com base na classe, iniciando com letra minúscula (ex.: `loginPage` para a classe `LoginPage`).

## 🛡️ Boas Práticas

- **Reutilização**: Métodos genéricos em `PageBase` e `TestBase` para evitar duplicação de código.
- **Modularidade**: Separação clara entre Page Objects, Flows e Testes.
- **Manutenção**: Estrutura de projeto organizada para facilitar alterações e adições.

## 📄 Licença

Este projeto está licenciado sob a [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

## 🤝 Contribuição

Contribuições são bem-vindas! Siga os passos abaixo para contribuir:

1. Faça um fork do repositório.
2. Crie uma branch para sua feature:
   ```bash
   git checkout -b minha-feature
   ```
3. Commit suas alterações:
   ```bash
   git commit -m "Adiciona minha feature"
   ```
4. Envie para o repositório remoto:
   ```bash
   git push origin minha-feature
   ```
5. Abra um Pull Request.

---

**Desenvolvido com 💻 e ☕ por [Seu Nome](https://github.com/seu-usuario).**


