
# # Reflected XSS into attribute with angle brackets HTML-encoded
#### Description

This lab contains a [reflected cross-site scripting](https://portswigger.net/web-security/cross-site-scripting/reflected) vulnerability in the search blog functionality where angle brackets are HTML-encoded. To solve this lab, perform a cross-site scripting attack that injects an attribute and calls the `alert` function.

>  
----------------------------------------------------------------------

## **APPROACH**
We come to a reflected XSS again, but now it encode angle brackets character. The query is added to value attribute: `value=` 
\
\
[![https://imgur.com/2WhAC8j.png](https://imgur.com/2WhAC8j.png)](https://imgur.com/2WhAC8j.png)
\
\
 Now, we try trigger XSS by a payload that doesn't contain `<` or `>`. Since the payload will be added to value of input, we can try `onmousemove="alert(1)"` event. 
\
\
[![https://imgur.com/zh2eqcE.png](https://imgur.com/zh2eqcE.png)](https://imgur.com/zh2eqcE.png)
UwU, I forgot close value of value :smile: so the correct payload is `"onmousemove="alert(1)"`. Explain this payload: when mouse moves, it trigger js to call alert function.<br>
\
[![https://imgur.com/Zc4i7QZ.png](https://imgur.com/Zc4i7QZ.png)](https://imgur.com/Zc4i7QZ.png)
