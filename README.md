# Kodree Web Testing — Manual QA Portfolio

## Project overview

This repository contains manual QA testing documentation for **Kodree**, a web application tested as part of a QA internship / training project.

The main focus of this project was testing the registration and checkout flows, with special attention to validation, mobile web behavior, expected result vs actual result analysis, and bug reporting.

## Application under test

**Kodree**
Web application tested on desktop and Android mobile browser.

## Tools used

* Jira
* Xray
* Android device
* Chrome Mobile
* Chrome Desktop
* Manual testing
* Test documentation

## Testing types covered

* Functional testing
* Web testing
* Mobile web testing
* UI/UX testing
* Validation testing
* Regression testing
* Exploratory testing
* Test execution
* Bug reporting

## My role

**Junior QA Tester / Manual QA Tester**

My responsibilities included:

* executing existing test cases in Xray,
* testing the registration flow on Android mobile browser,
* testing selected checkout scenarios,
* comparing expected result with actual result,
* marking test cases as Passed or Failed,
* documenting actual results for failed tests,
* creating bug reports in Jira,
* assigning severity and priority,
* reviewing test execution results.

## Main tested areas

### Register / Sign up flow

The registration flow was tested mainly on Android mobile browser.

Tested scenarios included:

* user registration with valid data,
* password validation,
* email validation,
* registration with non-existent email address,
* registration with password exceeding maximum allowed length,
* registration with password containing special characters,
* registration with password containing spaces,
* registration with password identical to email address,
* mobile layout and usability during registration.

### Checkout flow

Selected checkout scenarios were also tested on desktop.

Tested areas included:

* selecting a course,
* selecting a subscription plan,
* entering email address,
* entering test card details,
* observing payment result,
* reporting payment-related issues.

## Example bugs found

* Password exceeding maximum allowed length is accepted during sign up.
* Password with special characters is accepted during sign up.
* Password with space characters is accepted during sign up.
* Password identical to email address is accepted during sign up.
* User is logged in after signing up with a non-existent email address.
* Payment for Lifetime Plan is declined after entering valid test card details.
* Payment for Monthly Plan is declined after entering valid test card details.

## Repository structure

```text
README.md
test-execution-summary.md
bug-reports.md
test-cases-examples.md
templates/
  bug-report-template.md
  test-case-template.md
```

## QA skills demonstrated

* Manual test execution
* Bug reporting
* Test case analysis
* Expected result vs actual result comparison
* Severity and priority assessment
* Jira/Xray workflow
* Mobile web testing
* Validation testing
* UI/UX observation
* Clear test documentation

