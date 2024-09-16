# Creating a new block
- miners: participants known as miners compete to create the next block
- 
with a hash function you cannot find a preimage without brute force

Nonce 11 must be selected such that Hash 11 is less
Hash(Trans 11 + Nonce 11 + Hash 10) < L

# Cryptographic Puzzle

work requirement - to find a valid hash under a threshold ensures miners have done significant work
sha-256 puzzle: given a block
looking for a hash value where the initial 12 bits are 0, like 0000

# Valid vs Non-Valid nonces

two block hashes with the same content but different nonce values, a nonce that produces a hash with 20 leading binary 0s, (5 in hexa) is valid
requiring 20 leading 0s is the same as requiring that the hash number be less than 2 ** 256

## Adjusting the difficulty

- target time to find a valid hash approx every 10 minutes
- if blocks are mined too quickly the max allowed hash value is decreased, making the puzzle harder

## Determining the difficulty
- no central authority dictates this, the majority rules
  - each participant follows the standard algorithm to compute the required number of leading zeros for a valid hash
  - if someone deviates, their blocks are rejected