# Test Summary Report

## 1. Document Information

| Field | Information |
|---|---|
| Project | SauceDemo E-commerce Testing |
| Application Under Test | SauceDemo |
| Testing Type | Manual Functional Testing |
| Exploratory Testing | Yes |
| Browser | Google Chrome |
| Operating System | Windows 11 |
| Test User | standard_user |
| Test Cases Executed | 35 |
| Report Status | Final |
| Defects Identified | 4 |

---

# 2. Project Overview

This project was created to simulate a real-world manual QA testing
process for an e-commerce web application.

The testing activities covered the complete functional testing lifecycle,
from requirements analysis to test execution, defect reporting,
exploratory testing, and test summary.

The main objective was to evaluate the functional behavior of the
SauceDemo application and identify defects that could affect the user
experience or the application's expected behavior.

---

# 3. Testing Scope

The following functional areas were covered:

- User Login
- Product Display
- Product Sorting
- Product Details
- Add to Cart
- Shopping Cart
- Remove Product from Cart
- Checkout Information
- Order Overview
- Order Completion
- User Logout
- Application Navigation

Additional exploratory testing was performed on:

- Shopping Cart
- Checkout
- Product availability behavior
- Checkout field validation
- Navigation
- Session behavior
- Multiple product handling
- Repeated user actions

---

# 4. Testing Activities Completed

The following QA activities were completed during the project:

1. Requirements Analysis
2. Test Planning
3. Test Scenario Design
4. Test Case Design
5. Test Data Preparation
6. Functional Test Execution
7. Defect Reporting
8. Exploratory Testing
9. Evidence Collection
10. Test Summary

---

# 5. Test Execution Summary

A total of **35 functional test cases** were executed.

| Result | Count | Percentage |
|---|---:|---:|
| PASS | 32 | 91.43% |
| FAIL | 3 | 8.57% |
| BLOCKED | 0 | 0% |
| **Total** | **35** | **100%** |

### Overall Pass Rate

**91.43%**

The pass rate was calculated based on:

**32 PASS / 35 Executed Test Cases × 100 = 91.43%**

---

# 6. Failed Test Cases

Three test cases failed during functional test execution.

| Test Case | Requirement | Scenario | Result | Jira Defect |
|---|---|---|---|---|
| TC-012 | FR-004 | SC-012 | FAIL | SCRUM-19 |
| TC-027 | FR-010 | SC-027 | FAIL | SCRUM-20 |
| TC-034 | FR-012 | SC-034 | FAIL | SCRUM-20 |

### TC-012 — Product Description

The Product Details page displayed the product name, price, image, and
Add to Cart action, but the product description was not displayed.

**Defect:** SCRUM-19

---

### TC-027 — Order Completion

The order was processed successfully, but the expected confirmation page
or confirmation message was not displayed.

**Defect:** SCRUM-20

---

### TC-034 — Complete Purchase Flow

The complete purchase flow could be completed, but the expected order
confirmation state was not displayed.

**Defect:** SCRUM-20

TC-027 and TC-034 were linked to the same Jira defect because they
represent the same underlying issue.

---

# 7. Defect Summary

A total of **4 confirmed defects** were identified during the project.

Two defects were identified during structured functional test execution,
and two additional defects were discovered during exploratory testing.

| Jira ID | Source | Summary | Severity | Priority | Status |
|---|---|---|---|---|---|
| SCRUM-19 | Functional Testing | Product description is not displayed on the Product Details page | Medium | P2 | Open |
| SCRUM-20 | Functional Testing | Order confirmation page or message is not displayed after completing an order | High | P1 | Open |
| SCRUM-21 | Exploratory Testing | Add to cart buttons are disabled for three products without availability indication | High | P1 | Open |
| SCRUM-22 | Exploratory Testing | Checkout fields accept whitespace-only values | Medium | P2 | Open |

---

# 8. Exploratory Testing Summary

Two exploratory testing sessions were completed.

## ET-001 — Shopping Cart Exploration

The session focused on:

- Adding products
- Removing products
- Re-adding products
- Shopping cart behavior
- Cart counter
- Navigation
- Empty cart behavior
- Session behavior

One confirmed defect was identified:

**SCRUM-21 — Add to cart buttons are disabled for three products without
availability indication**

Affected products:

- Sauce Labs Bolt T-Shirt
- Sauce Labs Fleece Jacket
- T-Shirt (Red)

---

## ET-002 — Checkout Exploration

The session focused on:

- Unusual customer information
- Whitespace-only values
- Checkout navigation
- Order modification
- Multiple products
- Repeated clicks
- Order review

One confirmed defect was identified:

**SCRUM-22 — Checkout fields accept whitespace-only values**

The following required fields accepted whitespace-only values:

- First Name
- Last Name
- Postal Code

The checkout process could continue despite the invalid values.

---

# 9. Defect Distribution

Defects were identified through two different testing approaches.

| Testing Approach | Defects |
|---|---:|
| Structured Functional Testing | 2 |
| Exploratory Testing | 2 |
| **Total** | **4** |

This demonstrates that exploratory testing provided additional coverage
beyond the predefined functional test cases.

---

# 10. Requirements Coverage

The functional test design covered the 12 requirements defined for the
project.

| Requirement | Description | Covered |
|---|---|---|
| FR-001 | User Login | Yes |
| FR-002 | Product Display | Yes |
| FR-003 | Product Sorting | Yes |
| FR-004 | Product Details | Yes |
| FR-005 | Add Product to Cart | Yes |
| FR-006 | Shopping Cart | Yes |
| FR-007 | Remove Product from Cart | Yes |
| FR-008 | Checkout Information | Yes |
| FR-009 | Order Overview | Yes |
| FR-010 | Complete Order | Yes |
| FR-011 | User Logout | Yes |
| FR-012 | Application Navigation | Yes |

---

# 11. Test Environment

Testing was performed using the following environment:

- **Application:** SauceDemo
- **Browser:** Google Chrome
- **Operating System:** Windows 11
- **Test Account:** standard_user

---

# 12. Test Evidence

Test evidence was collected to support the execution results and
identified defects.

Evidence is stored in:

```text
06-Evidence/
