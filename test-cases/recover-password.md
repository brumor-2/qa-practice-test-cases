Test Case: Recover Password Validation

Scenario: User requests a password reset by providing an email address.

Steps (Same for all test cases):
1. Access the "Forgot Password" page.
2. Enter the specified email in the field.
3. Click "Recover Password".

Test Variations:

| Email Input               | Expected Result                                |
|-------------------------- |------------------------------------------------|
| Valid registered email    | Success message: "Password reset sent"         |
| Unregistered email        | Error: "Email not found"                       |
| Empty field               | Error: "Email field is required"               |
| Invalid format (`abc.com`)| Error: "Enter a valid email address"           |

## Acceptance Criteria
- Email must be valid format.
- Must check if email is registered.
- Display clear success/error messages.

