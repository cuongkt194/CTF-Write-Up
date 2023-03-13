
# Search Source
#### Description


The developer of this website mistakenly left an important artifact in the website source, can you find it?The website is  [here](http://saturn.picoctf.net:65352/).
### Hints: 

>  
----------------------------------------------------------------------

## **APPROACH**	
The challenge is named "Search Source," which suggests searching for something in the website source code. To accomplish this, we can use Burp Suite.<br>

To start, open Burp Suite and select the Target tab. Then, right-click and select Engagement Tools > Find Comment.

[  
](https://imgur.com/uXVJRzk.png)[![https://imgur.com/uXVJRzk.png](https://imgur.com/uXVJRzk.png)](https://imgur.com/uXVJRzk.png)<br>
We'll get a lot of comments, so we can export them to a text file to search through them more easily. Since we know the flag format is `picoCTF{xxx}`, we can search for this string and find the flag.
[  
](https://imgur.com/G7Iq6oB.png)[![https://imgur.com/G7Iq6oB.png](https://imgur.com/G7Iq6oB.png)](https://imgur.com/G7Iq6oB.png)<br>
The flag for this challenge is: `picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7}`.
 
