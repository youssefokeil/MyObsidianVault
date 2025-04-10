Created on: 14-08-2024 10:57
Status: #idea
Tags: #security
# Hashing
> the process of transforms any given string of characters  into another value

### Used in:
- Securing the user's passwords. Instead of storing passwords in plain text, they're stored as hash values. It's always difficult to reverse engineer a hashing algorithm
### Algorithms:
**Using flask's bcrypt:**
```
from flask_crypyt import Bcrypt
bcrypt=Bcrypt()
hashed=bcrypt.generaate_password_hash('password')
```
the hashed variable contains what is returned after hashing the string of characters "password"




-----------------
# References