***Welcome to my first write-up 😁 I've solved some CTF challenges before but didn't write up solutions, but now I think that if I wanna go far, I must to write out what I think in my head and maybe these write-up will help me in my career 🤔 Just goooo!***
# GET aHEAD.

#### Description
Find the flag being held on this server to get ahead of the competition  [http://mercury.picoctf.net:28916/](http://mercury.picoctf.net:28916/)

#### Hints: 

> Maybe you have more than 2 choices 
> Check out tools like Burpsuite to modify your requests and look at the responses

## **STEP**	

 **1**. Open Burp Suite and turn Intercept on<br>
 **2**. Go to [http://mercury.picoctf.net:28916/]<br>
 **3**. Based on the name of the challenge, edit the HTTP method from **GET** to **HEAD**<br>
<img src="/Web Application/PicoCTF/img/aHEAD.png"><br>
 **4**. Forward this request, open browser and go to Network tab then check the **Response Headers** and get the flag
<img src="/Web Application/PicoCTF/img/flagaHEAD.png">

