# Scavenger Hunt

#### Description
There is some interesting information hidden around this site [http://mercury.picoctf.net:55079/](http://mercury.picoctf.net:55079/). Can you find it?
#### Hints: 

> You should have enough hints to find the files, don't run a brute forcer.
----------------------------------------------------------------------
Do the same as previous challenge (insp3ct0r), we'll get 2 parts of the flag and a hint to find next part(s)
> picoCTF{t<br>
> h4ts_4_l0<br>

***How can I keep Google from indexing my website?***
Do you know Google Crawler and how to prevent it crawl your website? Let check the robots.txt we'll get 
> User-agent: * <br>
Disallow: /index.html<br>
 Part 3: t_0f_pl4c<br>
 I think this is an apache server... can you Access the next flag?

Hmm, we get a new hint, Apache server? Check .htaccess
Why is ".htaccess"? Because it is **a configuration file used by apache-based web servers**
Replace robots.txt with **.htaccess**, yeah, we got this 
>Part 4: 3s_2_lO0k<br>
>I love making websites on my Mac, I can Store a lot of information there.

Search Google for "Where does Mac store file", I got **.DS_Store**, it's **a macOS file that is created by Finder in every folder to hold the user's folder view preferences**. Just replace .htaccess with **.DS_Store** and you will get *"Congrats! You completed the scavenger hunt. Part 5: _74cceb07}''*


## Finally, the flag is picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_74cceb07}
That's a lot of places to look 
