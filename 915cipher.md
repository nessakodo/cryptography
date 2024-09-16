# Symmetric Encryption

- hashing provides integrity but no confidentiality
  - a suit of encryption and decryption algorithm is called a cipher

*in symmetric encryption, the same key is used for both)*
- caesar cipher is an example of this (but a weak one)

## Advanced Encryption Standard
AES - currently the most well-used and secure symmetric cipher

### AES-128 vs AES-256
- 256 is more secure, but of course slower


#### How to generate a random 128 bit key
```python
import os
key = os.userrandom(16)
```

## What if our input plaintext is larger than 128 bits
- AES Mode of Operation determines how AES encrypts larger texts
- The simplest, yet not ideal mode of operation is ECB: Electronic Code Block

