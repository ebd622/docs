# TLS/SSL versions

* TLS - Transport Layer Security
* SSL - Secure Socket Layer
* Terms TLS and SSL are mostly interchangeable

| SSL 1.0 | SSL 1.0 | SSL 1.0 | SSL 1.0 | SSL 1.0 | SSL 1.0 | SSL 1.0 |
|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|
|  1994   |  1995   |  1996   |  1999   |  2006   |  2008   |  2018   |
|  1994   |  1995   |  1996   |  1999   |  2006   |  2008   |  2018   |
|  1994   |  1995   |  1996   |  1999   |  2006   |  2008   |  2018   |
|  1994   |  1995   |  1996   |  1999   |  2006   |  2008   |  2018   |



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

#### TLS 1.0 ([RFC 2246](https://www.rfc-editor.org/rfc/rfc2246))
- Renamed "TLS" when "SSL" becomeopen standard
- Protocol ownership transferred to [IETF](https://www.ietf.org/about/introduction/)
  - SSL is a protoclo invented by Netscape
  - TLS is a protocol mainteined by IETF
- Minor changes:
  - HMAC Support;
  - Required support for additional key exchange;
- Major vulnerability is BEAST (attach on CBC ciphers). It is mitigated in most modern browsers

#### TLS 1.1 ([RFC 4346](https://www.rfc-editor.org/rfc/rfc4346))
- Formally deprecated "EXPORT grade" ciphers
- Protection against BEAST (vulnerability in TLC 1.0);
- Officialy TLS 1.0 and TLS 1.1 are deprecated as of March 2021 (RFC 8996). Both versions are not recommended for use on a public Internet




### Resourcse
* [TLS / SSL Versions - Part 1 - Practical TLS](https://youtu.be/_KgZNF8nQvE)
* [TLS / SSL Versions - Part 2 - Practical TLS](https://youtu.be/fk0-UqwVNqY)



