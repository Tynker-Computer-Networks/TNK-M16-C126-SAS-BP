Prevent the IDOR
======================
In this activity, you will modify the Toy Store website to take important info from server side and not rely on clients input for sensitive data such as name, price and quantity of product.

<img src= "https://s3-whjr-curriculum-uploads.whjr.online/73c5b457-c974-4415-a10b-e7569aefec53.gif" width = "auto" height = "auto">

Follow the given steps to complete this activity.

1. Open `controller.py` file. 
2. Use data from server side for the selected product.
   * Check which product is selected from list of products in `addTocart()` function.
    ```
    for product in products:
        if product['id'] == int(data['product_id']):
            selectedProduct = product
    ```
    * Use selectedProduct to set values such as name, price, image, total in the `data`
    ```
    data['price'] = selectedProduct['selling_price']
    data['total'] = selectedProduct['selling_price'] * data['quantity']
    data['name'] = selectedProduct['name']
    data['image'] = 'static/images/' + selectedProduct['image']
    ```
   
Save and run the code to check the if the product is fixed.
