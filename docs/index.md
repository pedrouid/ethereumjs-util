<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [addHexPrefix](#addhexprefix)
-   [baToJSON](#batojson)
-   [BN](#bn)
-   [bufferToHex](#buffertohex)
-   [bufferToInt](#buffertoint)
-   [defineProperties](#defineproperties)
-   [ecrecover](#ecrecover)
-   [ecsign](#ecsign)
-   [fromRpcSig](#fromrpcsig)
-   [fromSigned](#fromsigned)
-   [generateAddress](#generateaddress)
-   [hashPersonalMessage](#hashpersonalmessage)
-   [importPublic](#importpublic)
-   [isPrecompiled](#isprecompiled)
-   [isValidAddress](#isvalidaddress)
-   [isValidChecksumAddress](#isvalidchecksumaddress)
-   [isValidPrivate](#isvalidprivate)
-   [isValidPublic](#isvalidpublic)
-   [privateToAddress](#privatetoaddress)
-   [pubToAddress](#pubtoaddress)
-   [ripemd160](#ripemd160)
-   [rlp](#rlp)
-   [rlphash](#rlphash)
-   [secp256k1](#secp256k1)
-   [setLengthRight](#setlengthright)
-   [sha256](#sha256)
-   [sha3](#sha3)
-   [toBuffer](#tobuffer)
-   [toChecksumAddress](#tochecksumaddress)
-   [toRpcSig](#torpcsig)
-   [toUnsigned](#tounsigned)
-   [unpad](#unpad)
-   [isValidSignature](#isvalidsignature)
-   [isZeroAddress](#iszeroaddress)
-   [lsetLength](#lsetlength)
-   [MAX_INTEGER](#max_integer)
-   [privateToPublic](#privatetopublic)
-   [SHA3_NULL](#sha3_null)
-   [SHA3_NULL_S](#sha3_null_s)
-   [SHA3_RLP](#sha3_rlp)
-   [SHA3_RLP_ARRAY](#sha3_rlp_array)
-   [SHA3_RLP_ARRAY_S](#sha3_rlp_array_s)
-   [SHA3_RLP_S](#sha3_rlp_s)
-   [TWO_POW256](#two_pow256)
-   [zeroAddress](#zeroaddress)
-   [zeros](#zeros)

## addHexPrefix

[index.js:525-531](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L525-L531 "Source code on GitHub")

Adds "0x" to a given `String` if it does not already start with "0x"

**Parameters**

-   `str` **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

## baToJSON

[index.js:574-584](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L574-L584 "Source code on GitHub")

Converts a `Buffer` or `Array` to JSON

**Parameters**

-   `ba` **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array))** 

Returns **([Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) | null)** 

## BN

[index.js:62-62](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L62-L62 "Source code on GitHub")

[`BN`](https://github.com/indutny/bn.js)

Type: [Function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)

## bufferToHex

[index.js:192-195](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L192-L195 "Source code on GitHub")

Converts a `Buffer` into a hex `String`

**Parameters**

-   `buf` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

## bufferToInt

[index.js:183-185](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L183-L185 "Source code on GitHub")

Converts a `Buffer` to a `Number`

**Parameters**

-   `buf` **[Buffer](https://nodejs.org/api/buffer.html)** 


-   Throws **any** If the input number exceeds 53 bits.

Returns **[Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

## defineProperties

[index.js:596-689](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L596-L689 "Source code on GitHub")

Defines properties on a `Object`. It make the assumption that underlying data is binary.

**Parameters**

-   `self` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** the `Object` to define properties on
-   `fields` **[Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)** an array fields to define. Fields can contain:-   `name` - the name of the properties
    -   `length` - the number of bytes the field can have
    -   `allowLess` - if the field can be less than the length
    -   `allowEmpty`
-   `data` **any** data to be validated against the definitions

## ecrecover

[index.js:370-378](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L370-L378 "Source code on GitHub")

ECDSA public key recovery from signature

**Parameters**

-   `msgHash` **[Buffer](https://nodejs.org/api/buffer.html)** 
-   `v` **[Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `r` **[Buffer](https://nodejs.org/api/buffer.html)** 
-   `s` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[Buffer](https://nodejs.org/api/buffer.html)** publicKey

## ecsign

[index.js:339-347](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L339-L347 "Source code on GitHub")

ECDSA sign

**Parameters**

-   `msgHash` **[Buffer](https://nodejs.org/api/buffer.html)** 
-   `privateKey` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** 

## fromRpcSig

[index.js:408-427](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L408-L427 "Source code on GitHub")

Convert signature format of the `eth_sign` RPC method to signature parameters
NOTE: all because of a bug in geth: <https://github.com/ethereum/go-ethereum/issues/2053>

**Parameters**

-   `sig` **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** 

## fromSigned

[index.js:202-204](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L202-L204 "Source code on GitHub")

Interprets a `Buffer` as a signed integer and returns a `BN`. Assumes 256-bit numbers.

**Parameters**

-   `num` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **BN** 

## generateAddress

[index.js:494-508](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L494-L508 "Source code on GitHub")

Generates an address of a newly created contract

**Parameters**

-   `from` **[Buffer](https://nodejs.org/api/buffer.html)** the address which is creating this new address
-   `nonce` **[Buffer](https://nodejs.org/api/buffer.html)** the nonce of the from account

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## hashPersonalMessage

[index.js:357-360](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L357-L360 "Source code on GitHub")

Returns the keccak-256 hash of `message`, prefixed with the header used by the `eth_sign` RPC call.
The output of this function can be fed into `ecsign` to produce the same signature as the `eth_sign`
call for a given `message`, or fed to `ecrecover` along with a signature to recover the public key
used to produce the signature.

**Parameters**

-   `message`  

Returns **[Buffer](https://nodejs.org/api/buffer.html)** hash

## importPublic

[index.js:325-331](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L325-L331 "Source code on GitHub")

Converts a public key to the Ethereum format.

**Parameters**

-   `publicKey` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## isPrecompiled

[index.js:515-518](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L515-L518 "Source code on GitHub")

Returns true if the supplied address belongs to a precompiled account

**Parameters**

-   `address` **([Buffer](https://nodejs.org/api/buffer.html) \| [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))** 

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

## isValidAddress

[index.js:443-445](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L443-L445 "Source code on GitHub")

Checks if the address is a valid. Accepts checksummed addresses too

**Parameters**

-   `address` **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

## isValidChecksumAddress

[index.js:484-486](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L484-L486 "Source code on GitHub")

Checks if the address is a valid checksummed address

**Parameters**

-   `address` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

## isValidPrivate

[index.js:268-270](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L268-L270 "Source code on GitHub")

Checks if the private key satisfies the rules of the curve secp256k1.

**Parameters**

-   `privateKey` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

## isValidPublic

[index.js:279-290](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L279-L290 "Source code on GitHub")

Checks if the public key satisfies the rules of the curve secp256k1
and the requirements of Ethereum.

**Parameters**

-   `publicKey` **[Buffer](https://nodejs.org/api/buffer.html)** The two points of an uncompressed key, unless sanitize is enabled
-   `sanitize` **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Accept public keys in other formats (optional, default `false`)

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

## privateToAddress

[index.js:434-436](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L434-L436 "Source code on GitHub")

Returns the ethereum address of a given private key

**Parameters**

-   `privateKey` **[Buffer](https://nodejs.org/api/buffer.html)** A private key must be 256 bits wide

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## pubToAddress

[index.js:299-307](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L299-L307 "Source code on GitHub")

Returns the ethereum address of a given public key.
Accepts "Ethereum public keys" and SEC1 encoded keys.

**Parameters**

-   `pubKey` **[Buffer](https://nodejs.org/api/buffer.html)** The two points of an uncompressed key, unless sanitize is enabled
-   `sanitize` **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Accept public keys in other formats (optional, default `false`)

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## ripemd160

[index.js:244-252](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L244-L252 "Source code on GitHub")

Creates RIPEMD160 hash of the input

**Parameters**

-   `a` **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))** the input data
-   `padded` **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** whether it should be padded to 256 bits or not

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## rlp

[index.js:68-68](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L68-L68 "Source code on GitHub")

[`rlp`](https://github.com/ethereumjs/rlp)

Type: [Function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)

## rlphash

[index.js:259-261](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L259-L261 "Source code on GitHub")

Creates SHA-3 hash of the RLP encoded version of the input

**Parameters**

-   `a` **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))** the input data

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## secp256k1

[index.js:74-74](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L74-L74 "Source code on GitHub")

[`secp256k1`](https://github.com/cryptocoinjs/secp256k1-node/)

Type: [Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)

## setLengthRight

[index.js:131-133](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L131-L133 "Source code on GitHub")

Right Pads an `Array` or `Buffer` with leading zeros till it has `length` bytes.
Or it truncates the beginning if it exceeds.

**Parameters**

-   `msg` **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array))** the value to pad
-   `length` **[Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** the number of bytes the output should be

Returns **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array))** 

## sha256

[index.js:233-236](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L233-L236 "Source code on GitHub")

Creates SHA256 hash of the input

**Parameters**

-   `a` **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))** the input data

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## sha3

[index.js:221-226](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L221-L226 "Source code on GitHub")

Creates SHA-3 hash of the input

**Parameters**

-   `a` **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))** the input data
-   `bits` **[Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** the SHA width (optional, default `256`)

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## toBuffer

[index.js:153-175](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L153-L175 "Source code on GitHub")

Attempts to turn a value into a `Buffer`. As input it supports `Buffer`, `String`, `Number`, null/undefined, `BN` and other objects with a `toArray()` method.

**Parameters**

-   `v` **any** the value

## toChecksumAddress

[index.js:463-477](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L463-L477 "Source code on GitHub")

Returns a checksummed address

**Parameters**

-   `address` **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

## toRpcSig

[index.js:387-400](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L387-L400 "Source code on GitHub")

Convert signature parameters into the format of `eth_sign` RPC method

**Parameters**

-   `v` **[Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `r` **[Buffer](https://nodejs.org/api/buffer.html)** 
-   `s` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** sig

## toUnsigned

[index.js:211-213](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L211-L213 "Source code on GitHub")

Converts a `BN` to an unsigned integer and returns it as a `Buffer`. Assumes 256-bit numbers.

**Parameters**

-   `num` **BN** 

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## unpad

[index.js:140-148](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L140-L148 "Source code on GitHub")

Trims leading zeros from a `Buffer` or an `Array`

**Parameters**

-   `a` **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))** 

Returns **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))** 

## isValidSignature

[index.js:543-567](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L543-L567 "Source code on GitHub")

Validate ECDSA signature

**Parameters**

-   `v` **[Buffer](https://nodejs.org/api/buffer.html)** 
-   `r` **[Buffer](https://nodejs.org/api/buffer.html)** 
-   `s` **[Buffer](https://nodejs.org/api/buffer.html)** 
-   `homestead` **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)**  (optional, default `true`)

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

## isZeroAddress

[index.js:453-456](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L453-L456 "Source code on GitHub")

Checks if a given address is a zero address

**Parameters**

-   `address` **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

## lsetLength

[index.js:106-122](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L106-L122 "Source code on GitHub")

Left Pads an `Array` or `Buffer` with leading zeros till it has `length` bytes.
Or it truncates the beginning if it exceeds.

**Parameters**

-   `msg` **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array))** the value to pad
-   `length` **[Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** the number of bytes the output should be
-   `right` **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** whether to start padding form the left or right (optional, default `false`)

Returns **([Buffer](https://nodejs.org/api/buffer.html) \| [Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array))** 

## MAX_INTEGER

[index.js:14-14](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L14-L14 "Source code on GitHub")

the max integer that this VM can handle (a `BN`)

Type: BN

## privateToPublic

[index.js:314-318](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L314-L318 "Source code on GitHub")

Returns the ethereum public key of a given private key

**Parameters**

-   `privateKey` **[Buffer](https://nodejs.org/api/buffer.html)** A private key must be 256 bits wide

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 

## SHA3_NULL

[index.js:32-32](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L32-L32 "Source code on GitHub")

SHA3-256 hash of null (a `Buffer`)

Type: [Buffer](https://nodejs.org/api/buffer.html)

## SHA3_NULL_S

[index.js:26-26](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L26-L26 "Source code on GitHub")

SHA3-256 hash of null (a `String`)

Type: [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)

## SHA3_RLP

[index.js:56-56](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L56-L56 "Source code on GitHub")

SHA3-256 hash of the RLP of null (a `Buffer`)

Type: [Buffer](https://nodejs.org/api/buffer.html)

## SHA3_RLP_ARRAY

[index.js:44-44](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L44-L44 "Source code on GitHub")

SHA3-256 of an RLP of an empty array (a `Buffer`)

Type: [Buffer](https://nodejs.org/api/buffer.html)

## SHA3_RLP_ARRAY_S

[index.js:38-38](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L38-L38 "Source code on GitHub")

SHA3-256 of an RLP of an empty array (a `String`)

Type: [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)

## SHA3_RLP_S

[index.js:50-50](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L50-L50 "Source code on GitHub")

SHA3-256 hash of the RLP of null  (a `String`)

Type: [String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)

## TWO_POW256

[index.js:20-20](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L20-L20 "Source code on GitHub")

2^256 (a `BN`)

Type: BN

## zeroAddress

[index.js:91-95](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L91-L95 "Source code on GitHub")

Returns a zero address

Returns **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

## zeros

[index.js:82-84](https://github.com/ethereumjs/ethereumjs-util/blob/0bc0616c2de0de0723f87c3b64923bb9f962a8e1/index.js#L82-L84 "Source code on GitHub")

Returns a buffer filled with 0s

**Parameters**

-   `bytes` **[Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** the number of bytes the buffer should be

Returns **[Buffer](https://nodejs.org/api/buffer.html)** 
