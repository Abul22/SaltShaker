# SaltShaker

Use nacl (tweetnacl) easily to create public private keypairs to sign, verify, encrypt and decrypt messages.

## How to use SaltShaker
Web
- https://github.com/dchest/tweetnacl-js
- https://github.com/dchest/ed2curve-js
- https://github.com/dchest/tweetnacl-util-js

Node
```
npm install saltshaker-crypto

var SaltShaker = require("saltshaker-crypto").SaltShaker;
```


## SaltShaker

```

SaltShaker.create()
= Create a new keypair

SaltShaker.create(private-key)
= Create a new keypair from private key

SaltShaker.sign(message, private-key)
= Sign a message with your private key

SaltShaker.verify(signed-message, public-key)
= Verify a sign message with a public key

SaltShaker.encrypt(message, public-key, private-key)
= Encrypt a message with a target public-key and private-key

SaltShaker.decrypt(message, nonce, public-key, private-key)
= Decrypt a message with a target public-key and private-key

SaltShaker.AESencrypt(msg,key)
= AES encrypt a msg with a symmetric key

SaltShaker.AESdecrypt(msg,key)
= AES decrypt a msg with a symmetric key

```

## Example

```

var x = SaltShaker.create();

var y = null;

console.log(y = SaltShaker.sign("Hello",x.privatekey));

console.log(SaltShaker.verify(y,x.publickey));

console.log(y = SaltShaker.encrypt("Test",x.publickey,x.privatekey));

console.log(SaltShaker.decrypt(y.message, y.nonce, x.publickey, x.privatekey));

console.log(y = SaltShaker.encryptPSK("lol","hy"));

console.log(SaltShaker.decryptPSK(y.message,"hy",y.nonce));

```

## License

Copyright (c) 2019 Andrew Lee
