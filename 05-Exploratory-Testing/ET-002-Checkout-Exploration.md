# ET-002 — Checkout Exploration

## 1. Exploratory Testing Charter

**Charter ID:** ET-002

**Title:** Checkout Exploration

**Objective:**

Explore the Checkout functionality to identify unexpected behaviors
related to customer information, validation, navigation, order review,
and order completion.

---

## 2. Test Environment

- **Application:** SauceDemo
- **Browser:** Google Chrome
- **Operating System:** Windows 11
- **Test User:** standard_user

---

## 3. Exploration Areas

The following areas were explored:

- Checkout field validation
- Unusual customer information
- Whitespace-only values
- Checkout navigation
- Order modification
- Multiple products
- Repeated clicks during checkout
- Order review and total calculation

---

# 4. Exploration Results

## Exploration 1 — Unusual Data

### First Name

**Action:**

Entered unusual values in the First Name field, including numeric and
special-character values.

**Observation:**

The application accepts the entered data and the checkout process
continues normally.

**Result:**

No defect identified.

---

### Last Name

**Action:**

Entered unusual values in the Last Name field, including numeric and
special-character values.

**Observation:**

The application accepts the entered data and the checkout process
continues normally.

**Result:**

No defect identified.

---

### Postal Code

**Action:**

Entered unusual values in the Postal Code field, including alphabetic,
numeric, special-character, and long values.

**Observation:**

The application accepts the entered data and the checkout process
continues normally.

**Result:**

No defect identified.

---

## Exploration 2 — Whitespace-Only Values

**Action:**

Entered whitespace-only values in the required checkout fields.

The following fields were tested:

- First Name
- Last Name
- Postal Code

**Observation:**

The application accepts values containing only spaces.

The checkout process can continue and the order can be completed despite
the fields containing no meaningful information.

**Expected Result:**

The application should reject whitespace-only values in required
checkout fields and display an appropriate validation message.

**Actual Result:**

Whitespace-only values are accepted in First Name, Last Name, and Postal
Code fields, and the user can continue with the checkout process.

**Result:**

Unexpected behavior / Confirmed defect.

**Jira Defect:**

**SCRUM-22 — Checkout fields accept whitespace-only values**

**Severity:** Medium

**Priority:** P2

---

## Exploration 3 — Checkout Navigation

**Action:**

Navigated through the checkout process and used the Cancel button and
the browser Back button.

**Observation:**

The product remains in the shopping cart after using Cancel.

The product also remains in the shopping cart when using the browser
Back button.

**Result:**

Expected behavior.

**Finding:**

No inconsistency was observed in the shopping cart state during
navigation.

**Defect:**

None.

---

## Exploration 4 — Order Modification

**Action:**

Navigated between the shopping cart and checkout and modified the cart
contents before continuing with the checkout process.

**Observation:**

The checkout information corresponds to the actual contents of the
shopping cart.

When the cart was empty, the checkout information remained consistent
with the current cart state.

**Result:**

Expected behavior.

**Finding:**

No defect identified.

---

## Exploration 5 — Multiple Products

**Action:**

Added multiple products to the shopping cart and continued through the
checkout process.

**Observation:**

The products displayed in the Order Overview correspond to the products
in the shopping cart.

The total displayed is consistent with the sum of the selected products.

**Result:**

Expected behavior.

**Finding:**

No inconsistency was observed between the shopping cart, Order Overview,
and displayed total.

**Defect:**

None.

---

## Exploration 6 — Repeated Clicks

**Action:**

Performed repeated clicks on checkout action buttons, including Continue
and Finish.

**Observation:**

The application behaves normally when the actions are clicked repeatedly.

No duplicate or unexpected behavior was observed.

**Result:**

Expected behavior.

**Finding:**

No defect identified.

---

# 5. Findings Summary

| Exploration | Finding | Result | Defect |
|---|---|---|---|
| Unusual First Name data | Unusual values accepted | No defect identified | None |
| Unusual Last Name data | Unusual values accepted | No defect identified | None |
| Unusual Postal Code data | Unusual values accepted | No defect identified | None |
| Whitespace-only values | Required fields accept spaces only and allow checkout to continue | Unexpected | SCRUM-22 |
| Checkout navigation | Cart state remains consistent | Expected | None |
| Order modification | Checkout information remains consistent with cart | Expected | None |
| Multiple products | Products and total remain consistent | Expected | None |
| Repeated clicks | Checkout behaves normally | Expected | None |

---

# 6. Confirmed Defect

## SCRUM-22 — Checkout Fields Accept Whitespace-Only Values

**Source:** ET-002 — Checkout Exploration

**Affected Fields:**

- First Name
- Last Name
- Postal Code

**Severity:** Medium

**Priority:** P2

**Description:**

The application accepts whitespace-only values in required checkout
fields and allows the user to continue with the checkout process.

This may allow orders to be submitted with invalid or meaningless
customer information.

---

# 7. Traceability

This defect was discovered through exploratory testing rather than a
predefined functional test case.

```text
ET-002
  ↓
Checkout Exploration
  ↓
Whitespace-only values accepted
  ↓
Confirmed Defect
  ↓
SCRUM-22
