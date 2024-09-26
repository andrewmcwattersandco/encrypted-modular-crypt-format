# encrypted-modular-crypt-format
Encrypted Modular Crypt Format (EMCF)

## Examples
Given the following inputs:

* Algorithm: `aes-256-gcm`
* Key Identifier: K
* IV: _IV_
* Ciphertext: _C_
* Authentication Tag: _T_

A compliant EMCF string will be formatted to output:

```emcf
$aes-256-gcm$K$IV||C||T
```

### Password-based symmetric encryption
Given the following inputs:

* KDF: `7` [scrypt][1][^1]
* Salt: _S_

```emcf
$aes-256-gcm$7$S$IV||C||T
```

### Envelope encryption
Given the following inputs:

* Wrapped DEK: D

```emcf
$aes-256-gcm$D$IV||C||T
```

## Prior art
* Modular Crypt Format  
  https://passlib.readthedocs.io/en/stable/modular_crypt_format.html
* PHC String Format  
  https://github.com/P-H-C/phc-string-format/blob/master/phc-sf-spec.md

## See also
* Binary Modular Crypt Format (BMCF)  
  https://github.com/ademarre/binary-mcf
* SP 800-38D, Recommendation for Block Cipher Modes of Operation: Galois/Counter Mode (GCM) and GMAC | CSRC  
  https://csrc.nist.gov/pubs/sp/800/38/d/final

## License
Creative Commons Zero v1.0 Universal

[1]:  https://en.wikipedia.org/wiki/Scrypt
[^1]: https://en.wikipedia.org/wiki/Crypt_(C)#Key_derivation_functions_supported_by_crypt
