
# ## DOM XSS in  `document.write`  sink using source  `location.search`
#### Description




This lab contains a  [DOM-based cross-site scripting](https://portswigger.net/web-security/cross-site-scripting/dom-based)  vulnerability in the submit feedback page. It uses the jQuery library's  `$`  selector function to find an anchor element, and changes its  `href`  attribute using data from  `location.search`.

To solve this lab, make the "back" link alert  `document.cookie`.

>  
----------------------------------------------------------------------

## **APPROACH**
We come to this blog again, now it contains DOM XSS vuln in feedback function.
Try enter something into these boxes and open DevTool to check whether data is added or not. 
`Ctrl F` to find but nothing appears. 
Read the code and I see the URL is vulnerable. So try edit ReturnPath Parameter.
\
\
![img](https://imgur.com/Ad43uR7.png)
\
\
Since this parameter is vulnerable and the data is added into `href` tag, we can call JavaScript function simply by modify parameter with: `javascript:alert(1)`<br>
\
\
[![https://imgur.com/kVLFvgn.png](https://imgur.com/kVLFvgn.png)](https://imgur.com/kVLFvgn.png)
