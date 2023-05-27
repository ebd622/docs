# Keystore VS Truststore
TODO

A keystore is a repository that contains private keys and their corresponding digital certificates. These keys are used to authenticate the identity of a server to a client during an SSL/TLS handshake, and to establish a secure connection between them. A keystore can also contain public keys of other parties, which are used to encrypt data sent to them.

A truststore, on the other hand, is a repository that contains trusted digital certificates used to verify the identity of remote parties. When a client connects to a server, it needs to verify that the server's digital certificate is issued by a trusted authority and that it has not been tampered with. The truststore contains the public keys of the trusted authorities that are used to verify the server's digital certificate.

In summary, the main difference between a keystore and a truststore is that a keystore is used to store private keys and their corresponding digital certificates, while a truststore is used to store trusted public keys of other parties. The keystore is used by the server to prove its identity to the client, while the truststore is used by the client to verify the identity of the server.

# References
* https://www.youtube.com/watch?v=Ur9LlNOYnRg
