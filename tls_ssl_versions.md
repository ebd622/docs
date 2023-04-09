# TLS/SSL versions

* TLS - Transport Layer Security
* SSL - Secure Socket Layer
* Terms TLS and SSL are mostly interchangeable

| SSL/TLS |  Introduced   |Mainteined|   RFC   |
|:-------:|:-------:|:--------:|:-------:|
|`SSL 1.0` |  1994  | Netscape |  - |
|`SSL 2.0` |  1995  | Netscape |  - |
|`SSL 3.0` |  1996  | Netscape |  - |
|`TLS 1.0` |  1999  |  IETF    | [RFC 2246](https://www.rfc-editor.org/rfc/rfc2246) |
|`TLS 1.1` |  2006  |  IETF    | [RFC 4346](https://www.rfc-editor.org/rfc/rfc4346) |
|`TLS 1.2` |  2008  |  IETF    | [RFC 5246](https://www.rfc-editor.org/rfc/rfc5246) |
|`TLS 1.3` |  2018  |  IETF    | [RFC 8446](https://www.rfc-editor.org/rfc/rfc8446) |


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


### Resourcse
* [TLS / SSL Versions - Part 1 - Practical TLS](https://youtu.be/_KgZNF8nQvE)
* [TLS / SSL Versions - Part 2 - Practical TLS](https://youtu.be/fk0-UqwVNqY)



