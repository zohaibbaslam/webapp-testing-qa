# Test Cases – SauceDemo

Format:
TC-ID | Module | Preconditions | Steps | Expected Result | Actual Result | Status | Priority

---

TC-001 | Login | User on login page | Enter valid username (standard_user) and valid password, click Login | User is logged in and redirected to Products page | User logged in successfully and Products page displayed | Pass | High

TC-002 | Login | User on login page | Enter valid username and invalid password, click Login | Error message displayed, login blocked | Error message displayed and login prevented | Pass | High

TC-003 | Login | User on login page | Enter invalid username and valid password, click Login | Error message displayed, login blocked | Error message displayed and login prevented | Pass | High

TC-004 | Login | User on login page | Leave username and password empty, click Login | Validation error message displayed | Validation error message displayed | Pass | High

TC-005 | Login | User on login page | Login using locked_out_user credentials | User is not logged in; locked user error shown | Locked user error message displayed | Pass | High

TC-006 | Login | User on login page | Enter username only, leave password empty, click Login | Validation error message displayed | Validation error message displayed | Pass | Medium

TC-007 | Login | User on login page | Enter password only, leave username empty, click Login | Validation error message displayed | Validation error message displayed | Pass | Medium

---

TC-008 | Products | Logged in | Verify Products page loads after login | Products list is displayed correctly | Products page loaded with item list | Pass | High

TC-009 | Products | Logged in | Verify product name, price, and image are visible | All product details are visible | All product details visible | Pass | Medium

TC-010 | Products | Logged in | Click product name | Product details page opens | Product details page opened | Pass | Medium

TC-011 | Products | Logged in | Sort products by Price (low to high) | Products are sorted correctly | Products sorted correctly by price | Pass | Medium

TC-012 | Products | Logged in | Sort products by Name (A to Z) | Products are sorted alphabetically | Products sorted alphabetically | Pass | Medium

TC-013 | Products | Logged in | Click menu icon and select About | About page opens in new tab/window | About page opened successfully | Pass | Low

---

TC-014 | Cart | Logged in | Click Add to Cart on a product | Product added to cart; cart badge updates | Product added and cart badge updated | Pass | High

TC-015 | Cart | Logged in | Add multiple products to cart | Cart badge shows correct item count | Cart badge updated with correct count | Pass | High

TC-016 | Cart | Logged in with items in cart | Remove product from Products page | Product removed; cart count updates | Product removed and cart count updated | Pass | High

TC-017 | Cart | Logged in with items in cart | Open Cart page | Selected products displayed correctly | Cart page displayed selected items | Pass | High

TC-018 | Cart | Logged in with items in cart | Remove item from Cart page | Item removed from cart list | Item removed successfully | Pass | High

TC-019 | Cart | Logged in | Add product, navigate away, return to cart | Cart retains added product | Cart retained product correctly | Pass | Medium

---

TC-020 | Checkout | Logged in with items in cart | Click Checkout button | User navigated to Checkout: Your Information page | Checkout information page displayed | Pass | High

TC-021 | Checkout | On checkout info page | Leave all fields empty, click Continue | Validation error displayed | Validation error message displayed | Pass | High

TC-022 | Checkout | On checkout info page | Enter First Name only, click Continue | Validation error displayed | Validation error message displayed | Pass | High

TC-023 | Checkout | On checkout info page | Enter Last Name only, click Continue | Validation error displayed | Validation error message displayed | Pass | High

TC-024 | Checkout | On checkout info page | Enter Postal Code only, click Continue | Validation error displayed | Validation error message displayed | Pass | High

TC-025 | Checkout | On checkout info page | Enter valid First Name, Last Name, and Postal Code, click Continue | User navigated to Overview page | Overview page displayed | Pass | High

TC-026 | Checkout | On overview page | Verify product details and total amount | Product and totals displayed correctly | Product details and totals displayed | Pass | High

TC-027 | Checkout | On overview page | Click Finish | Order completes successfully | Order completed successfully | Pass | High

TC-028 | Checkout | Order completed | Verify confirmation message | Confirmation message displayed | Confirmation message displayed | Pass | Medium

---

TC-029 | Navigation | Logged in | Click menu icon and select All Items | Products page is displayed | Products page displayed | Pass | Medium

TC-030 | Navigation | Logged in | Click menu icon and select Reset App State | Cart is reset; badge cleared | Cart reset and badge cleared | Pass | Medium

TC-031 | Navigation | Logged in | Click menu icon and select Logout | User logged out and redirected to login page | User logged out successfully | Pass | High

---

TC-032 | Session | Logged out | Try accessing /inventory.html directly | Access denied or redirected to login page | User redirected to login page | Pass | High

TC-033 | Session | Logged in | Logout and press browser Back button | User not allowed back into products page | User redirected to login page | Pass | High

---

TC-034 | UI | Logged in | Verify cart icon is visible on all pages | Cart icon consistently visible | Cart icon visible on all pages | Pass | Low

TC-035 | UI | Logged in | Verify footer is displayed correctly | Footer visible and aligned | Footer displayed correctly | Pass | Low

TC-036 | UI | Logged in | Verify error message readability | Error text is readable and understandable | Error text readable and clear | Pass | Low

---

TC-037 | Negative | Logged in | Enter very long text in checkout fields | Application handles input without crash | Application accepted input without crashing | Pass | Medium

TC-038 | Negative | Logged in | Enter special characters in checkout fields | Validation handled correctly | Validation message not descriptive enough | Fail (BUG-001) | Medium

TC-039 | Negative | Logged in | Refresh page during checkout | Application state handled correctly | User remains on the same checkout page after refresh | Pass | Medium

TC-040 | Negative | Logged in | Open multiple tabs and add items in each | Cart behavior remains consistent | Cart item count does not update consistently across tabs until refresh | Fail (BUG-003) | Low

TC-041 | Negative | Logged in with items in cart | Click menu → Reset App State | Cart badge should clear immediately | Cart badge does not clear until page navigation or refresh | Fail (BUG-004) | Low