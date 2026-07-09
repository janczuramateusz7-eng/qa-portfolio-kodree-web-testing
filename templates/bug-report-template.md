
# Bug Report Template

## Summary

`[Project][Platform] Short bug summary`

Example:

`[Kodree][Android] Password exceeding maximum allowed length is accepted during sign up`

---

## Description

Describe what happened and why it is a problem.

Example:

During the registration flow on Android, the user enters a password that exceeds the maximum allowed length and tries to create an account.

The account is created successfully even though the password should not be accepted according to the test case.

---

## Environment

| Area | Details |
|---|---|
| Environment | Test / Staging / Production |
| Application |  |
| Platform | Web / Mobile Web / Mobile App |
| Device |  |
| OS |  |
| Browser / App version |  |
| Area |  |

---

## Preconditions

- User is on the correct page or screen.
- User has required test data.
- User is in the correct state, for example not logged in or logged in.

---

## Steps to reproduce

1. Open the application.
2. Navigate to the tested area.
3. Enter required test data.
4. Perform the tested action.
5. Observe the result.

---

## Expected result

Describe what should happen.

Example:

User should not be able to register with invalid data.  
A clear validation message should be displayed near the affected field.  
User should stay on the current page and be able to correct the data.

---

## Actual result

Describe what actually happens.

Example:

Account is created successfully after entering invalid data.  
User is logged in successfully.  
No validation message is displayed.

---

## Severity

Low / Medium / High / Critical

Example:

`Severity: Medium`

---

## Priority

Low / Medium / High / Critical

Example:

`Priority: Medium`

---

## Attachments

Add screenshots or screen recordings if available.

Before adding attachments to a public portfolio, remove or hide:

- email addresses,
- account data,
- private Jira links,
- internal comments,
- sensitive test data,
- personal information.

---

## Notes

Add any additional information that may help reproduce or understand the issue.
