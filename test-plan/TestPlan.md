# Test Plan – Manual Testing (SauceDemo)

**Document Version:** v1.0  
**Author:** Muhammad Zohaib Aslam  
**Date:** 2026-02-07  
**Target Application:** SauceDemo  
**Application URL:** https://www.saucedemo.com/  
**Testing Type:** Manual Functional + Exploratory (with basic Regression)

---

## 1. Objective
The objective of this testing effort is to validate the core functional workflows and input validation behavior of SauceDemo through structured manual testing. The focus is on verifying that key user journeys (login, product browsing, cart management, checkout) function correctly, errors are handled properly, and defects are documented with reproducible steps and evidence screenshots.

---

## 2. Scope

### 2.1 In-Scope
- Authentication: login/logout and error handling
- Product listing: product visibility, sorting, navigation
- Product details: opening individual product pages
- Cart management: add/remove items, cart visibility, consistency of cart count badge
- Checkout workflow: user information form validation and order completion
- Basic UI checks: labels, alignment, navigation consistency
- Session behavior: access restrictions after logout, back button behavior

### 2.2 Out-of-Scope
- Performance testing (load/stress/response time benchmarking)
- Security testing (penetration testing, vulnerability assessment)
- Cross-browser/device compatibility testing (beyond the stated environment)
- API testing
- Formal accessibility compliance testing (WCAG) as a full audit

---

## 3. Test Approach

### 3.1 Functional Testing
Test cases will be designed around SauceDemo’s visible user flows and expected behavior. Each test case will include preconditions, steps, and expected results. During execution, actual results will be recorded along with Pass/Fail status.

### 3.2 Exploratory Testing
Exploratory testing will be used to identify edge cases and usability issues not explicitly covered by predefined test cases (e.g., unexpected navigation behavior, unclear error messages, UI inconsistencies). Findings will be logged as defects.

### 3.3 Regression Testing
For any failed test case or logged defect, impacted flows will be re-tested (where possible) to confirm whether behavior remains consistent after retries or navigation changes within the demo application.

---

## 4. Test Environment
- Operating System: Windows 11
- Browser: Google Chrome 144.0.7559.133
- Device: Laptop/Desktop (single device)
- Network: Standard internet connection
- Test Execution Dates: 2026-02-07 to 2026-02-21

---

## 5. Test Data

### 5.1 Accounts
SauceDemo provides standard demo accounts. Testing will use demo credentials as needed.
- Primary account: standard_user
- Negative testing accounts (as applicable): locked_out_user, problem_user, performance_glitch_user

### 5.2 Sample Input Data (Checkout)
- First Name: Test, Zohaib, Ali
- Last Name: User, Aslam, Khan
- Postal Code:
  - Valid: 12345, 74200
  - Invalid: (blank), abc, 12 (short), 12345678901234567890 (very long)

---

## 6. Entry Criteria
- SauceDemo URL is accessible
- Test environment is ready (Chrome installed and stable)
- Test plan and initial test cases are prepared
- Evidence capture method is available (screenshots)

---

## 7. Exit Criteria
- All planned test cases are executed and marked Pass/Fail
- Failed test cases are linked to a bug report OR documented with a clear reason
- At least 30 test cases are executed (target: 40)
- At least 5 defects are documented (target: 7–10) with evidence screenshots
- README summary metrics are updated with final counts

---

## 8. Deliverables
- Test Plan: `test-plan/TestPlan.md`
- Executed Test Cases: `test-cases/TestCases.md`
- Bug Report Template: `bug-reports/BugReport_Template.md`
- Logged Bug Reports: `bug-reports/bugs/BUG-XXX.md`
- Evidence Screenshots: `evidence/screenshots/BUG-XXX.png`
- Summary + Metrics: `README.md`

---

## 9. Roles and Responsibilities
- Tester / Author: Muhammad Zohaib Aslam  
  Responsibilities: test planning, test case design, manual execution, defect reporting, evidence capture, and documentation updates.

---

## 10. Risks, Assumptions, and Limitations
- SauceDemo is a demo environment and may change without notice.
- Certain behaviors may differ across accounts (e.g., locked_out_user intentionally fails login).
- Testing is limited to one browser (Chrome) and one OS (Windows 11).
- Security and performance testing are excluded; results focus on functional correctness and usability.

---

## 11. Defect Severity and Priority Guidelines

### Severity
- Critical: Blocks a core workflow (login, add-to-cart, checkout) with no workaround
- Major: Breaks an important feature but a workaround may exist
- Minor: UI/cosmetic issues, unclear messages, small validation gaps

### Priority
- High: Must be fixed immediately; impacts core use
- Medium: Should be fixed; impacts usability or secondary flows
- Low: Nice-to-have improvement or cosmetic issue

---

## 12. Naming Conventions
- Test cases: TC-001, TC-002, ...
- Bug reports: BUG-001, BUG-002, ...
- Evidence screenshots: BUG-001.png, BUG-002.png (stored in `evidence/screenshots/`)
