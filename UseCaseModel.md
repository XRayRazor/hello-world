# EZShop and Grocery Store Kiosk Payment System Use Case Model

**Author**: 

## 1. Use Case Diagram

![Alt text](https://github.com/XRayRazor/hello-world/blob/master/user_diagrammmmmmmmmm.png)

## 2. Use Case Descriptions

### 2.1 Browse items

* **_Requirements: _**This use case generally allows existing customer to start a new grocery shopping and edit the shopping cart through mobile device for checkout.

* **_Pre-conditions:_**
    1. The valid customer card is immediately accessible.
    2. The customer's device successfully installed **EZShop APP**.

* **_Postconditions:_**   
    1. A shopping cart consists of customer's information, products, and discounts has been prepared for checkout.
    2. Or the customer directly exit shopping mode before checkout.

* **_Scenarios:_**  
    1. Normal: The customer starts shopping, edit the shopping list in the cart, and ready to checkout.
    2. Alternate: The customer starts shopping, but stops shopping before going for checkout.
    3. Exceptional:     
    i) The customer fails to provide a valid customer card.     
    ii) The customer doesn't pass any inputs to the APP.

									

### 2.2 Scan customer card and launch shopping

* **_Requirements: _**This use case allows customer to use the camera on the mobile device to aim the QR code on the customer card, scan it, and initiate the shopping.

* **_Pre-conditions:_**
    1. Mobile device and its camera are functional.
    2. Customer card is valid.
    3. Wireless internet, celluar or Wi-Fi, is available.
    4. The "QR" on mobile devices works well.

* **_Postconditions:_** The shopping procedure is launched. The customer can then add/remove products and add coupons using this APP.

* **_Scenarios:_**  
    1. Normal: The customer scans the card correctly and the shopping begin.
    2. Alternate: The customer doesn't scan the card correctly, ask for re-scan.
    3. Exceptional:     
    i) The customer doesn't pass any inputs (scan/button pressing) to the APP for over 1 minute, dim and then shut the screen.     
    ii) The customer fails to provide a valid customer card.


### 2.3 QR code operations (generation, scanning, interpretation)

* **_Requirements: _**This use case enables all devices which installed EZShop and the grocery store payment system to generate, scan, and interpret QR codes with encoded information.

* **_Pre-conditions:_**
    1. Valid QR codes.
    2. Enough information to be encoded into QR codes.
    3. Wireless/wire web is available.

* **_Postconditions:_** 
    1. The information encoded in the QR code is decoded.
    2. Or the information is encoded into the QR code.

* **_Scenarios:_**  
    1. Normal:      
    i) The customer/cashier successfully collects encoded information from QR codes through EZShop     
    ii) Or the customer successfully encodes shopping cart information into QR code.
    2. Alternate:     
    i) The customer/cashier doesn't scan the QR code correctly, ask for re-scan.     
    ii) The customer's shopping cart is empty. No QR code is generated.
    3. Exceptional:     
    i) The customer/cashier doesn't pass any inputs (scan/button pressing) to the APP for over 1 minute, dim and then shut the screen.     
    ii) The customer/cashier directly exits.


### 2.4 Edit shopping cart

* **_Requirements: _**This use case allows customers to add/remove products, add coupons by themselves through their mobile devices while shopping.

* **_Pre-conditions:_**
    1. QR code utility is functional.
    2. Customer has already initiated new shopping through EZShop APP.
    3. The virtual/physical buttons on mobile devices and kiosks work well.

* **_Postconditions:_** Get the list of currently kept products and coupons. The list is ready for checkout.

* **_Scenarios:_**  
    1. Normal: The customer get a list of currently wanted products and/or coupons and corresponding unit price and discount.
    2. Alternate: The customer doesn't want anything or doesn't checkout. The customer directly exit shopping.
    3. Exceptional: The customer doesn't pass any inputs (scan/button pressing) to the APP for over 1 minute, dim and then shut the screen.


### 2.5 EZShop/Kiosk payment system virtual and physical button inputs processing

* **_Requirements: _**This use case enables mobile devices and kiosk to process the button-pressing inputs.

* **_Pre-conditions:_**
    1. Physical buttons on mobile devices/kiosk are functional.
    2. Customer has already initiated new shopping through EZShop APP.
    3. The payment system on kiosk has been launched.

* **_Postconditions:_**
    1. Get the corresponding inputs ("QR/+/-/Pay/<-", definitions see below) for EZShop APP.    
    2. Get the corresponding inputs for grocery store kiosk payment system.
    
|||  |Button  | Physical or Virtual | Function
-------------:|-------------:|-------------:|-------------:|:-------------:|:-------------:|:-------------:
|||  |QR  | Virtual | Launch the QR code scanner
|||  |+  | Virtual   | Add item
|||  |-  | Virtual   | Remove item
|||  |<-  | Physical | Go back
|||  |Check  | Virtual | Pass honest check and go to payment
|||  |Credit  | Virtual | Pay by credit card
|||  |Debit  | Virtual | Pay by debit card
|||  |Gift  | Virtual | Pay by gift card
|||  |Cash  | Virtual | Pay by credit card
|||  |Print Receipt  | Virtual | Print receipt

* **_Scenarios:_**  
    1. Normal:      
    i) The customer presses specific button and the APP correctly goes into corresponding stage.     
    ii) The cashier presses specific button and the kiosk payment system correctly goes into corresponding stage.     
    2. Alternate: None.
    3. Exceptional: None.



### 2.6 Add items

* **_Requirements: _**This use case allows customers to add products through their mobile devices while shopping.

* **_Pre-conditions:_**
    1. QR code utility is functional.
    2. Customer has already initiated new shopping through EZShop APP.
    3. The "+" on mobile devices works well.

* **_Postconditions:_** The information of scanned product and corresponding price are added into customer's cart.

* **_Scenarios:_**  
    1. Normal: The customer added a product and corresponding price into the shopping cart.
    2. Alternate:       
    i) The customer turn on the "add" mode and then decide not to scan the item. The customer press back arrow "<-" to cancel the "add" mode.      
    ii) The customer adds the alcoholic beverage. EZShop prompt customer after adding.      
    iii) The customer turned on the "add" mode and accidently scanned the coupon QR code. EZShop prompts customer and go back to shopping mode.
    3. Exceptional: The customer doesn't pass any inputs (scan/button pressing) to the APP for over 1 minute, go back to the shopping cart.



### 2.7 Remove items

* **_Requirements: _**This use case allows customers to reomove added products through their mobile devices while shopping.

* **_Pre-conditions:_**
    1. QR code utility is functional.
    2. Customer has already initiated new shopping through EZShop APP.
    3. The "-" on mobile devices works well.
    4. There is already same type of product existing in the shopping cart before "remove" mode.

* **_Postconditions:_** The information of scanned product and corresponding price are removed from customer's cart.

* **_Scenarios:_**  
    1. Normal: The customer removed a product and corresponding price from the shopping cart.
    2. Alternate:        
    i) The customer turn on the "remove" mode and then decide not to scan the item. The customer press back arrow "<-" to cancel the "remove" mode.       
    ii) The customer turned on the "remove" mode but accidently scanned a coupon. EZShop prompts customer and go back to shopping mode.
    3. Exceptional:       
    i) The customer doesn't pass any inputs (scan/button pressing) to the APP for over 1 minute, go back to the shopping cart.      
    ii) There is no such type of product in the shopping cart. Prompt customer and go back to shopping cart without removing.




### 2.8 Add coupons

* **_Requirements: _**This use case allows customers to add coupons through their mobile devices while shopping no matter there is any such product or not in the shopping cart.

* **_Pre-conditions:_**
    1. QR code utility is functional.
    2. Customer has already initiated new shopping through EZShop APP.
    3. The "QR" on mobile devices works well.
* **_Postconditions:_** The information of scanned product and corresponding discount are added into customer's cart.

* **_Scenarios:_**  
    1. Normal: The customer added the discount corresponds to specific product into the shopping cart.
    2. Alternate: The customer turn on the QR scanning mode and then decide not to scan the item. The customer press back arrow "<-" to cancel the scanning mode.
    3. Exceptional: The customer doesn't pass any inputs (scan/button pressing) to the APP for over 1 minute, go back to the shopping cart.

### 2.9 Directly exit

* **_Requirements: _**This use case allows customers to exit shopping mode before checkout.

* **_Pre-conditions:_**
    1. Customer has already initiated new shopping through EZShop APP.
    2. The "<-" on mobile devices works well.
* **_Postconditions:_** Customer ends the shopping. 

* **_Scenarios:_**  
    1. Normal: Customer presses "<-" to terminate the shopping. EZShop prompt customer whether to end the shopping. The existing shopping cart got deleted with customer's consent.
    2. Alternate: Customer doesn't agree to exit. Stay in the shopping mode.
    3. Exceptional: None.


### 2.10 Checkout

* **_Requirements: _**This use case allows customers to checkout all the product and coupons within the current shopping cart and generate a corresponding QR code for kiosk payment system.

* **_Pre-conditions:_**
    1. Customer has already initiated new shopping through EZShop APP.
    2. The "Pay" on mobile devices works well.
    3. There is at least one product within the current shopping cart.
* **_Postconditions:_** EZShop generates a valid QR code for grocery store kiosk payment system. 

* **_Scenarios:_**  
    1. Normal: Customer presses "<-" to terminate the shopping. EZShop prompt customer whether to end the shopping. The existing shopping cart got deleted with customer's consent.
    2. Alternate: Customer doesn't agree to exit. Stay in the shopping mode.
    3. Exceptional: None.


### 2.11 Calculate total value

* **_Requirements: _**This use case calculates the total value of the cart considering total price, taxes (AB product and non-AB product), and discount.

* **_Pre-conditions:_**
    1. Customer has already initiated new shopping through EZShop APP.
    2. The "Pay" on mobile devices works well.
    3. There is at least one product within the current shopping cart.
* **_Postconditions:_** EZShop corresctly calculates the total value of the cart including the total price, necessary taxes (both AB product and non-AB product), and discounts. 

* **_Scenarios:_**  
    1. Normal: Customer decides to checkout and presses "Pay". EZShop prompt customer whether to checkout. The total value of the cart is calculated with customer's consent.
    2. Alternate: Customer doesn't agree to checkout. Stay in the shopping mode.
    3. Exceptional: If there is no concrete product in the cart, EZShop will prompt customer and go back to shopping mode. In other words, pressing "Pay" while the cart only contains coupons or nothing will not calculate the total value and generate QR code for following kiosk payment system.


### 2.12 Generate QR code

* **_Requirements: _**This use case encodes the customer's information, the items and coupons lists, and the total value of the cart into a QR code for following payment system.

* **_Pre-conditions:_**
    1. The total value of the cart has been calculated.
    2. QR code utility is functional.

* **_Postconditions:_** A valid QR code for grocery store kiosk payment system is generated. 

* **_Scenarios:_**  
    1. Normal: An QR code which encodes the customer's information, the items and coupons lists, and the total value of the cart is generated.
    2. Alternate: Non.
    3. Exceptional: Non.

### 2.13 Scan QR code of customer's cart

* **_Requirements: _**This use case enable cashier of the grocery store to collect the shopping information of the customer.

* **_Pre-conditions:_**
    1. Customer provides a valid QR code.
    2. QR code utility is functional.

* **_Postconditions:_** The customer's information, items and coupons list, and the total value of the shopping cart have been collected by the payment system. 

* **_Scenarios:_**  
    1. Normal: An QR code which encodes the customer's information, the items and coupons lists, and the total value of the cart is scanned and all information is collected.
    2. Alternate: Ask to scan again if cashier doesn't scan the QR code correctly.
    3. Exceptional: Customer fails to provide a valid QR code.


### 2.14 Honest checking

* **_Requirements: _**This use case can tell payment system that the cashier has verified the items in the customer's physical shopping cart are consistent to the virtual shopping cart. It also tell system that the cashier has checked the customer's ID when there is alcoholic beverage.

* **_Pre-conditions:_** Customer's QR code is scanned by cashier.
    
* **_Postconditions:_** The cashier makes sure the list of products of the virtual cart is consistent to the items physically in the cart. And cashier verifies the customer is above the legal drinking age if there is alcoholic beverage.

* **_Scenarios:_**  
    1. Normal: The items in the physical cart (also the age of customer if necessary) are checked. It is ready for following payment.
    2. Alternate: None
    3. Exceptional:          
    i) There is item inconsistency. Checkout is terminated. Customer goes back to shopping mode.       
    ii) The customer is below legal drinking age.

### 2.15 Payment

* **_Requirements: _**This use case enables grocery store kiosk payment system to conclude the transaction with customer safely and efficiently.

* **_Pre-conditions:_** Customer passes the honest checking conducted by cashier.
    
* **_Postconditions:_** The payment is collected from the customer.

* **_Scenarios:_**  
    1. Normal: The cashier collect a payment method, including credit card, debit card, gift card, and cash, from customer. Cusomter provide corresponding payment to cashier and kiosk payment system. The transaction is concluded.
    2. Alternate: None
    3. Exceptional: The customer fails to provide a valid payment. 




































































