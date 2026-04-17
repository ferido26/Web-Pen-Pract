# Server-side request forgery(SSRF)

### TWO TYPES
- BASIC: You can see the response the server made.
- BLIND: the server doesn't echo the response.

### TWO TYPES OF REQUEST 
- EXTERNAL: A request made to resources on the public internet.
- INTERNAL: A request made to resources inside the server's own network.
  
### OWN WORDS 
- It basically relates to puppet master, because we can be the puppet master and control the server inside it's own network.

- It mainly works on the application layer, because this vulnerability is caused by the application code written by the developer.


### BLACK-LIST BASED INPUT FILTER
- It works by maintaining a pre-defined list of know malicious or forbiddden patterns, such as **block input containing hostnames like 127.0.0.1 or localhost**
- We can often bypass this by URL encoding, obuscation, case variations.
 
### WHITE-LIST BASED INPUT FILTER
- It has a strict set of allowed characters or formats and rejects everything that doesn't match.
- BYPASS TECHNIQUES
   - **https://expected-host:fakepassword@evil-host** (In this the filter sees the expected-host but the browser goes to the evil-host)
   - **https://evil-host#expected-host** (In this we'll use the # character to indicate the URL fragment)
   - We can also use the sub-domain trick like http://expected-host.evil-host and we can also use the URL encoding trick.

### BYPASSING USING THE OPEN REDIRECTION
- In this the app blindly redirects to whatever parameter is given.
- /product/nextProduct?currentProductId=6&path=http://evil-user.net in this the redirect is returned to the **http://evil-user.net**
- 

