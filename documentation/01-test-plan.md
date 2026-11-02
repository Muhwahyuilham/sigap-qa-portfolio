# TEST PLAN

## SIGAP (SISTEM INFORMASI LAYANAN GANGGUAN DAN PERMOHONAN) APPLICATION

### 1. Project Information

- Project Name: SIGAP
- Application Type: Web Application
- Framework: CodeIgniter 4
- Programming Language: PHP
- Database: MySQL
- Testing Tool: Playwright
- Testing Environment: Localhost XAMPP
- Browser: Chromium

### 2. Testing Objective

The objective of this testing is to evaluate the
functionality, reliability, and usability of the
SIGAP application.

Testing will focus on identifying defects,
validating business workflows, and ensuring that
the application behaves according to its
requirements.

### 3. Scope of Testing

#### In Scope

- Authentication
- Admin Dashboard
- Incoming Orders
- Order Details
- Order Approval
- Order Rejection
- Order Status
- User Authorization

#### Out of Scope

- Large-scale performance testing
- Production security penetration testing
- Third-party integration testing

### 3.1 Business Rules

SIGAP implements four order statuses:

1. WAITING
   - An order has been submitted and is waiting
     for administrative processing.
   - Displayed as Pending in the Incoming Orders page.
   - Can be approved for further processing.
   - Can be rejected by the administrator.

2. ON PROCESS
   - An order is currently being handled by
     the administrator.
   - Represents an order that has entered
     the processing stage.

3. COMPLETED
   - An order has completed the administrative
     processing workflow.
   - Displayed as Done in the Order Status page.

4. REJECTED
   - An order has been rejected by
     the administrator.
   - Represents a separate outcome from
     the primary processing workflow.

### 3.2 Order Status Transition Rules

The primary workflow follows this sequence:

WAITING -> ON PROCESS -> COMPLETED

The rejection workflow is:

WAITING -> REJECTED

The following business rules apply:

- WAITING orders can be approved or rejected.
- ON PROCESS orders can proceed to COMPLETED.
- ON PROCESS orders cannot be rejected.
- COMPLETED orders cannot return to previous statuses.
- REJECTED orders cannot return to the primary workflow.
- Duplicate processing must be prevented.

### 3.3 Status Mapping Validation

The application uses different status labels
across its pages.

The following mappings must remain consistent:

| Business Status | UI Display |
| --------------- | ---------- |
| WAITING         | Pending    |
| ON PROCESS      | On Process |
| COMPLETED       | Done       |
| REJECTED        | Rejected   |

Testing must verify that displayed labels
correctly represent the underlying order status.

### 3.4 Business Rule Validation

Testing will verify:

- Correct initial order status.
- Valid status transitions.
- Rejection eligibility.
- Prevention of invalid transitions.
- Prevention of duplicate processing.
- Consistency of status across application pages.
- Accuracy of dashboard status counts.
- Consistency between displayed data and database records.

### 3.5 Status Transition Test Matrix

| Current Status | Target Status | Expected Result |
| -------------- | ------------- | --------------- |
| WAITING        | ON PROCESS    | Allowed         |
| WAITING        | REJECTED      | Allowed         |
| ON PROCESS     | COMPLETED     | Allowed         |
| ON PROCESS     | REJECTED      | Not Allowed     |
| ON PROCESS     | WAITING       | Not Allowed     |
| COMPLETED      | ON PROCESS    | Not Allowed     |
| COMPLETED      | REJECTED      | Not Allowed     |
| REJECTED       | COMPLETED     | Not Allowed     |
| REJECTED       | WAITING       | Not Allowed     |

### 4. Testing Approach

- Manual Testing
- Functional Testing
- Negative Testing
- Boundary Testing
- Regression Testing
- End-to-End Automation Testing
- API Testing (after endpoint assessment)
- Database Validation (after schema assessment)

### 5. Test Environment

- Operating System: Windows
- Web Server: XAMPP
- Application URL: http://localhost:8080
- Browser: Chromium
- Automation Framework: Playwright
- Programming Language: TypeScript

### 6. Entry Criteria

- Application is accessible.
- Required test accounts are available.
- Test environment is ready.
- Testing requirements are identified.

### 7. Exit Criteria

- Planned test cases have been executed or
  their status documented.
- Critical defects have been investigated.
- Test results are documented.
- Test summary report is prepared.

### 8. Deliverables

- Test Plan
- Test Scenarios
- Test Cases
- Test Execution Report
- Bug Reports
- Test Evidence
- Test Summary Report

### 9. Test Schedule

To be determined.

### 10. Risks and Assumptions

- Application behavior may change during testing.
- Test data must be controlled.
- Test environment must remain available.
- Test credentials must be stored securely.

### 11. Acceptance Criteria

The SIGAP application will be considered
functionally acceptable when:

1. Users can authenticate using valid credentials.
2. Unauthorized users cannot access protected administrative pages.
3. Order information is displayed correctly.
4. WAITING orders can be processed or rejected.
5. ON PROCESS orders can be completed.
6. Invalid status transitions are prevented.
7. Order status labels are displayed consistently.
8. Dashboard statistics reflect actual order data.
9. Order details match the selected order record.
10. No unresolved critical defects remain.

Final release recommendations will be based on
actual test execution results and defect analysis.
