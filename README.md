# skwd-lens-model

The default semantic model pack for [skwd-lens](https://github.com/liixini/skwd-wall),
distributed as a release asset rather than checked into source.

Semantic search in Skwd works out of the box because this pack ships with it.
It is a build artifact, not source, and is versioned independently of the
suite — a suite point release does not republish the weights.

## Contents

| | |
|---|---|
| Image encoder | SigLIP 2 base, patch 16, 224px, int8 |
| Text encoder | SigLIP 2 base text, int8, with a quantised token-embedding table |
| Tokenizer | SentencePiece model |
| Runtime | ONNX Runtime 1.27.0 (x86_64) |

The pack is `usr/share/skwd-lens/models/semantic/` once installed. A pack
installed per user takes precedence over this one, so a different model can be
supplied with `skwd-lens pack install` without removing this package.

## Installing

Install the `skwd-lens-model` package for your distribution. It is a hard
dependency of `skwd-lens`, so a package manager pulls it in automatically.

To verify a downloaded archive:

```sh
sha256sum -c skwd-lens-model-1.0.0.tar.xz.sha256
```

## Licensing

The pack bundles third-party material under Apache-2.0, CC-BY-4.0, and MIT.
The full texts ship inside the archive under `licenses/` and are installed to
`/usr/share/licenses/skwd-lens-model/`.
