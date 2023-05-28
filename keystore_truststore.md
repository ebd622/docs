# Keystore VS Truststore

Keystore and Truststore are very similar in terms of structure. The only difference is what they store, what is purpose and to use them.

## Definistion
A keystore is a repository that contains private keys and their corresponding digital certificates. A keystore can also contain public keys of other parties, which are used to encrypt data sent to them.

A truststore is a repository that contains trusted digital certificates used to verify the identity of remote parties. When a client connects to a server, it needs to verify that the server's digital certificate is issued by a trusted authority and that it has not been tampered with. The truststore contains the public keys of the trusted authorities that are used to verify the server's digital certificate.

In summary, the main difference between a keystore and a truststore is that a keystore is used to store private keys and their corresponding digital certificates, while a truststore is used to store trusted public keys of other parties. The keystore is used by the server to prove its identity to the client, while the truststore is used by the client to verify the identity of the server.

## Purpose
* Keystore is used by KeyManager, trust store is used by TrustManager;
* Keystore is used to authenticate the identity of a server to a client during an SSL/TLS handshake. After that a secure connection can be established.
TODO

## Content
* Keystore consists of private key which is configured at server side for SSL connection.  Keystore can be also configured on client side if client authentication is required at a server side.
* Truststore consits of public keys and certificates. It is configured on the side where autjentication of other party is required.


# References
* https://www.youtube.com/watch?v=Ur9LlNOYnRg
