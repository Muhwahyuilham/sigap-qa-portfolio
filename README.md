# SIGAP QA Portfolio

**Quality Assurance | Manual Testing | Test Documentation | Playwright Automation**

## About the Project

This repository contains my Quality Assurance portfolio, documenting the testing activities performed on the **SIGAP (Sistem Informasi Pengajuan)** application.

The project focuses on validating application functionality, identifying potential defects, verifying business requirements, and ensuring that the application behaves as expected from an end-user perspective.

This portfolio demonstrates my practical understanding of software testing methodologies, test case design, test execution, defect analysis, and test automation.

## Project Objectives

- Validate application functionality against defined requirements.
- Design structured and reusable test cases.
- Execute manual testing scenarios and document actual results.
- Identify, analyze, and report potential defects.
- Verify application data consistency between the user interface and database.
- Develop automated test scripts using Playwright.

## Application Under Test

| Information | Details |
|---|---|
| Application | SIGAP |
| Application Type | Web Application |
| Testing Approach | Manual Testing |
| Test Environment | Localhost |
| Browser | Google Chrome |
| Database | MySQL |
| Database Tool | phpMyAdmin |
| Automation Tool | Playwright (planned/in progress) |

## Testing Scope

The testing activities cover the following functional areas:

### 1. Authentication Testing
- Login with valid credentials.
- Login with invalid username.
- Login with invalid password.
- Logout functionality.
- Session termination after logout.
- Unauthorized dashboard access.

### 2. Dashboard Testing
- Dashboard accessibility.
- Application status count accuracy.
- Verification of dashboard data against database records.
- Validation of displayed status information based on business requirements.

### 3. Order Management Testing
- Incoming application list.
- Application detail page.
- Application file download.
- Application approval and rejection workflow.
- Role-based application processing.

## Repository Structure

```text
sigap-qa-portfolio/
│
├── documentation/
│   ├── Test Plans
│   ├── Test Cases
│   ├── Test Execution
│   └── Bug Reports
│
├── evidence/
│   └── manual/
│       ├── auth/
│       ├── dashboard/
│       └── orders/
│
├── automation/
│   └── Playwright test scripts (planned)
│
└── README.md
```

## Testing Artifacts

The following testing artifacts are maintained in this repository:

| Artifact | Description |
|---|---|
| Test Plan | Defines testing objectives, scope, and approach. |
| Test Cases | Documents preconditions, test steps, and expected results. |
| Test Execution | Records actual execution results. |
| Bug Reports | Documents identified defects and their impact. |
| Test Evidence | Screenshots supporting test execution results. |
| Automation Scripts | Automated testing scripts developed with Playwright. |

## Tools & Technologies

- **Manual Testing:** Functional and negative testing.
- **Playwright:** Web application test automation.
- **MySQL:** Database validation.
- **phpMyAdmin:** Database inspection and SQL queries.
- **Microsoft Excel:** Test case management and execution tracking.
- **Git & GitHub:** Version control and portfolio management.
- **Google Chrome:** Browser testing.

## Current Progress

| Activity | Status |
|---|---|
| Test Case Design | In Progress |
| Authentication Testing | Executed |
| Dashboard Testing | In Progress |
| Order Management Testing | In Progress |
| Database Validation | Executed |
| Test Evidence Documentation | In Progress |
| Playwright Automation | Planned |

*Progress status will be updated as testing activities continue.*

## Learning Outcomes

Through this project, I aim to strengthen my practical skills in:

- Understanding software requirements and translating them into test scenarios.
- Designing effective positive and negative test cases.
- Performing functional and regression testing.
- Analyzing actual results against expected results.
- Understanding session management and access control.
- Performing database validation using SQL.
- Developing automated end-to-end tests using Playwright.
- Maintaining structured QA documentation.

## Author

**Muhammad Wahyu Ilhan**

Aspiring Quality Assurance Engineer

GitHub: [@Muhwahyuilham](https://github.com/Muhwahyuilham)

---

*This repository is part of my continuous learning journey in Software Quality Assurance and Test Automation.*
