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
* Webcrypto like features http://www.w3.org/TR/WebCryptoAPI/ (hash, encrypt, decrypt, rsa, aes, dh, etc), including Tor specific ones (RSA_PKCS1_OAEP_PADDING, aes-128-ctr) --> TBD

OR
* websocket protocol (server side) --> OK
* websocket Tor protocol extension --> OK

Related and to be considered (for TBD resolution, inspired or built-in, the requirement being that everything must work into all browsers (fix and mobile) and follow the existing and future standards) :

* [The W3C Webcrypto Working Group] (http://www.w3.org/2012/webcrypto/) [and status] (http://it.slashdot.org/story/12/09/18/1526236/w3c-releases-first-working-draft-of-web-crypto-api)
* [DomCrypt (Webcrypto compatible) in Mozilla] (https://addons.mozilla.org/en-US/firefox/addon/domcrypt/) [and WebKit(Chrome/Safari/others)] (https://bugs.webkit.org/show_bug.cgi?id=62010) [and IE ?] (http://slashdot.org/comments.pl?sid=3126489&cid=41375473)
* [ArrayBuffer and Typed Arrays] (http://www.khronos.org/registry/typedarray/specs/latest/) [and implementation status] (https://developer.mozilla.org/en-US/docs/JavaScript_typed_arrays/ArrayBuffer#Browser_compatibility)
* [TextEncoder and TextDecoder](http://encoding.spec.whatwg.org/#api ) [and implementation] (http://code.google.com/p/stringencoding/)
* [The W3C Web Applications Security Working Group] (http://www.w3.org/2011/webappsec/) [and Content Security policy] (http://www.w3.org/TR/CSP/)
* [Forge (TLS implementation)] (https://github.com/digitalbazaar/forge)
* [The Stanford Javascript Crypto library] (http://crypto.stanford.edu/sjcl/)
* [cryptoJS] (http://code.google.com/p/crypto-js/)
* [The W3C WebApps Working Group] (http://www.w3.org/2008/webapps/wiki/PubStatus#API_Specifications)

Secondary interest :

* [The W3C WebRTC Working Group] (http://www.w3.org/2011/04/webrtc/)
* [Microsoft Cryptographic API] (http://msdn.microsoft.com/en-us/library/aa380256.aspx)
* [Microsoft Next-Generation Cryptographic API] (http://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx)

## Tests :

See https://github.com/Ayms/node-Tor/blob/master/test/log-anonym.txt
	
## Related projects :

* [Ayms/node-Tor](https://github.com/Ayms/node-Tor)
* [Ayms/node-typedarray](https://github.com/Ayms/node-typedarray)
* [Ayms/node-dom](https://github.com/Ayms/node-dom)
* [Ayms/node-bot](https://github.com/Ayms/node-bot)
* [Ayms/node-gadgets](https://github.com/Ayms/node-gadgets)
