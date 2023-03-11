# logon

#### Description


The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796`
### Hints: 

>  
----------------------------------------------------------------------

## **APPROACH**	
**1.**  Attempt to log in as Joe with a random password, but receive an error message indicating that Joe's password is secure.<br>
**2.**  Try a basic SQL injection with the username `Joe'--` and successfully log in, but receive a message indicating that there is no flag available.<br>
**3.**  Try logging in with different usernames, but all result in the same page with no flag available.<br>
**4.**  Check the value of the `admin` cookie using the browser's DevTool, and find that it is set to `False`.[![https://imgur.com/jXWsiO1.png](https://imgur.com/jXWsiO1.png)](https://imgur.com/jXWsiO1.png)<br>
**5.**  Edit the value of the `admin` cookie to `True` .<br>
**6.**  Refresh the page and receive the flag: `picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}`.<br>
