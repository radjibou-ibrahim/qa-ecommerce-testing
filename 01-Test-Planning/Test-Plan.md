# Test Plan – SauceDemo E-commerce Web Application

## 1. Document Information

| Field | Details |
|---|---|
| Test Plan ID | TP-ECO-001 |
| Project | SauceDemo E-commerce Testing |
| Application | SauceDemo |
| Application Type | E-commerce Web Application |
| Document Type | Test Plan |
| Version | 1.0 |
| Status | Draft |
| Testing Approach | Manual Testing |
| Test Level | System Testing |
| Author | QA Tester |
| Last Updated | 2026-08-30 |

---

# 2. Introduction

## 2.1 Purpose

The purpose of this Test Plan is to define the testing approach, scope, resources, environment, schedule, risks, and deliverables for the manual testing of the SauceDemo e-commerce web application.

The objective is to verify that the main e-commerce functionalities work according to the defined functional requirements and that users can successfully complete the main shopping workflow.

---

# 3. Application Under Test

## 3.1 Application Overview

SauceDemo is a web-based e-commerce demonstration application.

The application allows users to:

- Log in
- Browse products
- View product details
- Sort products
- Add products to the shopping cart
- Remove products from the cart
- Enter checkout information
- Review an order
- Complete an order
- Log out

## 3.2 Application URL

https://www.saucedemo.com/

## 3.3 Primary User Journey

The main end-to-end workflow to be tested is:

Login
    ↓
Products
    ↓
Product Details
    ↓
Add Product to Cart
    ↓
Shopping Cart
    ↓
Checkout
    ↓
Customer Information
    ↓
Order Overview
    ↓
Complete Order
    ↓
Order Confirmation

---

# 4. Test Objectives

The main objectives of testing are to:

1. Verify that users can successfully log in.
2. Verify that products are correctly displayed.
3. Verify that product sorting works correctly.
4. Verify that users can view product details.
5. Verify that products can be added to the shopping cart.
6. Verify that cart contents are displayed correctly.
7. Verify that products can be removed from the cart.
8. Verify that checkout information is correctly validated.
9. Verify that the order overview reflects the selected products.
10. Verify that users can successfully complete an order.
11. Verify that users can log out successfully.
12. Verify that the main application navigation works correctly.
13. Identify and document defects.
14. Provide clear evidence of test execution results.
15. Evaluate the overall quality of the tested functionalities.

---

# 5. Test Scope

## 5.1 In Scope

The following functionalities are included in this testing project.

### Authentication

- Login with valid credentials
- Login with invalid credentials
- Login with missing credentials
- Login validation messages
- Logout

### Product Management

- Product listing
- Product names
- Product descriptions
- Product prices
- Product images
- Product details
- Product sorting

### Shopping Cart

- Add product to cart
- View shopping cart
- Verify cart contents
- Remove product from cart
- Verify cart quantity

### Checkout

- Access checkout
- Enter customer information
- Validate required fields
- Review order
- Verify order information
- Complete order
- Verify order confirmation

### Navigation

- Products navigation
- Product details navigation
- Cart navigation
- Checkout navigation
- Return to products
- Logout navigation

---

# 6. Features Not Tested

The following areas are outside the scope of this project:

### Performance Testing

- Load testing
- Stress testing
- Volume testing
- Performance benchmarking

### Security Testing

- Penetration testing
- Vulnerability scanning
- Security assessment
- Advanced authentication security testing

### Infrastructure Testing

- Server performance
- Network infrastructure
- Server configuration
- Infrastructure monitoring

### Source Code Testing

- Code review
- Static code analysis
- Unit testing
- White-box testing

### Mobile Native Application Testing

This project focuses on the SauceDemo web application.

Native Android and iOS application testing are not included.

### Real Payment Processing

No real financial transaction will be performed.

---

# 7. Testing Strategy

The testing strategy will be primarily based on manual testing.

Testing will be performed progressively through the main user journey and individual application functionalities.

The general testing process will be:

1. Review functional requirements.
2. Identify test conditions.
3. Create test scenarios.
4. Design test cases.
5. Prepare test data.
6. Execute test cases.
7. Record test results.
8. Report defects.
9. Retest fixed defects.
10. Perform regression testing.
11. Perform exploratory testing.
12. Prepare the final test summary.

---

# 8. Testing Types

The following testing types will be performed.

## 8.1 Functional Testing

Verify that each application functionality behaves according to the defined requirements.

Examples:

- Login
- Product selection
- Add to cart
- Checkout
- Order completion

---

## 8.2 Positive Testing

Verify that the application works correctly when valid data and valid user actions are provided.

Example:

- Login using valid credentials.
- Add an available product to the cart.
- Complete checkout using valid information.

---

## 8.3 Negative Testing

Verify that the application handles invalid input and invalid user actions correctly.

Examples:

- Login with invalid credentials.
- Submit checkout without required information.
- Use incomplete form data.

---

## 8.4 Smoke Testing

A basic set of tests will be executed to determine whether the main application functionalities are stable enough for further testing.

The smoke test will include:

- Login
- Product display
- Add product to cart
- Cart access
- Checkout
- Order completion

---

## 8.5 Regression Testing

Regression testing will be performed after defects are fixed to verify that:

- The original defect has been resolved.
- Existing functionality has not been negatively affected.

---

## 8.6 Exploratory Testing

Exploratory testing will be performed to discover unexpected behavior that may not be covered by predefined test cases.

The tester will explore the application using different user actions, navigation paths, and combinations of inputs.

---

## 8.7 End-to-End Testing

The complete shopping journey will be tested from login through order completion.

The primary E2E flow is:

Login → Products → Cart → Checkout → Order Overview → Complete Order

---

# 9. Test Levels

The primary test level for this project is:

## System Testing

The application will be tested as a complete system from the user's perspective.

The focus will be on verifying the behavior of integrated application functionalities.

---

# 10. Test Environment

## 10.1 Hardware

| Component | Configuration |
|---|---|
| Device | Laptop/Desktop |
| Operating System | Windows 11 |
| Internet Connection | Stable Internet Connection |

## 10.2 Browsers

The following browsers will be considered for testing:

- Google Chrome
- Microsoft Edge

The primary browser for initial testing will be Google Chrome.

## 10.3 Tools

| Tool | Purpose |
|---|---|
| GitHub | Test documentation and project version control |
| Jira | Defect tracking |
| Microsoft Excel / Google Sheets | Test cases and execution results |
| Browser DevTools | Basic investigation and troubleshooting |
| Postman | API testing exercises where applicable |
| SQL | Database testing exercises where applicable |

---

# 11. Test Data

The following categories of test data will be used:

### Valid Login Data

Valid credentials provided by the SauceDemo test environment.

### Invalid Login Data

Examples:

- Invalid username
- Invalid password
- Empty username
- Empty password
- Both fields empty

### Product Data

Products available in the SauceDemo application.

### Checkout Data

Example valid data:

- First Name: John
- Last Name: Doe
- Postal Code: 10001

### Invalid Checkout Data

Examples:

- Empty First Name
- Empty Last Name
- Empty Postal Code
- All required fields empty

Test credentials and test data will be documented separately where appropriate.

---

# 12. Entry Criteria

Testing can begin when the following conditions are met:

- The SauceDemo application is accessible.
- The test environment is available.
- The main application functionalities are accessible.
- Test requirements have been reviewed.
- Test scope has been defined.
- Test scenarios have been prepared.
- Test cases have been prepared.
- Required test data is available.
- The test environment is stable enough for testing.

---

# 13. Exit Criteria

Testing will be considered complete when:

- All planned test cases have been executed.
- Critical and high-priority test cases have been completed.
- Test results have been documented.
- Identified defects have been documented.
- Critical defects have been investigated.
- Required regression testing has been completed.
- Test evidence has been collected.
- The final test summary report has been prepared.

Testing may also be stopped if a blocking issue prevents meaningful execution.

---

# 14. Pass / Fail Criteria

## PASS

A test case is considered PASS when:

- The actual result matches the expected result.
- No unexpected behavior is observed.

## FAIL

A test case is considered FAIL when:

- The actual result differs from the expected result.
- The observed behavior violates a defined requirement.

## BLOCKED

A test case is considered BLOCKED when:

- Testing cannot be completed because of another defect, environment issue, missing data, or unavailable functionality.

## NOT RUN

A test case is considered NOT RUN when:

- The test has not yet been executed.

---

# 15. Defect Management

Identified defects will be documented using a structured bug report.

Each bug report should include:

- Bug ID
- Summary
- Environment
- Preconditions
- Steps to Reproduce
- Expected Result
- Actual Result
- Severity
- Priority
- Evidence

Defects will be tracked using Jira where applicable.

---

# 16. Severity Definition

| Severity | Definition |
|---|---|
| Critical | The defect prevents a core functionality from working or causes a major system failure. |
| High | The defect significantly affects an important functionality or user journey. |
| Medium | The defect affects functionality but a workaround may exist. |
| Low | The defect has limited functional or visual impact. |

---

# 17. Priority Definition

| Priority | Definition |
|---|---|
| P1 – High | The defect should be addressed as soon as possible because it affects critical functionality. |
| P2 – Medium | The defect should be fixed but does not immediately block the main user journey. |
| P3 – Low | The defect has a low business impact and can be addressed later. |

---

# 18. Risks

The following risks have been identified.

| Risk | Impact | Probability | Mitigation |
|---|---|---|---|
| Application becomes unavailable | High | Medium | Retry testing later and document environment availability. |
| Test environment changes | Medium | Medium | Record environment information for each test execution. |
| Application behavior differs from expected behavior | High | Medium | Review requirements and document the observed behavior. |
| Limited testing time | Medium | Medium | Prioritize P1 functionalities and critical user journeys. |
| Test data becomes unavailable | Medium | Low | Maintain reusable test data. |
| Defects prevent further testing | High | Medium | Report blocking defects and execute unaffected test cases where possible. |
| Browser-specific behavior | Medium | Medium | Test the application using multiple supported browsers where possible. |

---

# 19. Test Deliverables

The following deliverables will be produced during the project:

### Requirements

- Functional Requirements Document

### Test Planning

- Test Plan

### Test Design

- Test Scenarios
- Test Cases
- Test Data

### Test Execution

- Test Execution Results
- Test Evidence

### Defect Management

- Bug Reports
- Jira Defects

### Exploratory Testing

- Exploratory Testing Report

### Final Reporting

- Test Summary Report

---

# 20. Roles and Responsibilities

## QA Tester

Responsibilities include:

- Analyze requirements.
- Define test conditions.
- Create test scenarios.
- Design test cases.
- Prepare test data.
- Execute tests.
- Identify defects.
- Report defects.
- Perform retesting.
- Perform regression testing.
- Document results.
- Prepare the final test summary.

## Developer

For this portfolio project, no development team is directly assigned.

If a defect is identified, the defect will be documented as it would be in a real project.

---

# 21. Test Schedule

The project will be completed progressively.

| Phase | Activity | Status |
|---|---|---|
| Phase 1 | Requirements Analysis | Completed |
| Phase 2 | Test Planning | In Progress |
| Phase 3 | Test Scenario Design | Planned |
| Phase 4 | Test Case Design | Planned |
| Phase 5 | Test Data Preparation | Planned |
| Phase 6 | Test Execution | Planned |
| Phase 7 | Bug Reporting | Planned |
| Phase 8 | Retesting | Planned |
| Phase 9 | Regression Testing | Planned |
| Phase 10 | Exploratory Testing | Planned |
| Phase 11 | Final Test Summary | Planned |

---

# 22. Requirements Traceability

The test activities will be linked to the functional requirements defined in the Requirements Document 
👉 [View Functional Requirements](./00-Requirements/Requirements.md).

| Requirement | Feature | Planned Test Coverage |
|---|---|---|
| FR-001 | User Login | Functional, Positive, Negative |
| FR-002 | Product Display | Functional, UI |
| FR-003 | Product Sorting | Functional |
| FR-004 | Product Details | Functional, Navigation |
| FR-005 | Add Product to Cart | Functional, E2E |
| FR-006 | Shopping Cart | Functional, E2E |
| FR-007 | Remove Product | Functional |
| FR-008 | Checkout Information | Functional, Negative |
| FR-009 | Order Overview | Functional, E2E |
| FR-010 | Complete Order | Functional, E2E |
| FR-011 | User Logout | Functional |
| FR-012 | Application Navigation | Functional, Navigation |

---

# 23. Test Prioritization

Testing will be prioritized according to business importance and impact on the main user journey.

## P1 – Highest Priority

- Login
- Product display
- Add to cart
- Shopping cart
- Checkout
- Order overview
- Order completion

## P2 – Medium Priority

- Product sorting
- Product details
- Logout
- General navigation

The primary end-to-end purchase workflow will receive the highest testing priority.

---

# 24. Testing Limitations

This project has the following limitations:

- Testing is performed on a demonstration application.
- No access to production systems is available.
- No real payment transactions are performed.
- Performance testing is not included.
- Advanced security testing is not included.
- Native mobile application testing is not included.
- API and database testing are not assumed to be part of the SauceDemo application unless appropriate interfaces or access are available.

---

# 25. Final Test Objective

The final objective of this project is to provide evidence that the main SauceDemo e-commerce workflow has been systematically tested.

The project will demonstrate the ability to:

- Analyze requirements.
- Plan testing activities.
- Design test scenarios and test cases.
- Execute tests.
- Identify and report defects.
- Perform retesting and regression testing.
- Document testing results.
- Communicate the overall quality status of the application.

---

# 26. Document Approval

| Role | Name | Status |
|---|---|---|
| QA Tester | QA Portfolio Project | Draft |
| Reviewer | N/A | Pending |

---

# 27. Document History

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-08-30 | QA Tester | Initial Test Plan created |
