Test Case: Coupon Code Restriction

Scenario: User applies a discount coupon during checkout, which must follow specific usage rules.

Steps (Same for all test cases):
1. Add a product to the cart.
2. Proceed to checkout.
3. Enter the specified coupon code.
4. Click "Apply".

Test Variations

| Coupon Code   | Cart Total | User Status   | Expected Result                                      |
|---------------|------------|---------------|------------------------------------------------------|
| `WELCOME10`   | $100       | New user      | Discount applied: 10% off                            |
| `WELCOME10`   | $100       | Returning user| Error: "Coupon valid for first purchase only"        |
| `SAVE50`      | $45        | Any           | Error: "Minimum purchase of $50 required"            |
| `INVALID123`  | $120       | Any           | Error: "Invalid coupon code"                         |
| `FREESHIP`    | $80        | Any           | Free shipping applied                                |

## Acceptance Criteria
- Validate coupon existence and expiration.
- Enforce user eligibility and minimum total.
- Apply correct benefit (discount or free shipping).
