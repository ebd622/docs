# Certificate Chain
**PKI** (stands for [Public Key Infrastructure](https://en.wikipedia.org/wiki/Public_key_infrastructure)) it is a system of technologies, processes, and policies that enables the secure exchange of digital information through the use of public key cryptography.

**Certificate chains** are an essential component of PKI system, which is used to manage digital certificates and ensure the secure exchange of digital information.</br>
Certificate chain is a set of digital certificates that are used to establish the authenticity of a digital certificate.

## Key Terms
* **CA** (Certificate Authority) is a trusted third-party organization that issues digital certificates to entities such as websites, servers and clients.
  * Reponsible for issuing digital certificates;
  * External to organisation and they charge for the service (e.g. VeriSign, ClobalSign and etc.) These are commercial CAs;
  * Can be also internal to organisation;
* **Issuer**  is the entity that actually issues the certificate, which can be either a CA or the entity (for examppe, a company) itself.
* **Subject** is a field within the digital certificate that identifies the entity that the certificate is issued to.

  The subject field typically includes information such as the domain name or IP address of the entity, along with other identifying information such as the organization name, location, and contact information. The subject field is used by the client to verify the identity of the server or other entity it is communicating with over the TLS connection.
  
## How it works
Every browser or operating system is delivered with a set of `root cerstificate authorities` (CA) which are trusted out of the box.

**Root certificate** includes a public key which is used to verify a signuture. Root certificate *doen't include* a private key.

**Intermediate certificate** is issued by a root certificate authority (CA) and used to issue end-entity certificates. It includes both private and public keys.

**End-entity certificate** is issued by intermediate certificate. It can be either a client a server certificate. It includes both private and public keys.
  
## Chain of trust
<p align="center">
  <img src="images/chain_of_trust.png" width="110%">
</p>

#### Root Certificate
* Self-signed and self-issued (Subject = Issuer)
* Usually has long expirity date
* Trusted by web-browsers, applications and etc

#### Intermediate Certificate
* Signed by Root

#### End entity certificate
* Indentifies an entity (website)
* Signed by Intermediate CA
* Usually shortest expirity time


## Resourcses
* [Certificates explained](https://youtu.be/kAaIYRJoJkc)
* https://www.youtube.com/watch?v=Z81jegMCrfk
