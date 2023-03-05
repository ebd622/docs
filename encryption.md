# Symmetric and Asymmetric Encryption
* `Symmetric encryption` uses a unique key that must be shared between parties (people or software) who need to receive messages. Common Symmetric encryption algorithms:
  * AES - one of the most frequently used algorithms. It is fast, ideal when handling large amounts of encrypted data.
  * TwoFish (previously BlowFish) - gives flexibility in performance, total control of the encryption speed.
  * 3DEC - despite its slower speeds and generally outdated status when compared to AES, it is still widely utilized in financial services to encrypt ATM PINs and UNIX passwords.

* `Asymmetric encryption` uses a pair of public keys and a private key to encrypt and decrypt messages when they are communicated. Common algorithms:
  * RSA (Rivest–Shamir–Adleman) - mostly used in digital signatures, email encryption, SSL/TLS certificates and browsers. Low speed, it is NOT convinient for processing large amount of data.
  * ECC (Elliptic Curve Cryptography) -
