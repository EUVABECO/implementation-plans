# EVC KEYSTORE

# Purpose

This document explains how to use the keystore deployed by EUVABECO for checking the signature of a European Vaccination Card (EVC)

# Overview

The EVCs delivered in the course of the project are signed with a cryptographic key pair specific to each signing entity.

To check this signature, it is required to have the corresponding public key. Contrary to X509 certificates, the COSE documents like the EVC do not embed the public key itself, but only a key identifier. A common and trusted store of public keys associated to the key identifiers is thus needed.

Ultimately, this keystore will be managed by a Trust Network within the WHO Global Digital Health Certification Network (DHCN). Yet, the administrative process for creating this Trust Network and enrolling all implementing partners could not be executed before the pilot implementations.

To support these implementations, an alternate keystore was created at:

<https://keys.euvabeco.eu/.well-known/jwks.json>

This keystore is built from data recorded in a common GitHub repository:

<https://github.com/EUVABECO/pub>

The following sections explain how to use, add, remove a public key from the key store.

# The keystore structure

The keystore is exposed as a JSON Web Keys Set (JWKS) structure compliant with [RFC 7517](https://datatracker.ietf.org/doc/html/rfc7517).

Each key in the set is described with a minimum set of attributes.

```json
{
"kty": "EC",
"x": "FDMpzOeGjkFpJ1mc9lo0884v_aVafspp7YkZo5TULw8",
"y": "YPfxp4DYp4O_t6LdayeW6BKNu87509Fo25Uplxo257k",
"crv": "P-256",
"kid": "SYA25A"
}
```
The “kid” term should match exactly with the key identifier used when signing the EVC.

There is a specificity here. During the COVID-19 crisis, the keystore consisted of X509 certificates, because the infrastructure to deliver such certificates already existed in countries. Such a certificate does not contain a key identifier, and the choice was made to generate key identifiers as a truncated hash of the certificate itself. Key identifiers generated in this way are sequences of bytes, but not valid strings, and this incompatible with the specification of a JSON Web key.

To support such legacy keys, we adopt the convention that if key identifier in the keystore starts with characters “0x”, the following characters are the hexadecimal representation of the key identifier.

```json
{
"kty": "EC",
"x": "S7-ibOk3VEzhFhAH55tNgRDlNQBDB3pr97KtSis5dDI",
"y": "KI7LhwoKfLa0EhwKg7Ni5RlLz0BinnTc5m4q8Qj0uIw",
"crv": "P-256",
"kid": "0xC9D8367933B4EC4C"
}
```
# Updating the keystore

## Generating a key

Generation of a JWK is not natively supported by OpenSSL. Yet, many languages (such as Java, Python, Go-Lang) include libraries to support this.

For example, in Python:
```python
import jwcrypto
from jwcrypto import jwk
key = jwk.JWK.generate(kty='EC,alg='ECDSA',crv='P-256,kid='SYA25B')
key.export_public()
```
Resulting in:
```json
'{"alg":"ECDSA",
"crv":"P-256",
"kid":"SYA25B",
"kty":"EC",
"x":"77hXNt3f65P566jxAPp9eBoPDM1V5MrWI5NaYNEO3VE",
"y":"DZb1a_DRNPKRK3aweNM8NrU3DjNWF3HISfZDRvpPDcE"}'
```

For those willing to use only OpenSSL, it is possible to derive the x and y factors from the public key.

```bash
$ openssl ecparam -name prime256v1 -genkey -noout -out private.pem
$ openssl ec -in private.pem -pubout \> public.pem
$ openssl asn1parse -in public.pem -dump

0:d=0 hl=2 l= 86 cons: SEQUENCE
2:d=1 hl=2 l= 16 cons: SEQUENCE
4:d=2 hl=2 l= 7 prim: OBJECT :id-ecPublicKey
13:d=2 hl=2 l= 5 prim: OBJECT :secp256k1
20:d=1 hl=2 l= 66 prim: BIT STRING
0000 - 00 04 96 3f bf 6e 5b 4c-ab 6c f3 72 20 f1 12 7b
0010 - 12 e8 1a 81 b5 e0 82 6e-81 04 24 a2 0e a1 11 38
0020 - 02 ce 2a 7e ad 4a 89 b2-bd 5d 9d e9 ac 6e f5 00
0030 - 3e a1 28 a0 f3 23 11 c9-85 4e d3 6c c8 1d e5 fe
0040 - de 3e
```

After the leading 00 04, the next 64 bytes correspond to x and y, that just need to be converted to base64.

For the newly generated keys, a code is assigned to each signing partner, and the key identifier will have to prefixed with this code. A suggested naming convention is Partner code, 2 digits for the year and 1 letter for the rank, such as SYA25C for the third key published by the SYADEM partner in 2025.

## The GitHub repository

The exposed keystore is built by assembling individual key files from the GitHub repository at:

<https://github.com/EUVABECO/pub>

In this repository, each signing partner has a dedicated folder /pub_keys/\<PartnerCode\> where he can manage his public keys, with one file containing the JWK token for each supported key.

Signing partners should require from SYADEM access to the repository. Once they have it, they are entitled to add, update or remove any file in their dedicated folder.

Each time a change is committed to the repository, the assembly of the keystore is triggered and the new version exposed.

It belongs to the partners to remove their outdated or compromised keys from the repository.
