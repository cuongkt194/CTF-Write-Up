
# Who are you?
#### Description



My dog-sitter's brother made this website but I can't get in; can you help?[login.mars.picoctf.net](https://login.mars.picoctf.net/)
### Hints: 

>  
----------------------------------------------------------------------

## **APPROACH**	
Yes, another login form, client-side again 
Open this index.js and we got thounsands lines of code: 
`(async()=>{await new Promise((e=>window.addEventListener("load",e))),document.querySelector("form").addEventListener("submit",(e=>{e.preventDefault();const r={u:"input[name=username]",p:"input[name=password]"},t={};for(const e in r)t[e]=btoa(document.querySelector(r[e]).value).replace(/=/g,"");return"YWRtaW4"!==t.u?alert("Incorrect Username"):"cGljb0NURns1M3J2M3JfNTNydjNyXzUzcnYzcl81M3J2M3JfNTNydjNyfQ"!==t.p?alert("Incorrect Password"):void alert(`Correct Password! Your flag is ${atob(t.p)}.`)}))})();`
<br>Huh, it's seem to be hard to read without Javascript format, let chatGPT beautify it for us: `Beautify this code <above code>` and we got [![https://imgur.com/PKk0Iem.png](https://imgur.com/PKk0Iem.png)](https://imgur.com/PKk0Iem.png)
<br>Notice at `else  if (values.p !== "cGljb0NURns1M3J2M3JfNTNydjNyXzUzcnYzcl81M3J2M3JfNTNydjNyfQ")`, it looks like base64 encode, try decoding it
[![https://imgur.com/tZ61OVy.png](https://imgur.com/tZ61OVy.png)](https://imgur.com/tZ61OVy.png)
Yeah, this is the flag
