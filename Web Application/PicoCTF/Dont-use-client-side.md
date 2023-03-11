
# Dont-use-client-side

#### Description


Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/29835/`
### Hints: 

>  
----------------------------------------------------------------------

## **APPROACH**	
1. Try some credentials but of course `Incorrect password` 
2. Open DevTool, because it's **Client-side problem**. Notice JS code of this website, we got a `verify` function
[![https://imgur.com/cmFVzS3.png](https://imgur.com/cmFVzS3.png)](https://imgur.com/cmFVzS3.png)
3. The flag is splitted into 8 parts, just concatenate it:
`picoCTF{no_clients_plz_7723ce}
