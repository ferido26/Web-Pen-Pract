# JWT (JSON WEB TOKENS)

- Most commonly used in authentication, Session management, Access Control mechanism.
- JWT attacks are basically a user sending modified JWT tokens to the server for malicious purpose, the goal is to bypass the authentication mechanism and access control.

### Structure 
- Header
- Payload
- Signature

### The payload cannot be trusted because it's just Base64 encoded and not encrypted, meaning it can be easily decoded and modified by an attacker. It cannot  be trusted on his own because it's integrity depends entirely on signature
