# Exploratory Testing

## Overview

This folder contains the exploratory testing activities performed on the
SauceDemo e-commerce application.

Unlike structured testing, exploratory testing was used to investigate the
application beyond the predefined test cases and identify unexpected
behaviors that may not have been covered during the initial test design.

The exploratory sessions were guided by specific testing charters and
focused on areas such as:

- Shopping Cart
- Checkout
- Navigation
- Login and Session Management
- Product functionality

---

## Exploratory Testing Approach

Each exploratory testing session follows a simple process:

1. Define a testing charter.
2. Identify the main areas to explore.
3. Perform hands-on exploration of the application.
4. Record observations and unexpected behaviors.
5. Reproduce potential issues.
6. Determine whether an observation is a confirmed defect.
7. Create a Jira defect when appropriate.
8. Document the results of the exploratory session.

The goal is not only to find bugs, but also to understand how the
application behaves under different conditions and user actions.

---

## Test Environment

- **Application:** SauceDemo
- **Browser:** Google Chrome
- **Operating System:** Windows 11
- **Test User:** standard_user

---

## Exploratory Testing Sessions

| Session ID | Title | Area | Result | Defects |
|---|---|---|---|---|
| ET-001 | Shopping Cart Exploration | Shopping Cart | Completed | SCRUM-21 |
| ET-002 | Checkout Exploration | Checkout | Planned | - |
| ET-003 | Navigation Exploration | Navigation | Planned | - |
| ET-004 | Login & Session Exploration | Authentication | Planned | - |
| ET-005 | Product Exploration | Products | Planned | - |

---

## ET-001 — Shopping Cart Exploration

### Objective

Explore the Shopping Cart functionality to identify unexpected behaviors
related to adding, removing, and navigating between products and the
shopping cart.

### Key Findings

The session identified one confirmed defect:

**SCRUM-21 — Add to cart buttons are disabled for three products without
availability indication**

Affected products:

- Sauce Labs Bolt T-Shirt
- Sauce Labs Fleece Jacket
- T-Shirt (Red)

The buttons are visible but disabled, and no indication is displayed to
explain why the products cannot be added to the shopping cart.

Other observations did not result in defect reports because the observed
behavior was functional, expected, or could not be classified as a defect
without a defined requirement.

---

## Defect Traceability

Exploratory testing findings are linked to Jira defects when a confirmed
issue is identified.

Example:

ET-001
→ Finding
→ SCRUM-21

This provides traceability between the exploratory testing session and
the corresponding defect.

---

## Difference from Structured Testing

Exploratory testing complements the structured testing performed earlier
in the project.

| Structured Testing | Exploratory Testing |
|---|---|
| Predefined test cases | Testing charter |
| Expected results defined in advance | Results discovered during exploration |
| Planned execution | Dynamic investigation |
| Requirement-focused | Behavior-focused |
| PASS / FAIL / BLOCKED | Findings and observations |
| Reproducible test steps | Flexible test exploration |

Both approaches are used together to increase test coverage and improve
confidence in the application.

---

## Tools

- SauceDemo
- Google Chrome
- Jira
- GitHub
- Microsoft Excel

---

## Status

**Exploratory Testing:** In Progress

**Completed Sessions:** 1

**Confirmed Defects from Exploratory Testing:** 1

**Jira Defect:** SCRUM-21
