#### Manage Namespaces with Github Pages

<h4 id="publicKeyJwk"><a href="#publicKeyJwk">publicKeyJwk</a></h4>

A secp256k1 public key in JWK format. A JSON Web Key (JWK) is a JavaScript Object Notation (JSON) data structure that represents a cryptographic key. Read [RFC7517](https://tools.ietf.org/html/rfc7517).

#### Example:

```json
{
  "id": "did:example:123#key-0",
  "controller": "did:example:123",
  "type": "EcdsaSecp256k1VerificationKey2019",
  "publicKeyJwk": {
    "crv": "secp256k1",
    "kty": "EC",
    "x": "dWCvM4fTdeM0KmloF57zxtBPXTOythHPMm1HCLrdd3A",
    "y": "36uMVGM7hnw-N6GnjFcihWE3SkrhMLzzLCdPMXPEXlA"
  }
}
```
