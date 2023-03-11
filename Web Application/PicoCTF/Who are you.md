
# Who are you?
#### Description



Let me in. Let me iiiiiiinnnnnnnnnnnnnnnnnnnn [http://mercury.picoctf.net:34588/](http://mercury.picoctf.net:34588/)
### Hints: 

>  
----------------------------------------------------------------------

## **APPROACH**	
Open this challenge, we got:
[![https://imgur.com/9cnrfxJ.png](https://imgur.com/9cnrfxJ.png)](https://imgur.com/9cnrfxJ.png)<br>
1. We need "change" our browser to `PicoBrowser` to access this site, so open Burp and **Send this request** to `Repeater`. Because there is no browser named `PicoBrowser`, so we must trick the server we are using `PicoBrowser` by edit the User-Agent header to `PicoBrowser`
![https://i.imgur.com/8On9eqs.png](https://i.imgur.com/8On9eqs.png)

2. After send the modified request, we got `I dont trust users visiting from another site.`.  So add this to the request for trick the website that we go here via Pico `Referer: http://mercury.picoctf.net:34588`
3. We got `Sorry, this site only worked in 2018`, huh, search Google for `date time header http` and we got `
Date: <day-name>, <day> <month> <year> <hour>:<minute>:<second> GMT`, edit this to any day in 2018 and send the request, for example: `
Date: Wed, 21 Oct 2018 07:28:00 GMT`
4.  Hmm, `I don't trust users who can be tracked`, there's a syntax in HTTP header that let user decide whether they can be tracked, it's called `DNT`. Add this and set value for `1` 
5. `This website is only for people from Sweden.` Yeah, so many step. Maybe this site use `X-Forwarded-For` to check where the user is, search for some Sweden IP in Google and modify `X-Forwarded-For` value.
6. `You're in Sweden but you don't speak Swedish?` It's `Accept-Language` problem, modify it to `SWE` (Swedish in HTTP header) and finally get the flag:[![https://imgur.com/JtKViRK.png](https://imgur.com/JtKViRK.png)](https://imgur.com/JtKViRK.png)
