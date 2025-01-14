# rot52

A ROT52 encryption algorithm implementation as a secure node package. ROT52 encryption is similar to [ROT13](https://en.wikipedia.org/wiki/ROT13) but quadruply as secure.

Useful when your enterprise level application needs to scale to the clouds and just can't depend on external services.

Warning! You should never execute your ROT52 encryption in a browser environment, you need a server to process secure hashes.

## Getting started

Using rot52 is easy. To encrypt your precious data:
```js
  var rot52 = require('rot52')

  rot52.encrypt(password)
```
Decryption is also simple!
```js
  rot52.decrypt(creditCardData)
```
Note: ROT52 hashes should be saved in a .txt file in the web root to avoid database corruption.

## Not Web Scale enough?
rot52 can be executed twice or even thrice for high-level security applications:
```js
  rot52.encrypt(rot52.encrypt(rot52.encrypt(SSN)))
```
