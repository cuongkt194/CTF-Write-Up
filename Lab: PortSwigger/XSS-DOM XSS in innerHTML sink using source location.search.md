
# ## DOM XSS in  `innerHTML`  sink using source  `location.search`
#### Description



This lab contains a  [DOM-based cross-site scripting](https://portswigger.net/web-security/cross-site-scripting/dom-based)  vulnerability in the search blog functionality. It uses an  `innerHTML`  assignment, which changes the HTML contents of a  `div`  element, using data from  `location.search`.

To solve this lab, perform a cross-site scripting attack that calls the  `alert`  function.
>  
----------------------------------------------------------------------

## **APPROACH**
Like a habit for search function vuln, I type something and Enter. Open DevTools and observe that data was put into a `span` tag. 
\
\
![img](https://imgur.com/W9NxjOa.png)
\
\
That's quite easy, put `img` tag payload to trigger this XSS bug . Here we go: `<img src=1 onerror="alert(1)">`. Explaining for this payload, I add an image where is incorrect addrest, so this site can't load the image, then `onerror` means if website cannot load image, it will execute and trigger XSS.
\
\
![https://imgur.com/aCUkuHR.png](https://imgur.com/aCUkuHR.png)
