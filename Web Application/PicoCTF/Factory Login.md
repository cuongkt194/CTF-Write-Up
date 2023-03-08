
# logon

#### Description


The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796`
### Hints: 

>  
----------------------------------------------------------------------

## **APPROACH**	
Try login with Joe and a random password, I got:
> I'm sorry Joe's password is super secure. You're not getting in that way.

Hmm, so I think it's a hint, we don't need bypass the login form. But I tried with a basic SQL Injection **Joe'--**, yes it logged in, but:
>Success: You logged in! Not sure you'll be able to see the flag though.
> No flag for you

I tried with different username and all got this page and of course there is no flag.
An idea came to my head, open Dev tool and check this cookie
[![https://imgur.com/jXWsiO1.png](https://imgur.com/jXWsiO1.png)](https://imgur.com/jXWsiO1.png)
Observe that **admin** is having a value **False**, so I try edit this value to **True** and get the flag:
> **Flag**:  `picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}`
