Prevent the IDOR
======================
In this activity, you will modify the Toy Store website to take important info from server side and not rely on clients input for sensitive data such as name, price, and quantity of product while placing orders.


<img src= "https://s3-whjr-curriculum-uploads.whjr.online/efed72ae-00ea-4a10-80bc-97040fe5784c.gif" width = "100%" height = "50%">


Follow the given steps to complete this activity.
1. Prevent the IDOR
   * Open `controller.py` file.
   * Use data from the server side for the order in the `placeOrder()` function.
   * Cart is stored in the session of the server so use the cart stored in the session while placing order instead of taking the whole cart from the user request.
    ```
    cart = session.get('cart', [])
    ```
    * make the cart in the session empty as now the order is placed.
    ```
    session['cart'] = []
    ```
   
   * Save and run the code to check if the product web page with prices is fixed.
