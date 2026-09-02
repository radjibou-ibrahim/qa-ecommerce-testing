# ET-001 — Shopping Cart Exploration

## 1. Exploratory Testing Charter

**Charter ID:** ET-001

**Title:** Shopping Cart Exploration

**Objective:**
Explore the Shopping Cart functionality to identify unexpected behaviors
related to adding, removing, and navigating between products and the
shopping cart.

---

## 2. Test Environment

- **Application:** SauceDemo
- **Browser:** Google Chrome
- **Operating System:** Windows 11
- **User:** standard_user

---

## 3. Exploration Areas

The following areas were explored:

- Adding products to the shopping cart
- Removing products from the shopping cart
- Re-adding previously removed products
- Shopping cart counter
- Shopping cart navigation
- Cart empty state
- Session behavior after inactivity

---

## 4. Exploration Results

### Exploration 1 — Adding Multiple Products

**Action:**
Attempted to add multiple products to the shopping cart.

**Products affected:**
- Sauce Labs Bolt T-Shirt
- Sauce Labs Fleece Jacket
- T-Shirt (Red)

**Observation:**
The "Add to cart" buttons are visible but disabled for the three
products. The products cannot be added to the shopping cart.

No availability indication such as "Out of stock" or "Unavailable"
is displayed.

**Result:** Unexpected behavior

**Finding:**
The affected products are displayed in the product catalog but cannot
be added to the cart, with no explanation provided to the user.

**Defect:** SCRUM-21

---

### Exploration 2 — Cart Button Cursor

**Action:**
Verified whether the mouse cursor changes when hovering over clickable
buttons, including the Shopping Cart button.

**Observation:**
The cursor does not change when hovering over the Shopping Cart button.

However, the Shopping Cart button remains clearly identifiable and
fully usable.

**Result:** No defect identified

**Finding:**
Minor UX observation. The button remains understandable and functional.

---

### Exploration 3 — Add, Remove and Re-add Product

**Action:**
Added a product to the cart, removed it, and attempted to add the same
product again.

**Observation:**
The removed product can be added to the shopping cart again correctly.

**Result:** Expected behavior

**Finding:**
No defect identified.

---

### Exploration 4 — Session Behavior

#### Test A — Inactivity

**Action:**
Logged in and remained inactive for approximately five minutes.

**Observation:**
The session was no longer active after the inactivity period.

**Result:** Observation

**Finding:**
The application ends the session after a period of inactivity.
No defect was created because no requirement was available defining
the expected session duration.

#### Test B — Leave and Return

**Action:**
Logged in, left the website, waited for a period of time, and returned
to the application.

**Observation:**
The user was logged out and required to authenticate again.

**Result:** Observation

**Finding:**
No defect identified.

---

### Exploration 5 — Empty Shopping Cart

**Action:**
Added a product, opened the shopping cart, removed the product, and
checked the cart state and navigation.

**Observation:**
No inconsistency was observed between:

- Empty shopping cart
- Cart counter
- Products page

**Result:** Expected behavior

**Finding:**
No defect identified.

---

## 5. Findings Summary

| Exploration | Finding | Result | Defect |
|---|---|---|---|
| Adding multiple products | Three products have disabled "Add to cart" buttons without availability indication | Unexpected | SCRUM-21 |
| Cart button cursor | Cursor does not change, but button remains usable | Observation | None |
| Add → Remove → Re-add | Product can be added again correctly | Expected | None |
| Session inactivity | Session becomes inactive after approximately five minutes | Observation | None |
| Leave and return | User is logged out after leaving and returning | Observation | None |
| Empty cart | Cart state remains consistent | Expected | None |

---

## 6. Defect Identified

### SCRUM-21 — Add to Cart Buttons Disabled

**Summary:**
Add to cart buttons are disabled for three products without availability
indication.

**Affected Products:**
- Sauce Labs Bolt T-Shirt
- Sauce Labs Fleece Jacket
- T-Shirt (Red)

**Source:**
Exploratory Testing — ET-001

---

## 7. Conclusion

The exploratory session identified one confirmed defect related to
product availability and the Add to Cart functionality.

The session also produced several observations that did not result in
defect reports because the observed behavior was either functional,
expected, or could not be classified as a defect without a defined
requirement.

Exploratory testing helped identify a behavior that was not covered
by the previously designed functional test cases.

**Overall Result:** 1 confirmed defect identified.

**Jira Defect:** SCRUM-21
