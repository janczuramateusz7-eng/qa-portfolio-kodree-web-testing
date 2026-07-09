
# Test Execution Summary — Kodree Register Android

## Project

**Kodree Web Application**

## Task

**Kodree Register — Execute TCs Android**

## Objective

The objective of this task was to execute existing manual test cases for the Kodree registration flow on Android mobile browser.

The main goal was to verify whether the registration flow works correctly on mobile and whether the actual application behavior matches the expected results defined in the test cases.

## Scope

The test execution focused on the **Register / Sign up** flow.

Tested areas included:

* opening the registration page on Android,
* entering valid registration data,
* email field validation,
* password field validation,
* registration with invalid password formats,
* registration with non-existent email address,
* checking validation messages,
* checking whether the user is logged in after registration,
* mobile web behavior on Android Chrome.

## Environment

| Area                 | Details        |
| -------------------- | -------------- |
| Application          | Kodree         |
| Platform             | Mobile Web     |
| Device               | Android 13     |
| Browser              | Chrome         |
| Test Management Tool | Xray           |
| Bug Tracking Tool    | Jira           |
| Test Type            | Manual testing |

## Test execution approach

Each test case was executed manually on Android mobile browser.

For every test case, I followed the steps defined in Xray:

* **Action** — what should be done,
* **Data** — what test data should be used,
* **Expected Result** — what should happen after the action.

During execution, I compared the **Expected Result** with the **Actual Result**.

## Test status rules

| Status | Meaning                                              |
| ------ | ---------------------------------------------------- |
| Passed | Actual result matched the expected result            |
| Failed | Actual result was different from the expected result |

## Main focus during execution

The main focus was validation testing in the registration flow.

I checked whether the application correctly handles invalid input and whether it prevents account creation when the test case expected the input to be rejected.

The most important validation areas were:

* password maximum length,
* password with special characters,
* password with space characters,
* password identical to email address,
* non-existent email address,
* missing or unclear validation messages.

## Main findings

During test execution, several issues were found in the registration flow.

In multiple cases, the application accepted data that should have been rejected according to the test case expected result.

The most important findings were:

1. Account was created with a password exceeding the maximum allowed length.
2. Account was created with a password containing special characters.
3. Account was created with a password containing space characters.
4. Account was created when the password was identical to the email address.
5. User was logged in after signing up with a non-existent email address.

## Reported bugs

| Bug Summary                                                          | Severity | Priority |
| -------------------------------------------------------------------- | -------- | -------- |
| Password exceeding maximum allowed length is accepted during sign up | High     | High     |
| Password with special characters is accepted during sign up          | Medium   | Medium   |
| Password with space characters is accepted during sign up            | Medium   | Medium   |
| Password identical to email address is accepted during sign up       | Medium   | Medium   |
| User is logged in after signing up with a non-existent email address | High     | High     |

## Example actual result

Example of an actual result documented during failed test execution:

```text
Account is created successfully after entering a password that exceeds the maximum allowed length.

User is logged in successfully after registration.

No validation message is displayed near the password field.
```

## QA observations

The test execution showed that the registration flow allowed some invalid inputs that should have been blocked according to the test cases.

From a QA perspective, the most important risks were:

* weak or missing password validation,
* missing validation messages,
* user being logged in when confirmation or validation was expected,
* possible inconsistency between test case expected results and actual application behavior.

## What I practiced

During this task, I practiced:

* manual test execution,
* working with existing test cases,
* using Xray Test Execution,
* comparing expected result with actual result,
* documenting failed test results,
* creating bug reports in Jira,
* assigning severity and priority,
* mobile web testing on Android,
* validation testing,
* clear QA documentation.

## Summary

This test execution helped verify the Kodree registration flow on Android mobile browser.

The main outcome was identifying validation-related issues in the sign up process and documenting them as bug reports with clear steps to reproduce, expected results, actual results, severity and priority.
