# TEST SCENARIO

## SIGAP Application

### 1. Document Information

- Project Name: SIGAP
- Document ID: TS-SIGAP-001
- Version: 1.0
- Testing Type: Manual and Automation Testing
- Application: SIGAP Web Application

---

### 2. Authentication Module

| Scenario ID | Test Scenario                                   | Priority |
| ----------- | ----------------------------------------------- | -------- |
| TS-AUTH-001 | Verify login with valid credentials             | High     |
| TS-AUTH-002 | Verify login with invalid username              | High     |
| TS-AUTH-003 | Verify login with invalid password              | High     |
| TS-AUTH-004 | Verify login with empty credentials             | High     |
| TS-AUTH-005 | Verify logout functionality                     | Medium   |
| TS-AUTH-006 | Verify unauthorized dashboard access            | High     |
| TS-AUTH-007 | Verify admin page access after logout           | High     |
| TS-AUTH-008 | Verify direct URL access without authentication | High     |

### 3. Admin Dashboard Module

| Scenario ID | Test Scenario                                      | Priority |
| ----------- | -------------------------------------------------- | -------- |
| TS-DASH-001 | Verify dashboard accessibility                     | High     |
| TS-DASH-002 | Verify Waiting order count                         | High     |
| TS-DASH-003 | Verify On Process order count                      | High     |
| TS-DASH-004 | Verify Completed order count                       | High     |
| TS-DASH-005 | Verify dashboard count consistency with order data | High     |
| TS-DASH-006 | Verify rejected order count, if displayed          | Medium   |
| TS-DASH-007 | Verify dashboard count after status transition     | High     |

### 4. Incoming Orders Module

| Scenario ID | Test Scenario                                                      | Priority |
| ----------- | ------------------------------------------------------------------ | -------- |
| TS-ORD-001  | Verify incoming orders page accessibility                          | High     |
| TS-ORD-002  | Verify order information displayed correctly                       | High     |
| TS-ORD-003  | Verify empty state when no orders exist                            | Medium   |
| TS-ORD-004  | Verify order detail navigation                                     | High     |
| TS-ORD-005  | Verify order detail matches selected order ID                      | High     |
| TS-ORD-006  | Verify order attachment download                                   | Medium   |
| TS-ORD-007  | Verify order ID uniqueness                                         | High     |
| TS-ORD-008  | Verify order information consistency between list and detail pages | High     |

### 5. Order Approval Module

| Scenario ID | Test Scenario                                       | Priority |
| ----------- | --------------------------------------------------- | -------- |
| TS-APP-001  | Verify approval of Waiting orders                   | High     |
| TS-APP-002  | Verify order transitions from Waiting to On Process | High     |
| TS-APP-003  | Verify duplicate approval prevention                | High     |
| TS-APP-004  | Verify approval confirmation modal                  | Medium   |

### 6. Order Rejection Module

| Scenario ID | Test Scenario                                         | Priority |
| ----------- | ----------------------------------------------------- | -------- |
| TS-REJ-001  | Verify rejection of Waiting orders                    | High     |
| TS-REJ-002  | Verify rejection confirmation modal                   | Medium   |
| TS-REJ-003  | Verify rejected order appears in rejected list        | High     |
| TS-REJ-004  | Verify rejected order is removed from incoming orders | High     |
| TS-REJ-005  | Verify duplicate rejection prevention                 | High     |

### 7. Order Status Module

| Scenario ID | Test Scenario                                   | Priority |
| ----------- | ----------------------------------------------- | -------- |
| TS-STAT-001 | Verify On Process orders are displayed          | High     |
| TS-STAT-002 | Verify Completed orders are displayed           | High     |
| TS-STAT-003 | Verify status labels match business status      | High     |
| TS-STAT-004 | Verify status consistency across pages          | High     |
| TS-STAT-005 | Verify invalid status transitions are prevented | High     |

---

### 8. Test Scenario Execution Strategy

The identified scenarios will be evaluated through:

1. Manual Functional Testing
2. Negative Testing
3. Data Validation Testing
4. Navigation Testing
5. Regression Testing
6. End-to-End Automation Testing

Automation candidates will be selected after
manual validation and test case development.

---

### 9. Notes

- Test scenarios are based on currently available
  application information.
- Detailed test cases will be documented separately.
- Expected behavior must be validated against
  actual application requirements and implementation.
- Unverified scenarios must not be reported as
  executed or passed.
