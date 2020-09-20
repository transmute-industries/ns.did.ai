---
layout: respec
---

<section id="abstract">
  <p>
    This specification describes an Ed25519 Signature Suite created in 2020
    for the Linked Data Proof specification. The Signature Suite utilizes
    Ed25519 EdDSA signatures and multibase.
  </p>
</section>

<section id="sotd">
  <p>
    This is an experimental specification and is undergoing regular
    revisions. It is not fit for production deployment.
  </p>
</section>

<section id="terminology">
  <h2>Terminology</h2>
  <p>
    The following terms are used to describe concepts involved in the
    generation and verification of the Linked Data Proof
    <a>signature suite</a>.
  </p>

  <dl>
    <dt><dfn>signature suite</dfn></dt>
    <dd>
      A specified set of cryptographic primitives typically consisting of a
      canonicalization algorithm, a message digest algorithm, and a
      signature algorithm that are bundled together by cryptographers for
      developers for the purposes of safety and convenience.
    </dd>
    <dt><dfn>canonicalization algorithm</dfn></dt>
    <dd>
      An algorithm that takes an input document that has more than one
      possible representation and always transforms it into a
      <a>canonical form</a>. This process is sometimes also called
      normalization.
    </dd>
    <dt>
      <dfn data-lt="message digest algorithm | message digest algorithms"
        >message digest algorithm</dfn
      >
    </dt>
    <dd>
      An algorithm that takes a message, prefferably in some
      <a>canonical form</a> and produces a cryptographic output called a
      digest that is often many orders of magnitude smaller than the input
      message. These algorithms are often 1) very fast, 2) non-reversible,
      3) cause the output to change significantly when even one bit of the
      input message changes, and 4) make it infeasible to find two different
      inputs for the same output.
    </dd>
    <dt><dfn>canonical form</dfn></dt>
    <dd>
      The output of applying a <a>canonicalization algorithm</a> to an input
      document.
    </dd>
    <dt><dfn>signature algorithm</dfn></dt>
    <dd>
      An algorithm that takes an input message and produces an output value
      where the receiver of the message can mathematically verify that the
      message has not been modified in transit and came from someone
      possessing a particular secret.
    </dd>
    <dt>
      <dfn data-lt="linked data document|linked data documents"
        >linked data document</dfn
      >
    </dt>
    <dd>A document comprised of linked data.</dd>
    <dt>
      <dfn data-lt="linked data proof|linked data proofs"
        >linked data proof</dfn
      >
    </dt>
    <dd>
      A
      <a
        href="https://w3c-ccg.github.io/ld-proofs/#dfn-linked-data-proof"
        class="externalDFN"
        >linked data proof</a
      >
      which is a set of attributes that represent a linked data digital
      proof and the parameters required to verify it as defined by
      [[RDF-N-Quads]].
    </dd>
    <dt><dfn>linked data proof document</dfn></dt>
    <dd>
      A <a>linked data document</a> featuring one or more
      <a>linked data proofs</a>.
    </dd>

    <dt><dfn>Ed25519VerificationKey2020</dfn></dt>
    <dd>
      The <code>type</code> of the verification method for the signature
      suite <a>Ed25519Signature2020</a>.
    </dd>

    <dt><dfn>Ed25519Signature2020</dfn></dt>
    <dd>
      The <code>type</code> of the linked data proof for the signature suite
      <a>Ed25519Signature2020</a>.
    </dd>

  </dl>
</section>

## test markdown

#### Example:

<p class="red43">ehllo asdfadsf</p>

```json
{
  "id": "did:example:123#key-0",
  "controller": "did:example:123",
  "type": "JsonWebKey2020",
  "publicKeyJwk": {
    "crv": "secp256k1",
    "kty": "EC",
    "x": "dWCvM4fTdeM0KmloF57zxtBPXTOythHPMm1HCLrdd3A",
    "y": "36uMVGM7hnw-N6GnjFcihWE3SkrhMLzzLCdPMXPEXlA"
  }
}
```
