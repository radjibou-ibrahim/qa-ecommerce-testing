# Exploratory Testing

## Overview

This folder contains the exploratory testing activities performed on the
SauceDemo e-commerce application.

Unlike structured testing, exploratory testing was used to investigate
the application beyond the predefined test cases and identify unexpected
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
| ET-002 | Checkout Exploration | Checkout | Completed | SCRUM-22 |
| ET-003 | Navigation Exploration | Navigation | Planned | - |
| ET-004 | Login & Session Exploration | Authentication | Planned | - |
| ET-005 | Product Exploration | Products | Planned | - |

---

# ET-001 — Shopping Cart Exploration

## Objective

Explore the Shopping Cart functionality to identify unexpected behaviors
related to adding, removing, and navigating between products and the
shopping cart.

## Key Finding

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

# ET-002 — Checkout Exploration

## Objective

Explore the Checkout functionality to identify unexpected behaviors
related to customer information, validation, navigation, order review,
and order completion.

## Key Finding

The session identified one confirmed defect:

**SCRUM-22 — Checkout fields accept whitespace-only values**

The following required checkout fields accept values containing only
spaces:

- First Name
- Last Name
- Postal Code

The application allows the user to continue with the checkout process
despite these fields containing no meaningful information.

## Other Findings

The following areas were explored without identifying additional
confirmed defects:

- Unusual First Name values
- Unusual Last Name values
- Unusual Postal Code values
- Checkout navigation
- Order modification
- Multiple products
- Repeated clicks

---

## Defect Traceability

Exploratory testing findings are linked to Jira defects when a confirmed
issue is identified.

### ET-001

```text
ET-001
  ↓
Shopping Cart Exploration
  ↓
Finding
  ↓
SCRUM-21
