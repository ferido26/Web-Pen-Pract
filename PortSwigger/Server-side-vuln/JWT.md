# JWT (JSON WEB TOKENS)

- Most commonly used in authentication, Session management, Access Control mechanism.
- JWT attacks are basically a user sending modified JWT tokens to the server for malicious purpose, the goal is to bypass the authentication mechanism and access control.

### Structure 
- Header
- Payload
- Signature

### The payload cannot be trusted because it's just Base64 encoded and not encrypted, meaning it can be easily decoded and modified by an attacker. It cannot  be trusted on his own because it's integrity depends entirely on signature

#### MY ATTACK PATH 
- I would start by decoding the JWT to understand its structure, including the algorithm and payload contents. Then I would attempt payload manipulation to check if the server properly verifies the signature. If that fails, I would test for the alg=none vulnerability by removing the signature. I would also check whether signature verification is enforced by modifying the token without updating the signature. If the token uses a symmetric algorithm like HS256, I would consider the possibility of a weak secret. Additionally, I would attempt privilege escalation by modifying fields such as role or user_id and test access to restricted resources. Finally, I would assess token reuse and expiration to evaluate session security.
