iAnonym
===

Anonymity into your browser everywhere from any device

## Presentation :

See http://www.ianonym.com

Extended browserification of https://github.com/Ayms/node-Tor, using Tor or a Tor like network, one unique javascript code for all platforms.

## Browser's required modules and status :

OP
* mix node.js's Buffers and Typed Arrays --> OK, see https://github.com/Ayms/node-typedarray
* URL parser --> OK
* HTTP parser --> OK
* Secure script to control the page --> OK
* self signed certificates generation (OP) --> TBD
* certificates verification (OP) --> TBD
* implement TLS protocol (OP, inside websockets, both client and server side) --> TBD
* retrieve the certificate used for the first TLS connection between the page and the OP (Evil1 attack) --> NOK (W3C request Webcrypto API Group http://www.w3.org/2012/webcrypto/)
* implement Tor protocol and websocket Tor protocol extension (OP, inside websockets) --> OK
* Webcrypto like features http://www.w3.org/TR/WebCryptoAPI/ (hash, encrypt, decrypt, rsa, aes, etc), including Tor specific ones (RSA_PKCS1_OAEP_PADDING, aes-128-ctr) --> TBD

OR
* websocket protocol (server side) --> OK
* websocket Tor protocol extension --> OK

Related or to be considered (for TBD resolution, inspired or built-in, the requirement being that everything must work into all browsers and follow the existing and future standards) :

* [The W3C Webcrypto Working Group] (http://www.w3.org/2012/webcrypto/)
* [The IETF JOSE (Javascript Object Signing and Encryption) Working Group] (http://tools.ietf.org/wg/jose/charters)
* [The IETF RTCWeb Working Group] (http://tools.ietf.org/wg/rtcweb/)
* [The W3C WebRTC Working Group] (http://www.w3.org/2011/04/webrtc/)
* [The W3C Web Applications Security Working Group] (http://www.w3.org/2011/webappsec/)
* [The W3C WebApps Working Group] (http://www.w3.org/2008/webapps/)
* [DomCrypt in Mozilla and Chrome] (https://wiki.mozilla.org/Privacy/Features/DOMCryptAPISpec/Latest)
* [Microsoft Cryptographic API] (http://msdn.microsoft.com/en-us/library/aa380256.aspx)
* [Microsoft Next-Generation Cryptographic API] (http://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx)
* [The Stanford Javascript Crypto library] (http://crypto.stanford.edu/sjcl/)
* [Forge] (https://github.com/digitalbazaar/forge)
* [cryptoJS] (http://code.google.com/p/crypto-js/)

## Tests :

See https://github.com/Ayms/node-Tor/blob/master/test/log-anonym.txt
	
## Related projects :

* [Ayms/node-Tor](https://github.com/Ayms/node-Tor)
* [Ayms/node-typedarray](https://github.com/Ayms/node-typedarray)
* [Ayms/node-dom](https://github.com/Ayms/node-dom)
* [Ayms/node-bot](https://github.com/Ayms/node-bot)
* [Ayms/node-gadgets](https://github.com/Ayms/node-gadgets)
