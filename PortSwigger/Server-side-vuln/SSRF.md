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

## WHITE-LIST BASED INPUT FILTER

