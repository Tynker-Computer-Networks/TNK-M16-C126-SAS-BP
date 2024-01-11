Perform IDOR Attack using URL
======================
In this activity, you will perform an IDOR attack on the toy store website to access restricted data.


<img src= "https://s3-whjr-curriculum-uploads.whjr.online/0b1cf727-d2a4-4483-a29f-7b3d85b783b4.gif" width = "100%" height = "50%">




Follow the given steps to complete this activity.


1. Perform the IDOR attack
   * Run `app.py` to run the `Toy Store` website on localhost.
   * Open the hosted link and login to the website using your E-mail id and use password `123`.
   * Click on any product to view the product details.
   * Check the URL which has the product id as `id`.
   * Try changing the product id to 7, 8 etc. to access some products that are not available on the homepage of the website otherwise(not on sale).
   * Open the `controller.py` file from the `controller` folder.
   * Modify code for the `order()` function.
   * We have products in the format:
    ```
    {'id': 1,
    'name': 'Robo Dog',
    'image': 'toy1.png',
    'rating': 4,
    'selling_price': 900,
    'marked_price': 1000,
    'status': 'For Sale'
    }
    ```
    * Redirect the customer to the homepage if the product is `Not For Sale`.  
    ```
        if selectedProduct['status'] == 'Not For Sale':
            return redirect('/')  
    ```
   
   * Save and run the code to check if the product web page with prices is fixed.


