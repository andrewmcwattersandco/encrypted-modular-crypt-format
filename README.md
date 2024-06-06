# encrypted-modular-crypt-format
Encrypted Modular Crypt Format (EMCF)

## Example
Given the following inputs:

* Algorithm: `aes-256-gcm`
* KDF: `7` [scrypt][1][^1]
* Salt: _S_
* IV: _IV_
* Ciphertext: _C_
* Authentication Tag: _T_

A compliant EMCF string will be formatted to output:

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

## License
Creative Commons Zero v1.0 Universal

[1]:  https://en.wikipedia.org/wiki/Scrypt
[^1]: https://en.wikipedia.org/wiki/Crypt_(C)#Key_derivation_functions_supported_by_crypt
