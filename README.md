# 🥷 NinjaV7 – Selenium Hybrid Automation Framework

An **enterprise-grade Selenium Hybrid Automation Framework** built for automating the **CloudBerry Store (OpenCart)** application.

NinjaV7 follows industry best practices and is designed to deliver **scalable, maintainable, and high-performance UI test automation** using Java, Selenium WebDriver, and TestNG—without relying on BDD/Cucumber.

---

## 🚀 Overview

NinjaV7 is a production-style automation framework that demonstrates a clean architecture using the **Page Object Model (POM)** and a hybrid framework approach. It is suitable for real-world enterprise projects, continuous integration pipelines, and automation portfolio demonstrations.

### Highlights

- Hybrid Automation Framework
- Page Object Model (POM)
- TestNG-based execution
- Data-driven testing support
- Multi-browser compatibility
- Extent HTML Reporting
- Screenshot capture on failures
- Retry mechanism for flaky tests
- Maven build management
- Jenkins-ready architecture

---

# 🛠 Technology Stack

| Technology | Description |
|------------|-------------|
| ☕ Java | Programming Language |
| 🌐 Selenium WebDriver 4 | UI Automation |
| ✅ TestNG | Test Framework |
| 📦 Maven | Dependency Management |
| 📄 Extent Reports | HTML Reporting |
| 📝 Log4j | Logging |
| 🏗 Page Object Model | Design Pattern |
| 🔄 Jenkins | Continuous Integration |
| 🌍 Chrome / Firefox / Edge | Browser Support |

---

# 📁 Project Structure

```
NinjaV7
│
├── src
│   └── test
│       ├── java
│       │   ├── pageObjects
│       │   ├── testCases
│       │   ├── testBase
│       │   ├── utilities
│       │   └── listeners
│       │
│       └── resources
│           ├── config.properties
│           └── testdata
│
├── screenshots
├── test-output
├── testng.xml
├── pom.xml
└── README.md
```

---

# ✨ Framework Features

- ✅ Hybrid Framework Architecture
- ✅ Page Object Model (POM)
- ✅ Reusable Page Classes
- ✅ Centralized WebDriver Management
- ✅ TestNG Groups
- ✅ Parallel Test Execution
- ✅ Retry Failed Tests
- ✅ Screenshot Capture on Failure
- ✅ Extent HTML Reports
- ✅ Logging with Log4j
- ✅ Data-Driven Testing
- ✅ Cross-Browser Execution
- ✅ Jenkins Compatible

---

# 🌐 Application Under Test

**CloudBerry Store (OpenCart)**

https://www.cloudberrystore.services

---

# ⚙ Prerequisites

Before running the project, ensure the following are installed:

- Java JDK 17+
- Maven 3.8+
- Eclipse / IntelliJ IDEA
- Google Chrome / Firefox / Edge
- Git

---

# 📥 Installation

Clone the repository:

```bash
git clone https://github.com/affan-bugbuster/NinjaV7.git
```

Navigate to the project:

```bash
cd NinjaV7
```

Install dependencies:

```bash
mvn clean install
```

---

# ▶ Running the Tests

## Using TestNG

Run the **testng.xml** suite from your IDE.

---

## Using Maven

```bash
mvn test
```

---

## Execute Specific Test Groups

Example:

```xml
<groups>
    <run>
        <include name="sanity"/>
    </run>
</groups>
```

---

## Parallel Execution

```xml
<suite parallel="tests" thread-count="3">
```

---

# 🧪 Sample Test

```java
@Test(groups = {"sanity","regression"})
public void verifyLogin() {

    HomePage home = new HomePage(driver);
    LoginPage login = new LoginPage(driver);

    home.clickMyAccount();
    home.goToLogin();

    login.setEmail(prop.getProperty("email"));
    login.setPassword(prop.getProperty("password"));
    login.clickLogin();

    Assert.assertTrue(login.isMyAccountPageDisplayed());
}
```

---

# 📊 Reporting

After execution, reports are generated automatically.

### 📄 Extent Report

```
test-output/ExtentReport.html
```

### 📷 Screenshots

Failure screenshots are automatically captured and stored inside:

```
screenshots/
```

---

# 🏗 Framework Design

The framework is built with the following goals:

- Separation of concerns
- Easy maintenance
- High code reusability
- Enterprise project structure
- Scalable automation architecture
- CI/CD readiness

---

# 🚀 Future Enhancements

- Jenkins Pipeline Integration
- Selenium Grid
- Docker Support
- BrowserStack Integration
- Sauce Labs Integration
- REST API Automation
- Allure Reporting
- GitHub Actions Workflow

---

# 👨‍💻 Author

**Shadab Siddiqui**

Co-Founder – CloudBerry QA Automation

- Selenium Automation
- Java
- TestNG
- Hybrid Framework
- CI/CD
- Enterprise Test Automation

---

# ⭐ Support

If you found this project helpful:

- ⭐ Star the repository
- 🍴 Fork the project
- 🛠 Contribute improvements
- 📢 Share it with others

---

## 📜 License

This project is intended for educational, demonstration, and portfolio purposes.

Feel free to use and extend it for learning and personal projects.

---

> Built with ❤️ using Java, Selenium WebDriver, TestNG, and the Page Object Model.
