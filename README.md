jsonp-flickrAPI
===============
  - We are using a different domain so i can not use XmlHttpRequest.		
  - JSON does not work in a client side environment without callbacks. This is due to the fact that JSON objects come back anonymous and when you include them in your page via script tags, they do not initialize to anything.They must be passed to eval or to a function in order to become a Javascript object.*/

   But if i had to make this feed work i would do:
  - (1) Modify the given link deleting the curly brackets from  -jsoncallback={callback}- so as to create a callback function.
  - (2) Include the modified link via script tag into the head of the html document. 
  - (3) Add a function callback(data) to access the given data.
