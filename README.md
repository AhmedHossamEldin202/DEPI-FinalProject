# 🚀 Enterprise Automated Web & API Testing Framework
### Digital Egypt Pioneers Initiative (DEPI) — Graduation Project (QA Track)

[![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Selenium](https://img.shields.io/badge/Selenium_WebDriver-4.x-43B02A?style=for-the-badge&logo=selenium&logoColor=white)](https://www.selenium.dev/)
[![Cucumber BDD](https://img.shields.io/badge/Cucumber_BDD-7.x-23D96C?style=for-the-badge&logo=cucumber&logoColor=white)](https://cucumber.io/)
[![TestNG](https://img.shields.io/badge/TestNG-7.x-FF7F00?style=for-the-badge&logo=testng&logoColor=white)](https://testng.org/)
[![Postman](https://img.shields.io/badge/Postman-Collections-FF6C37?style=for-the-badge&logo=postman&logoColor=white)](https://www.postman.com/)
[![Newman CLI](https://img.shields.io/badge/Newman-CLI_Runner-FF6C37?style=for-the-badge&logo=npm&logoColor=white)](https://www.npmjs.com/package/newman)
[![Jira](https://img.shields.io/badge/Jira-Defect_Tracking-0052CC?style=for-the-badge&logo=jira&logoColor=white)](https://www.atlassian.com/software/jira)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AhmedHossamEldin202/DEPI-FinalProject)

An enterprise-grade Quality Assurance and Automation Testing ecosystem engineered for the **Digital Egypt Pioneers Initiative (DEPI)** Graduation Project. This repository implements an end-to-end quality validation lifecycle across Desktop Web UI and RESTful API architectures, combining **Behavior-Driven Development (BDD)**, **Page Object Model (POM)** patterns, structured **Manual Test Design**, and automated **CI/CD Regression Workflows**.

---

## 📌 Executive Summary & Project Objectives

This project defines, executes, and automates a multi-tier Quality Assurance strategy for two dedicated Systems Under Test (SUTs) across the full Agile delivery lifecycle:

* **End-to-End Desktop Web UI Validation:** Executing deep functional manual test cases and resilient BDD regression suites against the [BrowserStack Demo Store](https://bstackdemo.com/) using Java, Selenium WebDriver, Cucumber, and TestNG.
* **RESTful API Contract & Functional Testing:** Performing automated endpoint schema assertion, CRUD operation coverage, and negative scenario validation on the [Fake Store API](https://fakestoreapi.com) via Postman collections and Newman CLI.
* **Rigorous Defect Management:** Enforcing two-way traceability between structured Microsoft Excel test logs (Sheet 1: Test Cases, Sheet 2: Bug Reports Log) and an active Atlassian Jira Agile defect lifecycle.
* **Continuous Integration & Reporting:** Automated execution of smoke and regression test profiles upon code commits using headless browsers and multi-platform build pipelines.

---

## 👥 Dedicated QA Engineering Team

| Name | Role | Core Deliverables / Responsibilities |
| :--- | :--- | :--- |
| **Ahmed HossamEldin Ahmed** | **Team Leader / QC** | QA Test Strategy, Framework Architecture, Code Reviews, Final Sign-off |
| **Yossef Ayman Mohamed** | **QC Engineer** | UI Manual Testing, Cucumber Scenario Authoring, Test Execution |
| **Gehad Khamis Mahmoud** | **QC Engineer** | UI Manual Coverage, Selenium POM Implementation, Jira Defect Tracking |
| **Wafik Adel Razk** | **QC Engineer** | API Test Design, Automation Framework Support, Defect Evidence |
| **Gana EmadEldin** | **QC Engineer** | API Collection Design & Verification, Test Documentation & Excel Log |

---

## 🎯 Systems Under Test (SUT)

### 1. Frontend Web UI (Desktop Application)
* **Target SUT:** [BrowserStack Demo Store](https://bstackdemo.com/)
* **Architecture:** Responsive Single-Page Application (SPA) e-commerce storefront.
* **Core Verified Modules:**
  * **Authentication & Session Persistence:** Sign-in workflows, demo credential sessions, session timeout, and secure logout.
  * **Product Catalog & Dynamic Filtering:** Multi-vendor filtering (Apple, Samsung, Google), dynamic price sorting (Lowest to Highest, Highest to Lowest), and real-time DOM reactivity.
  * **Shopping Cart Mechanics:** Item addition/removal, live floating cart badge increment/decrement, dynamic subtotal calculations, and item counter accuracy.
  * **Mock Checkout & Fulfillment:** Shipping address form boundary assertions, simulated payment modal, and successful confirmation screens.

### 2. Backend REST API
* **Base Endpoint:** [https://fakestoreapi.com](https://fakestoreapi.com)
* **Services Verified:**
  * `POST /auth/login` — Token generation, valid/invalid payload verification, and HTTP 200/401 assertions.
  * `/products` — Full RESTful CRUD coverage (`GET` all products, `GET` by ID, `GET` categories, `POST`, `PUT`, `DELETE`).
  * `/carts` & `/carts/user/:id` — Cart persistence, date-range filtering, and user-specific payload validation.
  * `/users` — User profiles, schema contract checks, and data type boundary limits.

---

## 🚫 Scope Boundaries & Quality Safeguards

To prevent scope creep and guarantee high-depth verification of core business flows, scope limits were strictly enforced in accordance with the project test plan:

| In-Scope Capabilities | Out-of-Scope Limits | Engineering Justification |
| :--- | :--- | :--- |
| **Desktop Web UI Testing** (Manual & Automated) | ❌ **No Mobile Testing** | Focus is placed on enterprise desktop user journeys; mobile viewports and emulators are excluded. |
| **Cross-Browser Verification** (Chrome, Brave, Edge, Firefox) | ❌ **No Non-Functional / Stress Testing** | Performance benchmarks (JMeter) and security penetration testing are out of scope for functional sign-off. |
| **REST API Contract & Schema Assertions** | ❌ **No Direct Database Querying** | Integrity is evaluated via public API contracts and UI state, preserving clean-room black-box testing principles. |
| **Simulated E-Commerce Checkout Workflows** | ❌ **No Real Financial Transactions** | Payment flows operate exclusively via mock validation modals and simulated order confirmations. |

---

## 🛠️ Technology Stack & Framework Architecture

```text
                                  [ Cucumber BDD Feature Files ]
                                                 │
                                                 ▼
                                     [ Step Definitions Glue ]
                                                 │
                                                 ▼
                                   [ Page Object Model (POM) ]
                              (Encapsulated Locators & Interactions)
                                                 │
                                                 ▼
                                   [ Base Framework & Drivers ]
                             (Selenium WebDriver + Explicit Synchronization)
                                                 │
                                                 ▼
                               [ TestNG Engine & Parallel Suites ]
                                                 │
                        ┌────────────────────────┴────────────────────────┐
                        ▼                                                 ▼
             [ Extent / TestNG Reports ]                       [ GitHub Actions CI/CD ]

```

* **Programming Language:** Java 17 (LTS)
* **Build & Dependency Management:** Apache Maven
* **Web UI Automation:** Selenium WebDriver 4.x with Page Object Model (POM)
* **BDD Specification Engine:** Cucumber BDD using declarative Gherkin syntax (`Given`, `When`, `Then`)
* **Test Runner & Execution:** TestNG (driving assertions, test groups, XML suites, and listeners)
* **API Testing Engine:** Postman Desktop & Newman CLI
* **Synchronization Strategy:** Resilient Explicit Waits (`WebDriverWait` paired with `ExpectedConditions`) to eliminate flakiness on SPA DOM state changes.
* **Test Documentation & Defect Tracking:** Microsoft Excel Workbooks (Test Cases & Bug Log) synced with Atlassian Jira.

---

## 📁 Repository Directory Structure

```text
DEPI-FinalProject/
│
├── .github/
│   └── workflows/
│       └── regression-suite.yml         # GitHub Actions automated CI/CD pipeline
│
├── src/
│   ├── main/java/com/depi/framework/
│   │   ├── config/                      # Configuration managers & environment readers
│   │   ├── drivers/                     # Thread-safe WebDriver factory & browser initialization
│   │   ├── pages/                       # Page Object Model (POM) classes & UI locators
│   │   │   ├── LoginPage.java
│   │   │   ├── ProductCatalogPage.java
│   │   │   ├── CartPage.java
│   │   │   └── CheckoutPage.java
│   │   └── utils/                       # Explicit wait helpers, screenshot utilities, logger
│   │
│   └── test/
│       ├── java/com/depi/framework/
│       │   ├── runners/                 # TestNG Cucumber Runner suites
│       │   ├── stepdefinitions/         # BDD step definition glue code
│       │   └── listeners/               # TestNG execution & screenshot report listeners
│       └── resources/
│           ├── features/                # Gherkin BDD Feature Files
│           │   ├── Authentication.feature
│           │   ├── ProductCatalog.feature
│           │   ├── ShoppingCart.feature
│           │   └── CheckoutOrder.feature
│           ├── testdata/                # Parameterized test datasets
│           ├── config.properties        # Execution properties (browser, timeouts, baseUrl)
│           └── testng.xml               # Suite execution definitions
│
├── api-testing/
│   ├── postman/
│   │   ├── FakeStore_API_Collection.json   # Full Postman Collection (CRUD, Schema, Auth)
│   │   └── FakeStore_Environment.json      # Dynamic Postman Environment variables
│   └── reports/                            # Newman HTML execution summaries
│
├── test-management/
│   ├── DEPI_Manual_Test_Cases.xlsx         # Sheet 1: Detailed Test Cases with steps & statuses
│   └── DEPI_Bug_Reports_Log.xlsx           # Sheet 2: Formal Defect Log cross-referenced with Jira
│
├── reports/
│   ├── ExtentReports/                      # Interactive HTML automation dashboards
│   └── Final_Regression_Report.pdf         # Consolidated execution summary & sign-off
│
├── docs/
│   └── DEPI_Graduation_Test_Plan.pdf       # Approved Master QA Test Plan
│
├── pom.xml                                 # Maven dependencies and surefire plugins
└── README.md                               # Project documentation

```

---

## 📅 Agile Sprints & Execution Milestones

The project was executed across four structured sprints spanning **31/10 to 05/12**:

| Sprint | Date Window | Phase | Primary Deliverables & Milestones |
| --- | --- | --- | --- |
| **Sprint 1** | 31/10 – 11/11 | **Planning** | Master QA Test Plan approved, Scope established, Team RACI Matrix defined. |
| **Sprint 2** | 12/11 – 19/11 | **Design** | Detailed Manual Test Cases authored in Excel (Sheet 1), Postman API requests designed. |
| **Sprint 3** | 20/11 – 27/11 | **Implementation** | Java POM framework implemented, Cucumber step definitions bound, API scripts ready. |
| **Sprint 4** | 28/11 – 05/12 | **Execution** | Full Regression execution, Excel Bug Log synced with Jira, Final Sign-off Report delivered. |

---

## 📊 Team RACI Matrix

Governance and task ownership follow the approved RACI matrix:

* **R = Responsible** (Performs the activity)
* **A = Accountable** (Owns overall outcome and quality)
* **C = Consulted** (Provides input and review)
* **I = Informed** (Updated on progress)

| Project Activity / Deliverable | Ahmed Hossam | Yossef Ayman | Gehad Khamis | Wafik Adel | Gana Emad |
| --- | --- | --- | --- | --- | --- |
| **Test Plan, Scope & RACI** | **A / R** | C | C | I | I |
| **Manual UI Test Case Design** | **A** | **R** | **R** | C | I |
| **Manual UI Execution & Evidence** | **A** | **R** | **R** | C | I |
| **API Design & Postman Collections** | **A** | C | I | **R** | **R** |
| **Java / Selenium POM Framework** | **A** | C | **R** | **R** | I |
| **Cucumber BDD & TestNG Execution** | **A** | **R** | **R** | C | I |
| **Excel Bug Log & Jira Synchronization** | **A** | **R** | C | **R** | I |
| **Regression Report & Final Sign-Off** | **A / R** | C | C | C | I |

---

## 🐞 Defect Management & Jira Workflow

All defects discovered during manual and automated execution are logged in `test-management/DEPI_Bug_Reports_Log.xlsx` and synchronized with Atlassian Jira using the following engineering standards:

### 1. Defect Severity Classification

* **Blocker:** Prevents testing or obstructs a critical business flow with no workaround. Requires immediate notification, prioritization, and resolution prior to project sign-off.
* **Critical:** Major failure in core functionality with severe business impact and no workaround. High-priority resolution required prior to final sign-off.
* **Major:** Significant functional failure where a workaround exists or impact is isolated. Prioritized and fixed within the active sprint.
* **Minor:** Low-impact inconsistency, UI alignment/cosmetic defect, or non-blocking inconvenience. Scheduled based on capacity.

### 2. Jira Defect Lifecycle Workflow

```text
   [ Open ] ────────► [ In Progress ] ────────► [ Fixed ]
      ▲                                             │
      │                                             ▼
      └────────── [ Reopened ] ◄─────────────── [ Retest ]
                                                    │
                                                    ▼
                                                [ Closed ]

```

* **Open:** Defect logged with preconditions, reproduction steps, test data, and screenshots.
* **In Progress:** Assigned engineer investigates the root cause.
* **Fixed:** Engineering fix deployed and packaged for verification.
* **Retest:** QA validates the fix against explicit reproduction steps and regression areas.
* **Closed:** Resolution verified and signed off by QA.
* **Reopened:** Defect persists or triggers regression failures.

---

## 🚦 Quality Gates: Entry & Exit Criteria

Strict quality gates govern project sign-off:

### Entry Criteria

* Approved Test Plan and agreed scope signed off.
* Target SUTs (BrowserStack Demo Store and Fake Store API) accessible and operational.
* Test automation environment configured (Java 17+, Maven, Selenium, TestNG, Cucumber, Postman).
* Test datasets and demo credentials prepared for execution.

### Exit Criteria

* **>= 90% Pass Rate** achieved on critical business flows.
* **Zero (0) Unresolved Blocker or Critical defects** remaining at project closure.
* 100% of planned in-scope manual test cases executed and status logged.
* Core UI BDD smoke and regression suites automated and executed.
* Postman API collections executed with response assertions logged.
* Final Regression Execution Report completed with formal sign-off.

---

## 🛡️ Risk Management & Mitigation Matrix

| Risk Event | Potential Impact | Engineering Mitigation Strategy |
| --- | --- | --- |
| **SUT / API Unavailability** | Execution delays and blocked evidence capture. | Pre-execution health checks; execution pauses logged and resumed immediately once target is online. |
| **Dynamic SPA DOM / Element Flakiness** | False negative automation test failures. | Bounded Explicit Waits (`WebDriverWait`) replacing hard-coded thread sleeps entirely. |
| **Browser Compatibility Variations** | UI inconsistencies across rendering engines. | Cross-browser smoke testing executed across Chrome, Brave, Edge, and Firefox. |
| **API Schema Contract Drift** | Assertion failures on response payload changes. | Strict status code and schema verification scripts; contract discrepancies logged immediately. |
| **Test Data / Credential Invalidation** | Blocked authentication and checkout journeys. | Isolated test user pools maintained and validated prior to sprint execution. |
| **Unresolved Defect Ambiguity** | Inability to reproduce or confirm bug fixes. | Standardized defect logging requiring exact steps, environment details, and Jira keys. |
| **Scope Expansion / Creep** | Dilution of core functional testing deliverables. | Firm enforcement of Out-of-Scope boundaries (no mobile, no performance, no direct DB). |

---

## ⚙️ How to Set Up and Run the Framework

### Prerequisites

* **Java Development Kit (JDK):** Version 17 or higher
* **Apache Maven:** Version 3.8+
* **Browsers:** Google Chrome, Brave, Microsoft Edge, or Mozilla Firefox
* **Node.js & Newman (Optional for CLI API runs):**
```bash
npm install -g newman newman-reporter-htmlextra

```



### 1. Clone & Configure the Repository

```bash
git clone [https://github.com/AhmedHossamEldin202/DEPI-FinalProject.git](https://github.com/AhmedHossamEldin202/DEPI-FinalProject.git)
cd DEPI-FinalProject
mvn clean compile

```

### 2. Execute Automated UI Regression Tests

```bash
# Execute the complete automated test suite via TestNG
mvn clean test

# Execute smoke tests only
mvn test -Dcucumber.filter.tags="@Smoke"

# Execute a specific browser profile (e.g., Chrome or Firefox)
mvn test -Dbrowser=chrome

```

### 3. Execute Automated API Contract Tests via Newman

```bash
# Run the API suite with formatted CLI output
newman run api-testing/postman/FakeStore_API_Collection.json \
  -e api-testing/postman/FakeStore_Environment.json \
  --reporters cli,htmlextra \
  --reporter-htmlextra-export reports/api-report.html

```

---

## 🔄 CI/CD Automation Pipeline

Automated regression builds are managed via **GitHub Actions** (`.github/workflows/regression-suite.yml`). The workflow triggers on every `push` and `pull_request` to the `main` branch:

1. Provisions an Ubuntu runner with JDK 17 and headless Chrome/Firefox.
2. Caches Maven dependencies for faster build cycles.
3. Executes the full Cucumber BDD regression suite headlessly.
4. Archives TestNG test reports and ExtentReports as downloadable build artifacts.
