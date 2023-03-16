
#  Reflected XSS into HTML context with nothing encoded
#### Description



This lab contains a simple  [reflected cross-site scripting](https://portswigger.net/web-security/cross-site-scripting/reflected)  vulnerability in the search functionality.

To solve the lab, perform a cross-site scripting attack that calls the  `alert`  function

>  
----------------------------------------------------------------------

## **APPROACH**

Open this lab and well, we will see a simple blog
\[![https://imgur.com/np58SVs.png](https://imgur.com/np58SVs.png)](https://imgur.com/np58SVs.png)<br>
\
In the description, we know this web contains a vulnerability in the search function, it's the fisrt lab of XSS and it named `nothing encoded`, so I think it's very simple. Let put simple payload into search bar: `<script>alert("Welcome to my GitHub);</script>`
<br>
[![https://imgur.com/NThLkNk.png](https://imgur.com/NThLkNk.png)](https://imgur.com/NThLkNk.png)
\
\
Yes, this script is triggered, **Ctrl + U** to check the source code:
\
\
 <br>[![https://imgur.com/GYVrbjO.png](https://imgur.com/GYVrbjO.png)](https://imgur.com/GYVrbjO.png)<br>
Done 💗
