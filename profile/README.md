<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/velyrlabs/velyr/main/.github/assets/brand/banner-dark.png">
    <img src="https://raw.githubusercontent.com/velyrlabs/velyr/main/.github/assets/brand/banner-light.png" alt="Velyr: the security-first JavaScript and TypeScript runtime, written in Rust" width="100%">
  </picture>
</p>

# Velyr Labs

Velyr Labs builds [Velyr](https://github.com/velyrlabs/velyr), a JavaScript and
TypeScript runtime written in Rust, with a deny-by-default permission model.

## Status

Velyr is in **alpha** (`v0.1.0-alpha.1`). APIs and the CLI may change, Node.js
compatibility is partial and experimental, and performance work is ongoing. It
is not ready for production use.

## Principles

- **Secure by default.** Programs get no filesystem, network or environment
  access unless it is granted explicitly.
- **Web standards first.** `fetch`, streams, Web Crypto and friends come before
  Node.js-specific APIs.
- **Name the trade-off.** Node.js compatibility is an optional layer, and it
  costs something. Use it when you need it, not by default.
- **Rust host.** The runtime around the JavaScript engine is written in Rust.
  V8 is the default engine, and a native Rust engine is in progress.

## Try it

Download a binary from the
[releases page](https://github.com/velyrlabs/velyr/releases) (checksums, SBOM
and provenance attestations are published with each release), or build from
source:

```sh
cargo build --release -p velyr-cli
./target/release/velyr run hello.ts
```

## Built on

V8, Tokio and Oxc, checked against test262 and the Web Platform Tests (WPT).
We do not publish a number without its benchmark, machine and commit.

## License

MIT OR Apache-2.0
