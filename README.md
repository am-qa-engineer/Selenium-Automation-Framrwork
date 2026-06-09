# 🧪 Selenium Automation Framework

![Java](https://img.shields.io/badge/Java-11-orange?logo=java)
![Selenium](https://img.shields.io/badge/Selenium-4.18-green?logo=selenium)
![TestNG](https://img.shields.io/badge/TestNG-7.9-blue)
![Maven](https://img.shields.io/badge/Maven-3.9-red?logo=apache-maven)
![CI](https://github.com/YOUR_USERNAME/selenium-automation-framework/actions/workflows/ci.yml/badge.svg)

A professional, scalable UI automation framework built with **Java**, **Selenium WebDriver 4**, and **TestNG** — following the **Page Object Model (POM)** design pattern.

---

## 📁 Project Structure

```
selenium-automation-framework/
├── src/test/java/
│   ├── pages/              # Page Object classes (POM)
│   │   ├── BasePage.java   # Shared page actions
│   │   ├── LoginPage.java
│   │   └── HomePage.java
│   ├── tests/              # TestNG test classes
│   │   └── LoginTest.java  # 7 test cases (smoke + regression)
│   └── utils/              # Utilities
│       ├── BaseTest.java   # Driver setup/teardown
│       ├── WaitUtils.java  # Explicit waits
│       └── ConfigReader.java
├── src/test/resources/
│   ├── testng.xml          # Suite configuration
│   └── config.properties   # Environment config
├── .github/workflows/
│   └── ci.yml              # GitHub Actions CI pipeline
└── pom.xml
```

---

## ✅ Test Coverage

| Test ID | Scenario | Type |
|---------|----------|------|
| TC_LOGIN_01 | Valid login redirects to secure page | Smoke |
| TC_LOGIN_02 | Welcome message shown after login | Regression |
| TC_LOGIN_03 | User can logout successfully | Regression |
| TC_LOGIN_04 | Invalid password shows error | Regression |
| TC_LOGIN_05 | Invalid username shows error | Regression |
| TC_LOGIN_06 | Empty credentials shows error | Regression |
| TC_LOGIN_07 | Data-driven invalid credentials (5 scenarios) | Regression |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Java 11 | Programming language |
| Selenium WebDriver 4 | Browser automation |
| TestNG 7.9 | Test framework & assertions |
| Maven | Build & dependency management |
| WebDriverManager | Automatic driver management |
| Log4j2 | Logging |
| GitHub Actions | CI/CD pipeline |

---

## 🚀 How to Run

### Prerequisites
- Java 11+
- Maven 3.6+
- Chrome browser

### Run all tests
```bash
mvn clean test
```

### Run smoke tests only
```bash
mvn clean test -Dgroups=smoke
```

### Run with Firefox
```bash
mvn clean test -Dbrowser=firefox
```

### Run headless
```bash
mvn clean test -Dheadless=true
```

---

## 🔄 CI/CD

This project uses **GitHub Actions** for continuous testing:
- Triggers on every **push** and **pull request** to `main`
- Scheduled **daily regression run** at 8:00 AM UTC
- Test reports uploaded as **artifacts** after each run

---

## 📌 Design Patterns Used

- **Page Object Model (POM)** — separates test logic from UI interactions
- **Data-Driven Testing** — TestNG `@DataProvider` for multiple input scenarios
- **BaseTest / BasePage** — reduces code duplication across tests
- **Explicit Waits** — via `WaitUtils`, no hardcoded `Thread.sleep()`

---

## 👤 Author

Amal 
QA Engineer | Java | Selenium | TestNG  
[LinkedIn](https://www.linkedin.com/in/amal-a49244350) • [GitHub](https://github.com/am-qa-engineer)

