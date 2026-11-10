# 🚀 DEPI Graduation Project - Automated Web Testing Framework

[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)](https://www.selenium.dev/)
[![Cucumber](https://img.shields.io/badge/Cucumber-23D96C?style=for-the-badge&logo=cucumber&logoColor=white)](https://cucumber.io/)
[![TestNG](https://img.shields.io/badge/TestNG-FF7F00?style=for-the-badge&logo=testng&logoColor=white)](https://testng.org/)
[![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)](https://www.postman.com/)
[![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)](https://www.atlassian.com/software/jira)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AhmedHossamEldin202/DEPI-FinalProject)

An enterprise-standard Quality Assurance testing ecosystem developed for the **Digital Egypt Pioneers Initiative (DEPI)** Graduation Project. This repository hosts a robust **BDD Test Automation Framework** combined with structured **Manual Testing** and **RESTful API Contract Testing**.

---

## 📌 Project Overview & Objectives

The goal of this project is to implement an end-to-end functional quality engineering workflow across an Agile lifecycle:

- **Desktop Web UI Testing:** Manual validation and BDD test automation using Page Object Model (POM) on the **[BrowserStack Demo Store](https://bstackdemo.com/)**.
- **RESTful API Validation:** Automated functional and schema assertion testing on the **[Fake Store API](https://fakestoreapi.com)** via Postman collections and Newman CLI.
- **Defect Tracking:** Formal bug logging and test execution synchronization using **Microsoft Excel** and **Atlassian Jira**.

---

## 👥 Dedicated QA Engineering Team

| Name | Role | Core Deliverables / Responsibilities |
| :--- | :--- | :--- |
| **Ahmed HossamEldin Ahmed** | **Team Leader / QC** | Test Strategy, Framework Architecture, Code Reviews, Final Sign-off |
| **Yossef Ayman Mohamed** | **QC Engineer** | UI Manual Testing, Cucumber Scenario Authoring, Test Execution |
| **Gehad Khamis Mahmoud** | **QC Engineer** | UI Manual Coverage, Selenium POM Implementation, Jira Defect Tracking |
| **Wafik Adel Razk** | **QC Engineer** | API Test Design, Automation Framework Support, Defect Evidence |
| **Gana EmadEldin** | **QC Engineer** | API Collection Design & Verification, Test Documentation & Excel Log |

---

## 🎯 Systems Under Test (SUT)

### 1. Frontend Web UI (Desktop Only)
* **Application URL:** [https://bstackdemo.com/](https://bstackdemo.com/)
* **Architecture:** Responsive Single-Page Application (SPA) e-commerce storefront.
* **Core Modules Validated:**
  * **User Authentication:** Demo account login, persistent user session, sign-out states.
  * **Product Catalog:** Product list view, vendor filters (Apple, Samsung, Google), dynamic price sorting.
  * **Shopping Cart:** Add/remove items, live cart badge counter updates, dynamic subtotal calculations.
  * **Mock Checkout:** Shipping address validation, fake payment modal, order confirmation messages.

### 2. Backend REST API
* **Base Endpoint:** [https://fakestoreapi.com](https://fakestoreapi.com)
* **Services Tested:**
  * `/auth/login` (Token generation, schema verification, negative credential tests).
  * `/products` (GET all products, GET single product by ID, categories, POST, PUT, DELETE).
  * `/carts` (Cart payload retrieval, user-specific cart verification, date filtering).
  * `/users` (User profiles, data structure verification, boundary checks).

---

## 🚫 Scope Boundaries

* **In-Scope:**
  * Desktop Functional Manual & Automated Testing (Google Chrome, Brave, Microsoft Edge, Mozilla Firefox).
  * REST API Contract & Functional Validation.
  * Defect Management via Jira and Excel Sheets.
* **Out-of-Scope:**
  * ❌ **NO Mobile Testing:** No mobile devices, viewports, or emulators.
  * ❌ **NO Non-Functional Testing:** No performance, load/stress (JMeter), or security penetration testing.
  * ❌ **NO Direct Database Testing:** Data consistency evaluated strictly via UI and API responses.
  * ❌ **NO Real Financial Transactions:** Mock checkout simulations only.

---

## 🛠️ Tech Stack & Framework Architecture

### Framework Architectural Highlights:
* **Design Pattern:** Modular **Page Object Model (POM)** separating UI locators from test logic.
* **BDD Implementation:** Human-readable Gherkin specifications (`Given`, `When`, `Then`) mapped to Java step definitions.
* **Synchronization:** Resilient explicit waits (`WebDriverWait` + `ExpectedConditions`) eliminating flakiness on SPA elements.
* **Execution Engine:** **TestNG** powering assertions, test suites (`testng.xml`), and execution profiles.

---

## 📅 Agile Sprints & Project Roadmap

| Sprint | Date Window | Phase | Key Milestone Deliverables |
| :--- | :--- | :--- | :--- |
| **Sprint 1** | 31/10 – 11/11 | **Planning** | Master Test Plan approved, Scope defined, RACI Matrix established. |
| **Sprint 2** | 12/11 – 19/11 | **Design** | Excel Test Cases (Sheet 1) authored, Postman API collections structured. |
| **Sprint 3** | 20/11 – 27/11 | **Implementation** | Java POM framework complete, Cucumber steps bound, API assertions ready. |
| **Sprint 4** | 28/11 – 05/12 | **Execution** | Regression execution, Excel Bug Log (Sheet 2) synced with Jira, Sign-off report. |

---

## 🚀 How to Set Up and Run the Tests

### Prerequisites
* **Java JDK:** Version 17 or higher installed and configured.
* **Apache Maven:** Version 3.8+ installed.
* **Browsers:** Google Chrome (Latest), Brave, Firefox, or Edge.
* **Node.js & Newman (Optional for CLI API tests):** `npm install -g newman`

### 1. Clone the Repository
```bash
git clone [https://github.com/AhmedHossamEldin202/DEPI-FinalProject.git](https://github.com/AhmedHossamEldin202/DEPI-FinalProject.git)
cd DEPI-FinalProject# 🚀 DEPI Graduation Project - Automated Web Testing Framework

[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)](https://www.selenium.dev/)
[![Cucumber](https://img.shields.io/badge/Cucumber-23D96C?style=for-the-badge&logo=cucumber&logoColor=white)](https://cucumber.io/)
[![TestNG](https://img.shields.io/badge/TestNG-FF7F00?style=for-the-badge&logo=testng&logoColor=white)](https://testng.org/)
[![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)](https://www.postman.com/)
[![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)](https://www.atlassian.com/software/jira)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AhmedHossamEldin202/DEPI-FinalProject)

An enterprise-standard Quality Assurance testing ecosystem developed for the **Digital Egypt Pioneers Initiative (DEPI)** Graduation Project. This repository hosts a robust **BDD Test Automation Framework** combined with structured **Manual Testing** and **RESTful API Contract Testing**.

---

## 📌 Project Overview & Objectives

The goal of this project is to implement an end-to-end functional quality engineering workflow across an Agile lifecycle:

- **Desktop Web UI Testing:** Manual validation and BDD test automation using Page Object Model (POM) on the **[BrowserStack Demo Store](https://bstackdemo.com/)**.
- **RESTful API Validation:** Automated functional and schema assertion testing on the **[Fake Store API](https://fakestoreapi.com)** via Postman collections and Newman CLI.
- **Defect Tracking:** Formal bug logging and test execution synchronization using **Microsoft Excel** and **Atlassian Jira**.

---

## 👥 Dedicated QA Engineering Team

| Name | Role | Core Deliverables / Responsibilities |
| :--- | :--- | :--- |
| **Ahmed HossamEldin Ahmed** | **Team Leader / QC** | Test Strategy, Framework Architecture, Code Reviews, Final Sign-off |
| **Yossef Ayman Mohamed** | **QC Engineer** | UI Manual Testing, Cucumber Scenario Authoring, Test Execution |
| **Gehad Khamis Mahmoud** | **QC Engineer** | UI Manual Coverage, Selenium POM Implementation, Jira Defect Tracking |
| **Wafik Adel Razk** | **QC Engineer** | API Test Design, Automation Framework Support, Defect Evidence |
| **Gana EmadEldin** | **QC Engineer** | API Collection Design & Verification, Test Documentation & Excel Log |

---

## 🎯 Systems Under Test (SUT)

### 1. Frontend Web UI (Desktop Only)
* **Application URL:** [https://bstackdemo.com/](https://bstackdemo.com/)
* **Architecture:** Responsive Single-Page Application (SPA) e-commerce storefront.
* **Core Modules Validated:**
  * **User Authentication:** Demo account login, persistent user session, sign-out states.
  * **Product Catalog:** Product list view, vendor filters (Apple, Samsung, Google), dynamic price sorting.
  * **Shopping Cart:** Add/remove items, live cart badge counter updates, dynamic subtotal calculations.
  * **Mock Checkout:** Shipping address validation, fake payment modal, order confirmation messages.

### 2. Backend REST API
* **Base Endpoint:** [https://fakestoreapi.com](https://fakestoreapi.com)
* **Services Tested:**
  * `/auth/login` (Token generation, schema verification, negative credential tests).
  * `/products` (GET all products, GET single product by ID, categories, POST, PUT, DELETE).
  * `/carts` (Cart payload retrieval, user-specific cart verification, date filtering).
  * `/users` (User profiles, data structure verification, boundary checks).

---

## 🚫 Scope Boundaries

* **In-Scope:**
  * Desktop Functional Manual & Automated Testing (Google Chrome, Brave, Microsoft Edge, Mozilla Firefox).
  * REST API Contract & Functional Validation.
  * Defect Management via Jira and Excel Sheets.
* **Out-of-Scope:**
  * ❌ **NO Mobile Testing:** No mobile devices, viewports, or emulators.
  * ❌ **NO Non-Functional Testing:** No performance, load/stress (JMeter), or security penetration testing.
  * ❌ **NO Direct Database Testing:** Data consistency evaluated strictly via UI and API responses.
  * ❌ **NO Real Financial Transactions:** Mock checkout simulations only.

---

## 🛠️ Tech Stack & Framework Architecture

### Framework Architectural Highlights:
* **Design Pattern:** Modular **Page Object Model (POM)** separating UI locators from test logic.
* **BDD Implementation:** Human-readable Gherkin specifications (`Given`, `When`, `Then`) mapped to Java step definitions.
* **Synchronization:** Resilient explicit waits (`WebDriverWait` + `ExpectedConditions`) eliminating flakiness on SPA elements.
* **Execution Engine:** **TestNG** powering assertions, test suites (`testng.xml`), and execution profiles.

---

## 📅 Agile Sprints & Project Roadmap

| Sprint | Date Window | Phase | Key Milestone Deliverables |
| :--- | :--- | :--- | :--- |
| **Sprint 1** | 31/10 – 11/11 | **Planning** | Master Test Plan approved, Scope defined, RACI Matrix established. |
| **Sprint 2** | 12/11 – 19/11 | **Design** | Excel Test Cases (Sheet 1) authored, Postman API collections structured. |
| **Sprint 3** | 20/11 – 27/11 | **Implementation** | Java POM framework complete, Cucumber steps bound, API assertions ready. |
| **Sprint 4** | 28/11 – 05/12 | **Execution** | Regression execution, Excel Bug Log (Sheet 2) synced with Jira, Sign-off report. |

---

## 🚀 How to Set Up and Run the Tests

### Prerequisites
* **Java JDK:** Version 17 or higher installed and configured.
* **Apache Maven:** Version 3.8+ installed.
* **Browsers:** Google Chrome (Latest), Brave, Firefox, or Edge.
* **Node.js & Newman (Optional for CLI API tests):** `npm install -g newman`

### 1. Clone the Repository
```bash
git clone [https://github.com/AhmedHossamEldin202/DEPI-FinalProject.git](https://github.com/AhmedHossamEldin202/DEPI-FinalProject.git)
cd DEPI-FinalProject
