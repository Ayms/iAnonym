iAnonym
===

Anonymity into your browser everywhere from any device

## Presentation :

See http://www.ianonym.com

Extended browserification of https://github.com/Ayms/node-Tor, using Tor or a Tor like network, one unique javascript code for all platforms.

## Browser's modules :

OP
	- mix node.js Buffers and Typed Arrays
    - URL parser
    - HTTP parser
    - self signed certificates generation (OP)
    - certificates verification (OP)
    - implement TLS protocol (OP, inside websockets, both client and server side)
    - retrieve the certificate used for the first TLS connection between the page and the OP (Evil1 attack)
    - implement Tor protocol and Tor protocol websocket extension (OP, inside websockets)
    - Webcrypto like features (hash, encrypt, decrypt, rsa, aes, etc), including Tor specific ones (RSA_PKCS1_OAEP_PADDING, aes-128-ctr)

OR
	- websocket protocol (server side)
	- websocket Tor protocol extension
	
## Tests :

See https://github.com/Ayms/node-Tor/blob/master/test/log-anonym.txt
	
## Related projects :

[Ayms/node-Tor](https://github.com/Ayms/node-Tor)
[Ayms/node-typedarray](https://github.com/Ayms/node-typedarray)
[Ayms/node-dom](https://github.com/Ayms/node-dom)
[Ayms/node-bot](https://github.com/Ayms/node-bot)
[Ayms/node-gadgets](https://github.com/Ayms/node-gadgets)
