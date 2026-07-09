
# Bug Reports — Kodree Web Application

## Overview

This file contains example bug reports created during manual testing of the Kodree web application.

The reported issues were found during test execution of the **Register / Sign up** flow on Android mobile browser and selected checkout scenarios on desktop.

Each bug report includes:

* summary,
* description,
* environment,
* preconditions,
* steps to reproduce,
* expected result,
* actual result,
* severity,
* priority.

---

# Bug 1: Password exceeding maximum allowed length is accepted during sign up

## Summary

`[Kodree][Android] Password exceeding maximum allowed length is accepted during sign up`

## Severity

High

## Priority

High

## Description

During the registration flow on Android, the user enters a password that exceeds the maximum allowed length and tries to create an account.

The account is created successfully even though the password should not be accepted due to exceeding the maximum allowed length.

## Environment

| Area        | Details                |
| ----------- | ---------------------- |
| Environment | Test                   |
| Device      | Android 13             |
| Browser     | Chrome                 |
| Platform    | Mobile Web             |
| Area        | Registration / Sign up |

## Preconditions

* User is not logged in.
* User is on the Kodree registration page.
* User uses a valid email address that is not registered in Kodree.

## Steps to reproduce

1. Open Kodree main page on Android Chrome.
2. Open the registration page.
3. Enter a valid email address that is not registered in Kodree.
4. Enter a password that exceeds the maximum allowed length.
5. Tap the **Sign up** button.
6. Observe the result.

## Expected result

User should not be able to register with a password that exceeds the maximum allowed length.

A clear validation message should be displayed near the password field, for example:

`Password is too long`

or

`Password must be less than X characters`

User should stay on the registration page and be able to correct the password.

## Actual result

Account is created successfully after entering a password that exceeds the maximum allowed length.

User is logged in successfully after registration.

No validation message is displayed near the password field.

The application accepts a password that should be rejected according to the maximum length validation.

---

# Bug 2: Password with special characters is accepted during sign up

## Summary

`[Kodree][Android] Password with special characters is accepted during sign up`

## Severity

Medium

## Priority

Medium

## Description

During the registration flow on Android, the user enters a password that contains special characters and tries to create an account.

The account is created successfully even though the password with special characters should not be accepted according to the test case.

## Environment

| Area        | Details                |
| ----------- | ---------------------- |
| Environment | Test                   |
| Device      | Android 13             |
| Browser     | Chrome                 |
| Platform    | Mobile Web             |
| Area        | Registration / Sign up |

## Preconditions

* User is not logged in.
* User is on the Kodree registration page.
* User uses a valid email address that is not registered in Kodree.

## Steps to reproduce

1. Open Kodree main page on Android Chrome.
2. Open the registration page.
3. Enter a valid email address that is not registered in Kodree.
4. Enter password with special characters, for example: `Pass!@#123`.
5. Tap the **Sign up** button.
6. Observe the result.

## Expected result

User should not be able to register with a password that contains special characters.

A clear validation message should be displayed near the password field, informing the user that special characters are not allowed.

User should stay on the registration page and be able to correct the password.

## Actual result

Account is created successfully after entering a password with special characters: `Pass!@#123`.

User is logged in successfully after registration.

No validation message is displayed near the password field.

The application accepts a password that should be rejected according to the test case.

---

# Bug 3: Password with space characters is accepted during sign up

## Summary

`[Kodree][Android] Password with space characters is accepted during sign up`

## Severity

Medium

## Priority

Medium

## Description

During the registration flow on Android, the user enters a password that contains space characters and tries to create an account.

The account is created successfully even though the password with space characters should not be accepted according to the test case.

## Environment

| Area        | Details                |
| ----------- | ---------------------- |
| Environment | Test                   |
| Device      | Android 13             |
| Browser     | Chrome                 |
| Platform    | Mobile Web             |
| Area        | Registration / Sign up |

## Preconditions

* User is not logged in.
* User is on the Kodree registration page.
* User uses a valid email address that is not registered in Kodree.

## Steps to reproduce

1. Open Kodree main page on Android Chrome.
2. Open the registration page.
3. Enter a valid email address that is not registered in Kodree.
4. Enter password with space characters, for example: `Pass 123456`.
5. Tap the **Sign up** button.
6. Observe the result.

## Expected result

User should not be able to register with a password that contains space characters.

A clear validation message should be displayed near the password field, informing the user that space characters are not allowed.

User should stay on the registration page and be able to correct the password.

## Actual result

Account is created successfully after entering a password with space characters.

User is logged in successfully after registration.

No validation message is displayed near the password field.

The application accepts a password that should be rejected according to the test case.

---

# Bug 4: Password identical to email address is accepted during sign up

## Summary

`[Kodree][Android] Password identical to email address is accepted during sign up`

## Severity

Medium

## Priority

Medium

## Description

During the registration flow on Android, the user enters the same value in the email field and password field, then tries to create an account.

The account is created successfully even though the password identical to the email address should not be accepted according to the test case.

## Environment

| Area        | Details                |
| ----------- | ---------------------- |
| Environment | Test                   |
| Device      | Android 13             |
| Browser     | Chrome                 |
| Platform    | Mobile Web             |
| Area        | Registration / Sign up |

## Preconditions

* User is not logged in.
* User is on the Kodree registration page.
* User uses a valid email address that is not registered in Kodree.

## Steps to reproduce

1. Open Kodree main page on Android Chrome.
2. Open the registration page.
3. Enter a valid email address that is not registered in Kodree.
4. Enter the same value in the password field as in the email field.
5. Tap the **Sign up** button.
6. Observe the result.

## Expected result

User should not be able to register when the password is identical to the email address.

A clear validation message should be displayed near the password field, informing the user that the password cannot be the same as the email address.

User should stay on the registration page and be able to correct the password.

## Actual result

Account is created successfully after entering a password identical to the email address.

User is logged in successfully after registration.

No validation message is displayed near the password field.

The application accepts a password that should be rejected according to the test case.

---

# Bug 5: User is logged in after signing up with non-existent email address

## Summary

`[Kodree][Android] User is logged in after signing up with non-existent email address`

## Severity

High

## Priority

High

## Description

During the registration flow on Android, the user enters a non-existent email address and a valid password, then tries to create an account.

The registration is completed and the user is logged in successfully, even though the system should inform the user that a confirmation link has been sent to the email address.

Since the email address does not exist, the user should not be able to verify the account.

## Environment

| Area        | Details                |
| ----------- | ---------------------- |
| Environment | Test                   |
| Device      | Android 13             |
| Browser     | Chrome                 |
| Platform    | Mobile Web             |
| Area        | Registration / Sign up |

## Preconditions

* User is not logged in.
* User is on the Kodree registration page.
* User uses a non-existent email address.

## Steps to reproduce

1. Open Kodree main page on Android Chrome.
2. Open the registration page.
3. Enter a non-existent email address.
4. Enter a valid password.
5. Tap the **Sign up** button.
6. Observe the result.

## Expected result

Registration should be technically successful without validation errors on the form.

The system should inform the user that a confirmation link has been sent to the provided email address.

User should not be fully logged in until the email address is confirmed.

## Actual result

Account is created successfully after entering a non-existent email address.

User is logged in successfully after registration.

No clear information about email confirmation is displayed.

The application allows the user to access the account without confirming the email address.

---

# Bug 6: Payment for Lifetime Plan is declined after entering valid test card details

## Summary

`[Kodree][Desktop] Payment for Lifetime Plan is declined after entering valid test card details`

## Severity

High

## Priority

High

## Description

During the checkout flow, the user selects the Lifetime Plan, enters a valid email address and valid test card details, but the payment is declined.

As a result, the user cannot complete the Lifetime Plan purchase flow.

## Environment

| Area        | Details            |
| ----------- | ------------------ |
| Environment | Test               |
| Device      | Desktop            |
| OS          | Windows 11         |
| Browser     | Chrome             |
| Platform    | Web                |
| Area        | Checkout / Payment |

## Preconditions

* User uses a valid email address.
* User has valid test card details.
* User is on Kodree main page.

## Steps to reproduce

1. Open Kodree main page.
2. Click **Catalog**.
3. Select any available course.
4. Click **Get started**.
5. Select **Lifetime Plan**.
6. Enter a valid email address.
7. Click **Continue**.
8. Wait until the payment modal is displayed.
9. Enter valid test card details.
10. Submit the payment.
11. Observe the result.

## Expected result

Payment for the Lifetime Plan should be processed successfully after entering a valid email address and valid test card details.

User should be able to complete the purchase flow.

## Actual result

Payment is declined.

The following error message is displayed:

`Your card has been declined. Please try again, or use a different payment method.`

User cannot complete the Lifetime Plan purchase flow.

---

# Bug 7: Payment for Monthly Plan is declined after entering valid test card details

## Summary

`[Kodree][Desktop] Payment for Monthly Plan is declined after entering valid test card details`

## Severity

High

## Priority

High

## Description

During the checkout flow, the user selects the Monthly Plan, enters a valid email address and valid test card details, but the payment is declined.

As a result, the user cannot complete the Monthly Plan purchase flow.

## Environment

| Area        | Details            |
| ----------- | ------------------ |
| Environment | Test               |
| Device      | Desktop            |
| OS          | Windows 11         |
| Browser     | Chrome             |
| Platform    | Web                |
| Area        | Checkout / Payment |

## Preconditions

* User uses a valid email address.
* User has valid test card details.
* User is on Kodree main page.

## Steps to reproduce

1. Open Kodree main page.
2. Click **Catalog**.
3. Select any available course.
4. Click **Get started**.
5. Select **Monthly Plan**.
6. Enter a valid email address.
7. Click **Continue**.
8. Wait until the payment modal is displayed.
9. Enter valid test card details.
10. Submit the payment.
11. Observe the result.

## Expected result

Payment for the Monthly Plan should be processed successfully after entering a valid email address and valid test card details.

User should be able to complete the purchase flow.

## Actual result

Payment is declined.

The following error message is displayed:

`Your card has been declined. Please try again, or use a different payment method.`

User cannot complete the Monthly Plan purchase flow.

---

# Notes

These bug reports were created for portfolio purposes based on manual QA work.

The main focus was to show clear bug documentation, including:

* reproducible steps,
* expected result,
* actual result,
* severity,
* priority,
* affected area,
* test environment.
