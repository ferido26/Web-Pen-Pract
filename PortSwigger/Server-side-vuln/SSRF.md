Server-side request forgery(SSRF)
- BASIC: You can see the response the server made.
- BLIND: the server doesn't echo the response/
- 
You trick the server into making a request, but you never get to know about the response, so you can create a fake server which you control and give the URL
to the vulnerable application so that it makes a request to your server and you can get the incoming request in your logs!! (Know as the OAST Technique)

## whitelist-based input filters
