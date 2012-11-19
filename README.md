iAnonym
===

Anonymity into your browser everywhere from any device

## Presentation :

See http://www.ianonym.com

Extended browserification of https://github.com/Ayms/node-Tor, using Tor or a Tor like network, one unique javascript code for all platforms.

## Browser's required modules and status :

OP
* mix node.js Buffers and Typed Arrays --> OK, see https://github.com/Ayms/node-typedarray
* URL parser --> OK
* HTTP parser --> OK
* self signed certificates generation (OP) --> TBD inspired from forge + cryptoJS (modified Webcrypto like)
* certificates verification (OP) --> TBD inspired from forge + cryptoJS (modified Webcrypto like)
* implement TLS protocol (OP, inside websockets, both client and server side) --> TBD inspired from forge + cryptoJS (modified Webcrypto like)
* retrieve the certificate used for the first TLS connection between the page and the OP (Evil1 attack) --> NOK (W3C request Webcrypto API Group)
* implement Tor protocol and Tor protocol websocket extension (OP, inside websockets) --> OK
* Webcrypto like features http://www.w3.org/TR/WebCryptoAPI/ (hash, encrypt, decrypt, rsa, aes, etc), including Tor specific ones (RSA_PKCS1_OAEP_PADDING, aes-128-ctr) --> TBD inspired from cryptoJS (modified Webcrypto like)

OR
* websocket protocol (server side) --> OK
* websocket Tor protocol extension --> OK
	
## Tests :

See https://github.com/Ayms/node-Tor/blob/master/test/log-anonym.txt
	
## Related projects :

[Ayms/node-Tor](https://github.com/Ayms/node-Tor)
[Ayms/node-typedarray](https://github.com/Ayms/node-typedarray)
[Ayms/node-dom](https://github.com/Ayms/node-dom)
[Ayms/node-bot](https://github.com/Ayms/node-bot)
[Ayms/node-gadgets](https://github.com/Ayms/node-gadgets)
