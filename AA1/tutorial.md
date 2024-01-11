Perform IDOR using Parameters on Place Order Page
======================
In this activity, you will perform an IDOR attack by modifying the request parameters, properties, and code for the toy website using Burp Suite.


<img src= "https://s3-whjr-curriculum-uploads.whjr.online/266425b7-451d-4b29-b36e-4ada2875dd87.gif" width = "100%" height = "50%">


Follow the given steps to complete this activity.
1. Perform the IDOR
   * Download and Install [Burp Suite](https://portswigger.net/burp/releases/professional-community-2023-10-3-7?requestededition=community&requestedplatform=) to test the attack on the website.
   * Open Burp Suite and Open `Proxy` tab, turn off the Intercept and click on `Open Browser`.
   * Open [Toy Store](https://tnk-m16-toywebsite.onrender.com/) website in the Burp Suite browser.
   * Add products in the cart.
   * Now turn on the intercept so that burp suit holds the request to be seen and edited by us before sending it to the website's server.
   * Click on `Place Order` and check the burp suit for the intercepted request.
   * Change the price parameters in the request and click on `Forward` button to send the updated request to the server.


   * Check if the order is placed with the updated price on the website.
   
   * Save and run the code to check if the product web page with prices is fixed.
