# TLS/SSL versions

* TLS - Transport Layer Security
* SSL - Secure Socket Layer
* Terms TLS and SSL are mostly interchangeable

| SSL/TLS |  Introduced year   |Invented/Mainteined|   RFC   | Recommended to use | 
|:-------:|:-------:|:--------:|:-------:|:-------:|
|`SSL 1.0` |  1994  | Netscape |  - | No |
|`SSL 2.0` |  1995  | Netscape |  - | No |
|`SSL 3.0` |  1996  | Netscape |  - | No |
|`TLS 1.0` |  1999  |  IETF    | [RFC 2246](https://www.rfc-editor.org/rfc/rfc2246) | No (as of March 2021)|
|`[TLS 1.1]` |  2006  |  IETF    | [RFC 4346](https://www.rfc-editor.org/rfc/rfc4346) | No (as of March 2021)|
|[`TLS 1.2`](https://github.com/ebd622/docs/blob/main/tls_ssl_versions.md#tls-12) |  2008  |  IETF    | [RFC 5246](https://www.rfc-editor.org/rfc/rfc5246) | Yes |
|[`TLS 1.3`](https://github.com/ebd622/docs/blob/main/tls_ssl_versions.md#tls-13) |  2018  |  IETF    | [RFC 8446](https://www.rfc-editor.org/rfc/rfc8446) | Yes |


#### SSL 1.0
- Developed by Netscape
- Never publicly released
- Full of flaws
#### SSL 2.0
- Developed by Netscape
- Complete redesign of SSL 1.0 (to fix all flaws)
- Anyway, if was still full of flaws
#### SSL 3.0
- Complete redesign of SSL 2.0 by Netscape
- It is a foundation of TLS versions currently used
- New features:
  - Introduced concept of Certificate Chain
  - Added compression capability (vulnerability has been found there later, so compression was not really used)
  - Optional support for additional Key Exchange (SSL1.0 and SSL2.0 only supported RSA Key Exchange)
- Netscape relased it to the world, a historical copy of it is available as [RFC 6101](https://www.rfc-editor.org/rfc/rfc6101)
- Insecure as of October 2014 dur to [POODLE](https://en.wikipedia.org/wiki/POODLE) attach

#### TLS 1.0
- Renamed "TLS" when "SSL" becomeopen standard
- Protocol ownership transferred to [IETF](https://www.ietf.org/about/introduction/)
  - SSL is a protoclo invented by Netscape
  - TLS is a protocol mainteined by IETF
- Minor changes:
  - HMAC Support;
  - Required support for additional key exchange;
- Major vulnerability is BEAST (attach on CBC ciphers). It is mitigated in most modern browsers

#### TLS 1.1
- Formally deprecated "EXPORT grade" ciphers
- Protection against BEAST (vulnerability in TLC 1.0);
- Officialy TLS 1.0 and TLS 1.1 are deprecated as of March 2021 (RFC 8996). Both versions are not recommended for use on a public Internet

#### TLS 1.2
- Large similar to TLS 1.1
- Improved security of session key generation
- Introduced support for [AEAD](https://shadowsocks.org/guide/aead.html) Ciphers

#### TLS 1.3
- Major changes from prior versions of TLS/SSL;
  - Shorter handshake (2 messages vs 5+)
  - RSA is not longer supported as a method for key-exchange. [Diffie-Hellman](https://en.wikipedia.org/wiki/Diffie%E2%80%93Hellman_key_exchange) method is a more common way nowadays for exchaning sessin keys.
  - 0-RTT (round trip time) resuumption
  - Forward Secrecy required (incredibly important concept in crypthography. Using it is a huge step forward for security)
  - AEAD cihers required
- Favors security and simplicity over backwards compatibility
  - Insecure algorithms removed


### Resourcse
* [TLS / SSL Versions - Part 1 - Practical TLS](https://youtu.be/_KgZNF8nQvE)
* [TLS / SSL Versions - Part 2 - Practical TLS](https://youtu.be/fk0-UqwVNqY)



