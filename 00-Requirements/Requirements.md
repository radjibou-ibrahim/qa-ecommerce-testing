# E-commerce Application – Functional Requirements

## 1. Document Information

| Field | Details |
|---|---|
| Document ID | REQ-ECO-001 |
| Project | SauceDemo E-commerce Testing |
| Application | SauceDemo |
| Application Type | E-commerce Web Application |
| Document Type | Functional Requirements |
| Version | 1.0 |
| Status | Draft |
| Testing Approach | Manual Testing |
| Author | Radjibou Ibrahim |
| Last Updated | 2026-08-30 |

---

# 2. Purpose

The purpose of this document is to define the functional requirements used as the basis for testing the SauceDemo e-commerce web application.

These requirements describe the expected behavior of the main application functionalities and will be used to derive:

- Test Scenarios
- Test Cases
- Test Data
- Test Execution
- Defect Reports
- Regression Tests
- Test Summary

The requirements are based on the observable behavior and user flow of the SauceDemo demonstration application.

---

# 3. Application Overview

SauceDemo is a web-based e-commerce demonstration application.

The application allows users to:

1. Log in.
2. View available products.
3. Sort products.
4. View product details.
5. Add products to the shopping cart.
6. Review the shopping cart.
7. Remove products from the cart.
8. Enter checkout information.
9. Review the order.
10. Complete an order.
11. Log out.

---

# 4. Main User Journey

The primary end-to-end user journey is:

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

---

# 5. Functional Requirements

## FR-001 – User Login

### Requirement

The application shall allow a user to authenticate using a valid username and password.

### Description

A user must be able to enter login credentials and submit the login form.

When valid credentials are provided, the application should authenticate the user and provide access to the product catalog.

### Preconditions

- The application is accessible.
- The user is on the login page.
- A valid user account exists.

### Business Rules

- Username is required.
- Password is required.
- Both credentials must be valid for successful authentication.
- Invalid credentials must not provide access to the application.
- The application should provide feedback when authentication fails.

### Acceptance Criteria

- [ ] The login page is accessible.
- [ ] Username field is available.
- [ ] Password field is available.
- [ ] Login button is available.
- [ ] A user with valid credentials can log in successfully.
- [ ] A user with invalid credentials cannot access the product page.
- [ ] An appropriate error message is displayed when login fails.
- [ ] Empty required fields are validated.

### Priority

P1 – High

---

# FR-002 – Product Display

### Requirement

The application shall display the available products to an authenticated user.

### Description

After successful login, the user should be able to view the available products in the product catalog.

Each product should provide the information required for the user to identify and evaluate the product.

### Preconditions

- The application is accessible.
- The user is successfully authenticated.
- The Products page is available.

### Business Rules

- Products should be displayed in the product catalog.
- Each product should have a name.
- Each product should have a price.
- Each product should have an image.
- Each product should provide access to its details.
- An authenticated user should be able to add an available product to the cart.

### Acceptance Criteria

- [ ] The Products page is displayed after successful login.
- [ ] Available products are displayed.
- [ ] Product names are visible.
- [ ] Product prices are visible.
- [ ] Product images are displayed.
- [ ] Product actions are available.
- [ ] Products can be selected to view their details.

### Priority

P1 – High

---

# FR-003 – Product Sorting

### Requirement

The application shall allow users to sort products using the available sorting options.

### Description

Users should be able to change the order in which products are displayed.

### Preconditions

- The user is logged in.
- The Products page is displayed.
- Multiple products are available.

### Business Rules

The available sorting options should be applied to the product list.

The sorting options to be tested include:

- Name A to Z
- Name Z to A
- Price low to high
- Price high to low

### Acceptance Criteria

- [ ] The sorting control is available.
- [ ] Products can be sorted by name in ascending order.
- [ ] Products can be sorted by name in descending order.
- [ ] Products can be sorted by price from low to high.
- [ ] Products can be sorted by price from high to low.
- [ ] The displayed product order matches the selected sorting option.

### Priority

P2 – Medium

---

# FR-004 – Product Details

### Requirement

The application shall allow users to view detailed information about a selected product.

### Description

A user should be able to select a product from the product catalog and access its details.

### Preconditions

- The user is logged in.
- The Products page is displayed.
- At least one product is available.

### Business Rules

The product details page should display the relevant information associated with the selected product.

### Acceptance Criteria

- [ ] A product can be selected from the product list.
- [ ] The product details page is displayed.
- [ ] The product name is displayed.
- [ ] The product description is displayed.
- [ ] The product price is displayed.
- [ ] The product image is displayed.
- [ ] The user can add the product to the cart.
- [ ] The user can return to the product list.

### Priority

P2 – Medium

---

# FR-005 – Add Product to Cart

### Requirement

The application shall allow an authenticated user to add an available product to the shopping cart.

### Description

Users should be able to select the Add to Cart action for a product.

The selected product should then become available in the shopping cart.

### Preconditions

- The user is logged in.
- At least one product is available.
- The Products page or Product Details page is displayed.

### Business Rules

- Only available products can be added to the cart.
- Adding a product should update the cart state.
- The selected product should appear in the cart.
- The cart indicator should reflect the number of selected products when applicable.

### Acceptance Criteria

- [ ] The Add to Cart button is available for an available product.
- [ ] Clicking Add to Cart adds the product to the cart.
- [ ] The cart indicator is updated.
- [ ] The selected product appears in the cart.
- [ ] The product name in the cart matches the selected product.
- [ ] The product price in the cart matches the selected product.

### Priority

P1 – High

---

# FR-006 – Shopping Cart

### Requirement

The application shall allow users to view and review products that have been added to the shopping cart.

### Description

Users should be able to open the shopping cart and review the products selected for purchase.

### Preconditions

- The user is logged in.
- At least one product has been added to the cart.

### Business Rules

- Products added to the cart should be displayed.
- The cart should provide product information.
- The user should be able to continue shopping.
- The user should be able to proceed to checkout.

### Acceptance Criteria

- [ ] The shopping cart can be opened.
- [ ] Added products are displayed.
- [ ] Product names are displayed correctly.
- [ ] Product prices are displayed correctly.
- [ ] Product quantities are displayed correctly.
- [ ] The user can continue shopping.
- [ ] The user can proceed to checkout.

### Priority

P1 – High

---

# FR-007 – Remove Product from Cart

### Requirement

The application shall allow users to remove products from the shopping cart.

### Description

A user should be able to remove a selected product from the cart.

### Preconditions

- The user is logged in.
- At least one product is present in the cart.

### Business Rules

- The selected product should be removed from the cart.
- Removing a product should update the cart contents.
- The cart indicator should be updated when applicable.
- Removing the last product should result in an empty cart.

### Acceptance Criteria

- [ ] A Remove action is available for products in the cart.
- [ ] Clicking Remove removes the selected product.
- [ ] The removed product no longer appears in the cart.
- [ ] The cart indicator is updated.
- [ ] The cart correctly reflects an empty state when the last product is removed.

### Priority

P1 – High

---

# FR-008 – Checkout Information

### Requirement

The application shall allow users to provide the information required to proceed with checkout.

### Description

Before completing an order, the user must provide the required customer information.

### Preconditions

- The user is logged in.
- The shopping cart contains at least one product.
- The user has selected Checkout.

### Required Information

- First Name
- Last Name
- Postal Code

### Business Rules

- Required fields must be completed before the user can continue.
- Empty required fields should trigger validation.
- Valid information should allow the user to proceed to the order overview.

### Acceptance Criteria

- [ ] The checkout information page is displayed.
- [ ] First Name field is available.
- [ ] Last Name field is available.
- [ ] Postal Code field is available.
- [ ] Valid information allows the user to continue.
- [ ] Empty required fields are rejected.
- [ ] Appropriate validation messages are displayed when required information is missing.

### Priority

P1 – High

---

# FR-009 – Order Overview

### Requirement

The application shall display an order overview before the order is completed.

### Description

The user should be able to review the order information before completing the purchase.

### Preconditions

- The user is logged in.
- The cart contains at least one product.
- Valid checkout information has been provided.

### Business Rules

The order overview should reflect the products selected by the user.

The information displayed should be consistent with the cart contents.

### Acceptance Criteria

- [ ] The order overview page is displayed.
- [ ] Selected products are displayed.
- [ ] Product names are correct.
- [ ] Product prices are correct.
- [ ] Product quantities are correct.
- [ ] The order total is displayed.
- [ ] The user can review the order before completion.
- [ ] The user can complete the order.

### Priority

P1 – High

---

# FR-010 – Complete Order

### Requirement

The application shall allow users to complete an order after providing valid checkout information.

### Description

After reviewing the order, the user should be able to complete the purchase.

### Preconditions

- The user is logged in.
- At least one product is in the cart.
- Required checkout information has been provided.
- The order overview is displayed.

### Business Rules

- The order should only be completed after the required checkout information has been provided.
- The user must explicitly select the action to complete the order.
- A successful order should result in a confirmation state.

### Acceptance Criteria

- [ ] The Complete Order action is available.
- [ ] The order can be completed with valid information.
- [ ] A confirmation page or confirmation message is displayed after successful completion.
- [ ] The confirmation indicates that the order was successfully processed.
- [ ] The user can return to the product catalog after completing the order.

### Priority

P1 – High

---

# FR-011 – User Logout

### Requirement

The application shall allow an authenticated user to log out.

### Description

An authenticated user should be able to end the current session by using the Logout functionality.

### Preconditions

- The user is logged in.

### Business Rules

- Logout should terminate the current authenticated session.
- The user should no longer have access to authenticated application pages through the normal application flow.

### Acceptance Criteria

- [ ] The Logout option is available to an authenticated user.
- [ ] Clicking Logout ends the current session.
- [ ] The user is returned to the login page.
- [ ] The user cannot continue using authenticated pages without logging in again.

### Priority

P2 – Medium

---

# FR-012 – Application Navigation

### Requirement

The application shall provide functional navigation between the main pages and user actions.

### Description

Users should be able to navigate through the main e-commerce workflow without encountering unexpected navigation failures.

### Preconditions

- The application is accessible.
- The user is logged in when authentication is required.

### Business Rules

The main navigation flow should support movement between:

- Products
- Product Details
- Shopping Cart
- Checkout
- Order Overview
- Order Confirmation
- Login

### Acceptance Criteria

- [ ] Users can navigate from Products to Product Details.
- [ ] Users can navigate from Products to Shopping Cart.
- [ ] Users can return from Product Details to Products.
- [ ] Users can return from Cart to Products.
- [ ] Users can navigate from Cart to Checkout.
- [ ] Users can proceed from Checkout to Order Overview.
- [ ] Users can complete the order from the Order Overview.
- [ ] Users can return to the product catalog after completing an order.
- [ ] Users can log out from the authenticated application.

### Priority

P2 – Medium

---

# 6. Requirement Priority Definition

| Priority | Definition |
|---|---|
| P1 – High | Critical to the main e-commerce user journey or business functionality |
| P2 – Medium | Important functionality but not essential to completing the primary purchase flow |
| P3 – Low | Minor functionality or lower-impact behavior |

---

# 7. Requirement Traceability

The requirements defined in this document will be used as the basis for the following QA activities:

| Requirement | Test Scenarios | Test Cases | Test Execution | Defects |
|---|---|---|---|---|
| FR-001 | SC-001, SC-002 | TBD | TBD | TBD |
| FR-002 | SC-003 | TBD | TBD | TBD |
| FR-003 | SC-004 | TBD | TBD | TBD |
| FR-004 | SC-005 | TBD | TBD | TBD |
| FR-005 | SC-006 | TBD | TBD | TBD |
| FR-006 | SC-007 | TBD | TBD | TBD |
| FR-007 | SC-008 | TBD | TBD | TBD |
| FR-008 | SC-009 | TBD | TBD | TBD |
| FR-009 | SC-010 | TBD | TBD | TBD |
| FR-010 | SC-011 | TBD | TBD | TBD |
| FR-011 | SC-012 | TBD | TBD | TBD |
| FR-012 | SC-013 | TBD | TBD | TBD |

---

# 8. Assumptions

The following assumptions are made for this testing project:

- The application is available through the public SauceDemo environment.
- Test accounts provided by the application can be used for testing.
- The application is treated as a demonstration e-commerce application.
- Testing is performed in a controlled test environment.
- No real financial transaction is performed.
- Requirements are derived from observable application behavior and the defined testing scope.

---

# 9. Requirements Limitations

This document does not represent an official product requirements specification provided by the application owner.

The requirements are defined for QA portfolio and testing practice purposes based on the observable behavior and intended user workflow of the SauceDemo application.

Any behavior that differs from these requirements will be analyzed during testing and may be reported as a defect only when the expected behavior is sufficiently supported by the application's documented or observable behavior.

---

# 10. Document Status

**Status:** Draft

This document may be updated during the testing project if additional application behavior or requirements are identified.
