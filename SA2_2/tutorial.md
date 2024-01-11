Perform IDOR using Parameters
======================
In this activity, you will perform an IDOR attack by modifying the request parameters, properties and code for the toy website using Burp Suite.

<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10980281/C126_2_2.4.gif" width = "100%" height = "50%">


Follow the given steps to complete this activity.


1. Download and Install [Burp Suite](https://portswigger.net/burp/releases/professional-community-2023-10-3-7?requestededition=community&requestedplatform=) to test the attack on the website. 
2. Open Burp Suite and Open `Proxy` tab, turn off the Intercept and click on `Open Browser`.
3. Open [Toy Store](https://tnk-m16-toywebsite.onrender.com/) website in the Burp Suite browser.
4. Select a product from home screen of the website.
5. Now turn on the intercept so that burp suit holds the request to be seen and edited by us before sending it to the website's server.
6. Click on `Add To Cart` and check the burp suit for the intercepted request.
7. Change the price parameters in the request and click on `Forward` button to send the updated request to the server.

Check if the product is added to the cart with updated price in the website.
