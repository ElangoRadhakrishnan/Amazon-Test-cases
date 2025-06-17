Module Name: User Login

Test Id: UL-001
Test Scenario: Valid Login
- Pre-requisites: User is registered on Amazon.
- Test Data: Valid email and password.
- Steps:
  1. Go to Amazon login page.
  2. Enter valid email and password.
  3. Click 'Sign In'.
- Expected Result: User is logged in and redirected to the home page.
- Actual Result: User successfully logged in and redirected to home page.
- Status: Pass

Test Id: UL-002
Test Scenario: Invalid Login
- Pre-requisites: User is registered on Amazon.
- Test Data: Invalid email and/or password.
- Steps:
  1. Go to Amazon login page.
  2. Enter invalid email and/or password.
  3. Click 'Sign In'.
- Expected Result: Error message is displayed and user is not logged in.
- Actual Result: Error message "Incorrect email or password" displayed, user not logged in.
- Status: Pass

Test Id: UL-003
Test Scenario: Empty Fields
- Pre-requisites: None.
- Test Data: None.
- Steps:
  1. Go to Amazon login page.
  2. Leave email and password fields blank.
  3. Click 'Sign In'.
- Expected Result: Error message is displayed indicating required fields.
- Actual Result: Error message "Enter your email and password" displayed.
- Status: Pass

Test Id: UL-004
Test Scenario: Password Reset
- Pre-requisites: User is registered on Amazon.
- Test Data: Registered email address.
- Steps:
  1. Go to Amazon login page.
  2. Click on 'Forgot Password'.
  3. Enter registered email address.
  4. Follow the instructions to reset password.
- Expected Result: Password reset instructions are sent to the registered email.
- Actual Result: Password reset email received and able to reset password.
- Status: Pass

Test Id: UL-005
Test Scenario: Account Lockout After Multiple Failed Attempts
- Pre-requisites: User is registered on Amazon.
- Test Data: Invalid password.
- Steps:
  1. Go to Amazon login page.
  2. Enter valid email and invalid password multiple times (5 times).
- Expected Result: Account is temporarily locked and user is notified.
- Actual Result: Account locked after 5 failed attempts, notification displayed.
- Status: Pass

Test Id: UL-006
Test Scenario: Login with Unregistered Email
- Pre-requisites: None.
- Test Data: Unregistered email and any password.
- Steps:
  1. Go to Amazon login page.
  2. Enter unregistered email and any password.
  3. Click 'Sign In'.
- Expected Result: Error message is displayed indicating account does not exist.
- Actual Result: Error message "Account does not exist" displayed.
- Status: Pass

---

Module Name: Product Search

Test Id: PS-001
Test Scenario: Valid Product Search
- Pre-requisites: User is logged in.
- Test Data: "iPhone"
- Steps:
  1. Enter "iPhone" in the search bar.
  2. Click the search button.
- Expected Result: Product results for "iPhone" are displayed.
- Actual Result: List of iPhone products displayed.
- Status: Pass

Test Id: PS-002
Test Scenario: Invalid Product Search
- Pre-requisites: User is logged in.
- Test Data: "xyznotfound"
- Steps:
  1. Enter "xyznotfound" in the search bar.
  2. Click the search button.
- Expected Result: "No results found" message is displayed.
- Actual Result: "No results found" message displayed.
- Status: Pass

Test Id: PS-003
Test Scenario: Empty Search
- Pre-requisites: User is logged in.
- Test Data: None.
- Steps:
  1. Leave the search bar empty.
  2. Click the search button.
- Expected Result: Prompt to enter a search term is displayed.
- Actual Result: Prompt "Please enter a search term" displayed.
- Status: Pass

Test Id: PS-004
Test Scenario: Search with Filters
- Pre-requisites: User is logged in.
- Test Data: "iPhone", filter by price range.
- Steps:
  1. Enter "iPhone" in the search bar.
  2. Apply price filter.
  3. Click the search button.
- Expected Result: Only products within the selected price range are displayed.
- Actual Result: Only iPhone products within selected price range displayed.
- Status: Pass

Test Id: PS-005
Test Scenario: Search with Special Characters
- Pre-requisites: User is logged in.
- Test Data: "@#$%^&*"
- Steps:
  1. Enter special characters in the search bar.
  2. Click the search button.
- Expected Result: Appropriate message is displayed or no results are shown.
- Actual Result: "No results found" message displayed.
- Status: Pass

Test Id: PS-006
Test Scenario: Search with Category Selection
- Pre-requisites: User is logged in.
- Test Data: "iPhone", select "Electronics" category.
- Steps:
  1. Select "Electronics" from category dropdown.
  2. Enter "iPhone" in the search bar.
  3. Click the search button.
- Expected Result: Only "iPhone" products from Electronics category are displayed.
- Actual Result: Only iPhone products from Electronics category displayed.
- Status: Pass

---

Module Name: Add to Cart

Test Id: AC-001
Test Scenario: Add Valid Product
- Pre-requisites: User is logged in.
- Test Data: "iPhone"
- Steps:
  1. Search for "iPhone".
  2. Select a product from the results.
  3. Click 'Add to Cart'.
- Expected Result: Product is added to cart and confirmation is shown.
- Actual Result: Product added to cart, confirmation message displayed.
- Status: Pass

Test Id: AC-002
Test Scenario: Add Out-of-Stock Product
- Pre-requisites: User is logged in.
- Test Data: Out-of-stock product.
- Steps:
  1. Search and select an out-of-stock product.
  2. Click 'Add to Cart'.
- Expected Result: Error message is shown or 'Add to Cart' button is disabled.
- Actual Result: 'Add to Cart' button disabled for out-of-stock product.
- Status: Pass

Test Id: AC-003
Test Scenario: Add Same Product Multiple Times
- Pre-requisites: User is logged in.
- Test Data: "iPhone"
- Steps:
  1. Add the same product to the cart multiple times.
- Expected Result: Product quantity increases in the cart.
- Actual Result: Product quantity increased in cart as expected.
- Status: Pass

Test Id: AC-004
Test Scenario: Add Product Without Selecting Required Options
- Pre-requisites: User is logged in.
- Test Data: Product with size/color options.
- Steps:
  1. Search for a product with required options (e.g., size, color).
  2. Try to add to cart without selecting options.
- Expected Result: User is prompted to select required options.
- Actual Result: Prompt displayed to select required options.
- Status: Pass

Test Id: AC-005
Test Scenario: Add Product When Not Logged In
- Pre-requisites: User is not logged in.
- Test Data: Any product.
- Steps:
  1. Search for a product.
  2. Click 'Add to Cart'.
- Expected Result: User is prompted to log in or sign up.
- Actual Result: User prompted to log in before adding to cart.
- Status: Pass

---

Module Name: Cart Validation

Test Id: CV-001
Test Scenario: Empty Cart
- Pre-requisites: User is logged in.
- Test Data: None.
- Steps:
  1. Go to the cart page without adding any items.
- Expected Result: Message "Your cart is empty" is displayed.
- Actual Result: "Your cart is empty" message displayed.
- Status: Pass

Test Id: CV-002
Test Scenario: Cart with Items
- Pre-requisites: User is logged in and has added items to the cart.
- Test Data: "iPhone"
- Steps:
  1. Add a product to the cart.
  2. Go to the cart page.
- Expected Result: The added product is listed in the cart.
- Actual Result: Added product listed in the cart.
- Status: Pass

Test Id: CV-003
Test Scenario: Remove Item from Cart
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: "iPhone"
- Steps:
  1. Add a product to the cart.
  2. Go to the cart page.
  3. Remove the product from the cart.
- Expected Result: Product is removed and cart is updated.
- Actual Result: Product removed, cart updated accordingly.
- Status: Pass

Test Id: CV-004
Test Scenario: Update Quantity in Cart
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: "iPhone"
- Steps:
  1. Add a product to the cart.
  2. Go to the cart page.
  3. Change the quantity of the product.
- Expected Result: Cart updates the total price and quantity accordingly.
- Actual Result: Cart updated with new quantity and total price.
- Status: Pass

Test Id: CV-005
Test Scenario: Cart Persistence After Logout/Login
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: "iPhone"
- Steps:
  1. Add a product to the cart.
  2. Log out and log back in.
  3. Go to the cart page.
- Expected Result: Cart retains the previously added items.
- Actual Result: Cart retained previously added items after re-login.
- Status: Pass

Test Id: CV-006
Test Scenario: Cart Cleared After Order Placement
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: "iPhone"
- Steps:
  1. Add a product to the cart.
  2. Complete the checkout process.
  3. Go to the cart page.
- Expected Result: Cart is empty after successful order placement.
- Actual Result: Cart is empty after order placed.
- Status: Pass

---

Module Name: Checkout

Test Id: CO-001
Test Scenario: Valid Checkout
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: Valid address and payment details.
- Steps:
  1. Go to the cart page.
  2. Click 'Proceed to Checkout'.
  3. Enter valid address and payment information.
  4. Place the order.
- Expected Result: Order confirmation page is displayed.
- Actual Result: Order confirmation page displayed after successful checkout.
- Status: Pass

Test Id: CO-002
Test Scenario: Invalid Payment
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: Invalid card details.
- Steps:
  1. Go to the checkout page.
  2. Enter invalid payment information.
- Expected Result: Error message is displayed for payment failure.
- Actual Result: Error message "Payment failed" displayed.
- Status: Pass

Test Id: CO-003
Test Scenario: Checkout with Missing Address
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: No address entered.
- Steps:
  1. Go to the checkout page.
  2. Leave address fields blank.
  3. Attempt to place the order.
- Expected Result: Error message prompts user to enter address.
- Actual Result: Error message "Please enter your address" displayed.
- Status: Pass

Test Id: CO-004
Test Scenario: Apply Invalid Coupon Code
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: Invalid coupon code.
- Steps:
  1. Go to the checkout page.
  2. Enter an invalid coupon code.
- Expected Result: Error message is displayed for invalid coupon.
- Actual Result: Error message "Invalid coupon code" displayed.
- Status: Pass

Test Id: CO-005
Test Scenario: Place Order with Multiple Shipping Addresses
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: Multiple shipping addresses.
- Steps:
  1. Add multiple items to the cart.
  2. Select different shipping addresses for each item.
  3. Place the order.
- Expected Result: Order is placed successfully with items shipped to respective addresses.
- Actual Result: Order placed, items shipped to selected addresses.
- Status: Pass

Test Id: CO-006
Test Scenario: Cancel Order After Checkout
- Pre-requisites: User has placed an order.
- Test Data: Recent order.
- Steps:
  1. Go to 'Your Orders'.
  2. Select the recent order.
  3. Click 'Cancel Order'.
- Expected Result: Order is cancelled and user receives confirmation.
- Actual Result: Order cancelled, confirmation received.
- Status: Pass

Test Id: CO-007
Test Scenario: Checkout with Expired Card
- Pre-requisites: User is logged in and has items in the cart.
- Test Data: Expired credit/debit card details.
- Steps:
  1. Go to the checkout page.
  2. Enter expired card details.
  3. Attempt to place the order.
- Expected Result: Error message is displayed for expired card.
- Actual Result: Error message "Card expired" displayed.
- Status: Pass

Test Id: CO-008
Test Scenario: Checkout as Guest (if supported)
- Pre-requisites: User is not logged in.
- Test Data: Valid address and payment details.
- Steps:
  1. Add product to cart.
  2. Proceed to checkout as guest.
  3. Enter address and payment details.
  4. Place the order.
- Expected Result: Order is placed successfully and confirmation is shown.
- Actual Result: Order placed successfully as guest, confirmation displayed.
- Status: Pass

Test Id: CO-009
Test Scenario: Attempt Checkout with Empty Cart
- Pre-requisites: User is logged in.
- Test Data: None.
- Steps:
  1. Go to the cart page with no items.
  2. Click 'Proceed to Checkout'.
- Expected Result: User is prevented from checking out and shown a message that the cart is empty.
- Actual Result: Checkout prevented, "Your cart is empty" message displayed.
- Status: Pass





