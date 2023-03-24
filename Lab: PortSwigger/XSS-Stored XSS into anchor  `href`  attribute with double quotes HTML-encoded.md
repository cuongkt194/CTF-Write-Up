# Stored XSS into anchor  `href`  attribute with double quotes HTML-encoded
#### Description

his lab contains a [stored cross-site scripting](https://portswigger.net/web-security/cross-site-scripting/stored) vulnerability in the comment functionality. To solve this lab, submit a comment that calls the `alert` function when the comment author name is clicked.
>  
----------------------------------------------------------------------

## **APPROACH**
Stored XSS, we try put the previous payload to it but it has encoded `<,> and "`, so our payload did nothing. Observe that in HTML `a` tag, there is way to link Javascript:
\
\
[[![https://imgur.com/ItSsmlg.png](https://imgur.com/ItSsmlg.png)](https://imgur.com/ItSsmlg.png)
\
\
Try this and solve the lab: `javascript:alert(1) 
