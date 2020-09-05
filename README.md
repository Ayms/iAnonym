iAnonym
===

Anonymity into your browser everywhere from any device

## Crowdfunding campaign launched on Kickstarter the 19th of June for 40 days, you're welcome to contribute

[iAnonym kickstarter campaign] (http://www.kickstarter.com/projects/450023/ianonym-internet-privacy-everywhere-from-any-devic)

## Presentation :

See http://ianonym.peersm.com

Extended browserification of https://github.com/Ayms/node-Tor, using Tor or a Tor like network, one unique javascript code for all platforms.

9th February 2013 : first successfull complete communication from the browser with the OP js inside the browser, see the results [First loading - in black the OR,in white the OP inside the browser with web console messages] (http://ianonym.peersm.com/img/first_browser_page3.jpg) 

It's already fast while no optimization efforts have been made.

## Browser's required modules and status :

OP
* mix node.js's Buffers and Typed Arrays --> OK, see https://github.com/Ayms/node-typedarray
* URL parser --> OK
* HTTP parser --> OK
* Secure script to control the page --> OK
* self signed certificates generation (OP) --> OK
* certificates verification (OP) --> OK
* implement TLS protocol (OP, inside websockets, both client and server side) --> OK, see [Ayms/abstract-tls](https://github.com/Ayms/abstract-tls)
* retrieve the certificate used for the first TLS connection between the page and the OP (Evil1 attack) --> OK, see [Interception Detector](http://ianonym.peersm.com/intercept.html)
* implement Tor protocol and websocket Tor protocol extension (OP, inside websockets) --> OK
* Webcrypto like features http://www.w3.org/TR/WebCryptoAPI/ (hash, encrypt, decrypt, rsa, aes, dh, etc) --> OK, cryptoJS, jsbn and polycrypt (conversion fonctions) + RELAY_INFO

OR
* websocket protocol --> OK, see https://github.com/Ayms/websocket
* websocket Tor protocol extension --> OK (RELAY_WS, RELAY_ASSOCIATE, RELAY_INFO, CREATE_FAST_WS, CREATED_FAST_WS - see see https://github.com/Ayms/node-Tor)

Related :

* [The W3C Webcrypto Working Group] (http://www.w3.org/2012/webcrypto/) [and status] (http://it.slashdot.org/story/12/09/18/1526236/w3c-releases-first-working-draft-of-web-crypto-api)
* [DomCrypt (Webcrypto compatible) in Mozilla] (https://addons.mozilla.org/en-US/firefox/addon/domcrypt/)
* [ArrayBuffer / Typed Arrays] (http://www.khronos.org/registry/typedarray/specs/latest/) [and implementation status] (https://developer.mozilla.org/en-US/docs/JavaScript_typed_arrays/ArrayBuffer#Browser_compatibility)
* [TextEncoder / TextDecoder](http://encoding.spec.whatwg.org/#api ) [and implementation] (http://code.google.com/p/stringencoding/)
* TC39 ECMAScript and SES concepts + [Object.observe] (http://wiki.ecmascript.org/doku.php?id=harmony:observe)
* [Forge (TLS implementation)] (https://github.com/digitalbazaar/forge)
* [The Stanford Javascript Crypto library] (http://crypto.stanford.edu/sjcl/)
* [cryptoJS] (http://code.google.com/p/crypto-js/)
* [jsbn] (http://www-cs-students.stanford.edu/~tjw/jsbn/)
* [PolyCrypt] (http://github.com/polycrypt/polycrypt/)
* [The W3C WebApps Working Group] (http://www.w3.org/2008/webapps/wiki/PubStatus#API_Specifications)

Secondary interest :

* [The W3C Web Applications Security Working Group] (http://www.w3.org/2011/webappsec/) [and Content Security policy] (http://www.w3.org/TR/CSP/)
* [The W3C WebRTC Working Group] (http://www.w3.org/2011/04/webrtc/)

## Status and Tests :

####This section is deprecated since now everything is working inside the browser, we keep it for historical reasons.

See https://github.com/Ayms/node-Tor/blob/master/test/log-anonym.txt

You can try it Live (soon) :
* set the socks proxy V5 interface of your browser to IP 213.246.53.127 port xxx (to come) (on Firefox : Options/Advanced/Network/Parameters/Manual configuration of proxy), clear the cache/history, close your browser and reopen it
* enter url http://www.f4116a30c08bbdfd01813b96c909.com (fake domain)
* this will load the press public site www.lepoint.fr (a huge public site, therefore a good test site), you can use the web console (or network analyzer) to check that all requests from the browser are toward www.f4116a30c08bbdfd01813b96c909.com domain, the local resources urls (www.f4116a30c08bbdfd01813b96c909.com/logo.png) are not encrypted (but can not be seen when TLS will be implemented), the outside resources urls are encrypted and look like www.f4116a30c08bbdfd01813b96c909.com/ac496a69dbc0abf30b8a2dd7c0105509589a636c391e1e5d04d9e9170644ef2e573b55dcd701acc85

See http://ianonym.peersm.com Details section for url encoding.

* some requests can still appear to be on the domain www.lepoint.fr, this is because for now urls contained in css files are not filtered.

The test configuration is :

	[Browser] 		| <--socks--------------------------> |
					|									  |	[node-Tor_OR] <-----> [Tor Network] <-----> [Site]
	[node-Tor_OP]	| <--websocket RELAY_WS/ASSOCIATE---> |
					|	 RELAY_BEGIN/CONN/DATA			  |

See [Ayms/node-Tor](https://github.com/Ayms/node-Tor) for RELAY_WS/ASSOCIATE

## Related projects :

* [Ayms/node-Tor](https://github.com/Ayms/node-Tor)
* [Interception Detector](http://ianonym.peersm.com/intercept.html)
* [Ayms/abstract-tls](https://github.com/Ayms/abstract-tls)
* [Ayms/websocket](https://github.com/Ayms/websocket)
* [Ayms/node-typedarray](https://github.com/Ayms/node-typedarray)
* [Ayms/node-dom](https://github.com/Ayms/node-dom)
* [Ayms/node-bot](https://github.com/Ayms/node-bot)
* [Ayms/node-gadgets](https://github.com/Ayms/node-gadgets)
