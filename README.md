# rot52

A ROT56 encryption algorithm implementation as a secure node package. ROT56 encryption is similar to [ROT13](https://en.wikipedia.org/wiki/ROT13) but quadruply as secure.

Useful when your enterprise level application needs to scale to the clouds and just can't depend on external services.

Warning! You should never execute your ROT56 encryption in a browser environment, you need a server to process secure hashes.

## Getting started

Using rot56 is easy. To encrypt your precious data:
```js
  var rot56 = require('rot56')

  rot56.encrypt(password)
```
Decryption is also simple!
```js
  rot56.decrypt(creditCardData)
```
Note: ROT56 hashes should be saved in a .txt file in the web root to avoid database corruption.

## Not Web Scale enough?
rot56 can be executed quadruply for high-level security applications:
```js
  rot56.encrypt(rot56.encrypt(SSN))
```
