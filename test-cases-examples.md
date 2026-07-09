# Test Cases Examples — Kodree Web Application

## Overview

This file contains example manual test cases prepared for the Kodree web application.

The test cases are written in a clear manual QA format:

* **Action** — what the tester does,
* **Data** — what test data is used,
* **Expected Result** — what should happen.

The examples focus mainly on the **Register / Sign up** flow tested on Android mobile browser.

---

# Test Case 1: User can open registration page on Android

## Objective

Verify that the user can open the registration page on Android mobile browser.

## Environment

| Area        | Details    |
| ----------- | ---------- |
| Application | Kodree     |
| Platform    | Mobile Web |
| Device      | Android 13 |
| Browser     | Chrome     |

## Steps

| Step | Action                                  | Data       | Expected Result                                           |
| ---- | --------------------------------------- | ---------- | --------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome | Kodree URL | Main page is displayed successfully                       |
| 2    | Tap the sign up / register option       | N/A        | Registration page or registration form is displayed       |
| 3    | Verify registration form fields         | N/A        | Email and password fields are visible                     |
| 4    | Verify sign up button                   | N/A        | Sign up button is visible and tappable                    |
| 5    | Check mobile layout                     | N/A        | Registration form is displayed correctly on mobile screen |

---

# Test Case 2: User can create account with valid data

## Objective

Verify that the user can create an account using valid registration data.

## Preconditions

* User is not logged in.
* Email address is not already registered.

## Test data

| Field    | Value                                                             |
| -------- | ----------------------------------------------------------------- |
| Email    | [valid-test-user@example.com](mailto:valid-test-user@example.com) |
| Password | ValidPassword123                                                  |

## Steps

| Step | Action                                  | Data                                                              | Expected Result                                                                                            |
| ---- | --------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome | Kodree URL                                                        | Main page is displayed successfully                                                                        |
| 2    | Open the registration page              | N/A                                                               | Registration form is displayed                                                                             |
| 3    | Enter valid email address               | [valid-test-user@example.com](mailto:valid-test-user@example.com) | Email is entered correctly                                                                                 |
| 4    | Enter valid password                    | ValidPassword123                                                  | Password is entered correctly                                                                              |
| 5    | Tap the Sign up button                  | N/A                                                               | Registration request is submitted                                                                          |
| 6    | Observe the result                      | N/A                                                               | Account is created successfully or user receives email confirmation information, depending on requirements |

---

# Test Case 3: User cannot register with invalid email format

## Objective

Verify that the registration form validates incorrect email format.

## Test data

| Field    | Value            |
| -------- | ---------------- |
| Email    | invalid-email    |
| Password | ValidPassword123 |

## Steps

| Step | Action                                  | Data             | Expected Result                                            |
| ---- | --------------------------------------- | ---------------- | ---------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome | Kodree URL       | Main page is displayed successfully                        |
| 2    | Open the registration page              | N/A              | Registration form is displayed                             |
| 3    | Enter invalid email format              | invalid-email    | Invalid email is entered                                   |
| 4    | Enter valid password                    | ValidPassword123 | Password is entered correctly                              |
| 5    | Tap the Sign up button                  | N/A              | Registration is not completed                              |
| 6    | Verify validation message               | N/A              | Clear validation message is displayed near the email field |
| 7    | Verify current screen                   | N/A              | User stays on the registration page                        |

---

# Test Case 4: User cannot register with password exceeding maximum allowed length

## Objective

Verify that the registration form validates password maximum length.

## Test data

| Field    | Value                                                             |
| -------- | ----------------------------------------------------------------- |
| Email    | [valid-test-user@example.com](mailto:valid-test-user@example.com) |
| Password | VeryLongPasswordValueExceedingMaximumAllowedLength123456789       |

## Steps

| Step | Action                                          | Data                                                              | Expected Result                                                  |
| ---- | ----------------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome         | Kodree URL                                                        | Main page is displayed successfully                              |
| 2    | Open the registration page                      | N/A                                                               | Registration form is displayed                                   |
| 3    | Enter valid email address                       | [valid-test-user@example.com](mailto:valid-test-user@example.com) | Email is entered correctly                                       |
| 4    | Enter password exceeding maximum allowed length | VeryLongPasswordValueExceedingMaximumAllowedLength123456789       | Password is entered                                              |
| 5    | Tap the Sign up button                          | N/A                                                               | Registration is not completed                                    |
| 6    | Verify validation message                       | N/A                                                               | Clear validation message is displayed near the password field    |
| 7    | Verify current screen                           | N/A                                                               | User stays on the registration page and can correct the password |

---

# Test Case 5: User cannot register with password containing space characters

## Objective

Verify that the registration form validates password containing space characters.

## Test data

| Field    | Value                                                             |
| -------- | ----------------------------------------------------------------- |
| Email    | [valid-test-user@example.com](mailto:valid-test-user@example.com) |
| Password | Pass 123456                                                       |

## Steps

| Step | Action                                  | Data                                                              | Expected Result                                                  |
| ---- | --------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome | Kodree URL                                                        | Main page is displayed successfully                              |
| 2    | Open the registration page              | N/A                                                               | Registration form is displayed                                   |
| 3    | Enter valid email address               | [valid-test-user@example.com](mailto:valid-test-user@example.com) | Email is entered correctly                                       |
| 4    | Enter password with space characters    | Pass 123456                                                       | Password is entered                                              |
| 5    | Tap the Sign up button                  | N/A                                                               | Registration is not completed                                    |
| 6    | Verify validation message               | N/A                                                               | Clear validation message is displayed near the password field    |
| 7    | Verify current screen                   | N/A                                                               | User stays on the registration page and can correct the password |

---

# Test Case 6: User cannot register when password is identical to email address

## Objective

Verify that the user cannot register when the password is identical to the email address.

## Test data

| Field    | Value                                               |
| -------- | --------------------------------------------------- |
| Email    | [testuser@example.com](mailto:testuser@example.com) |
| Password | [testuser@example.com](mailto:testuser@example.com) |

## Steps

| Step | Action                                     | Data                                                | Expected Result                                                                     |
| ---- | ------------------------------------------ | --------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome    | Kodree URL                                          | Main page is displayed successfully                                                 |
| 2    | Open the registration page                 | N/A                                                 | Registration form is displayed                                                      |
| 3    | Enter valid email address                  | [testuser@example.com](mailto:testuser@example.com) | Email is entered correctly                                                          |
| 4    | Enter the same value in the password field | [testuser@example.com](mailto:testuser@example.com) | Password is entered                                                                 |
| 5    | Tap the Sign up button                     | N/A                                                 | Registration is not completed                                                       |
| 6    | Verify validation message                  | N/A                                                 | Clear validation message informs the user that password cannot be the same as email |
| 7    | Verify current screen                      | N/A                                                 | User stays on the registration page and can correct the password                    |

---

# Test Case 7: User receives information about email confirmation after signing up with non-existent email address

## Objective

Verify how the application handles registration with a non-existent email address.

## Test data

| Field    | Value                                                                           |
| -------- | ------------------------------------------------------------------------------- |
| Email    | [non-existing-user-example@test.com](mailto:non-existing-user-example@test.com) |
| Password | ValidPassword123                                                                |

## Steps

| Step | Action                                  | Data                                                                            | Expected Result                                                                     |
| ---- | --------------------------------------- | ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome | Kodree URL                                                                      | Main page is displayed successfully                                                 |
| 2    | Open the registration page              | N/A                                                                             | Registration form is displayed                                                      |
| 3    | Enter non-existent email address        | [non-existing-user-example@test.com](mailto:non-existing-user-example@test.com) | Email is entered correctly                                                          |
| 4    | Enter valid password                    | ValidPassword123                                                                | Password is entered correctly                                                       |
| 5    | Tap the Sign up button                  | N/A                                                                             | Registration is technically successful                                              |
| 6    | Observe the result                      | N/A                                                                             | System informs the user that a confirmation link has been sent to the email address |
| 7    | Verify login state                      | N/A                                                                             | User is not fully logged in until email address is confirmed                        |

---

# Test Case 8: Registration form is displayed correctly on mobile screen

## Objective

Verify that the registration form layout is displayed correctly on Android mobile browser.

## Steps

| Step | Action                                  | Data       | Expected Result                                        |
| ---- | --------------------------------------- | ---------- | ------------------------------------------------------ |
| 1    | Open Kodree main page on Android Chrome | Kodree URL | Main page is displayed successfully                    |
| 2    | Open the registration page              | N/A        | Registration form is displayed                         |
| 3    | Check email field                       | N/A        | Email field is visible and not cut off                 |
| 4    | Check password field                    | N/A        | Password field is visible and not cut off              |
| 5    | Check Sign up button                    | N/A        | Sign up button is visible and tappable                 |
| 6    | Scroll the page if needed               | N/A        | Page can be scrolled without layout issues             |
| 7    | Verify spacing and alignment            | N/A        | Form elements are aligned correctly and do not overlap |

---

# Test Case 9: Android keyboard does not block registration form fields or Sign up button

## Objective

Verify that the Android keyboard does not block important registration form elements.

## Steps

| Step | Action                                  | Data            | Expected Result                                               |
| ---- | --------------------------------------- | --------------- | ------------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome | Kodree URL      | Main page is displayed successfully                           |
| 2    | Open the registration page              | N/A             | Registration form is displayed                                |
| 3    | Tap the email field                     | N/A             | Android keyboard is displayed                                 |
| 4    | Verify email field visibility           | N/A             | Email field remains visible while typing                      |
| 5    | Tap the password field                  | N/A             | Password field is focused                                     |
| 6    | Verify password field visibility        | N/A             | Password field remains visible while typing                   |
| 7    | Verify Sign up button visibility        | N/A             | Sign up button is visible or accessible after scrolling       |
| 8    | Submit the form                         | Valid test data | User can submit the form without keyboard blocking the button |

---

# Test Case 10: User can navigate from registration page to login page

## Objective

Verify that the user can navigate from the registration page to the login page.

## Steps

| Step | Action                                    | Data       | Expected Result                                            |
| ---- | ----------------------------------------- | ---------- | ---------------------------------------------------------- |
| 1    | Open Kodree main page on Android Chrome   | Kodree URL | Main page is displayed successfully                        |
| 2    | Open the registration page                | N/A        | Registration form is displayed                             |
| 3    | Tap login link or existing account option | N/A        | User is redirected to the login page                       |
| 4    | Verify login page                         | N/A        | Login form is displayed correctly                          |
| 5    | Verify mobile layout                      | N/A        | Login page is displayed correctly on Android mobile screen |

---

# Notes

These test cases are examples of manual QA documentation created for portfolio purposes.

The focus was on:

* clear test steps,
* readable expected results,
* validation testing,
* mobile web behavior,
* Android-specific usability,
* registration flow risks.

