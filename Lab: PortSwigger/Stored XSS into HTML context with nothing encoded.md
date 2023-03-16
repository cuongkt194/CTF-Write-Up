
# Stored XSS into HTML context with nothing encoded
#### Description




This lab contains a  [stored cross-site scripting](https://portswigger.net/web-security/cross-site-scripting/stored)  vulnerability in the comment functionality.

To solve this lab, submit a comment that calls the  `alert`  function when the blog post is viewed.

>  
----------------------------------------------------------------------

## **APPROACH**
This lab is a blog again. In the description, we were told that it contains a Stored XSS vulnerability in the comment function. Since it's quite easy, I simply entered the payload and solved it. Here is the payload I used: `<script>alert(1)</script>`
