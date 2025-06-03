# Cryptography
## Hashing
Hashing is the process of converting any input (like a file, password, or message) into a fixed-size string of characters, which typically looks like a random sequence of letters and numbers. This output is called a hash or digest.
```
echo -n "Hello, world" | shasum -a 256
4ae7c3b6ac0beff671efa8cf57386151c06e58ca53a78d83f36107316cec125f
```
It is one-way: *you cannot reverse a hash to get the original data.*
