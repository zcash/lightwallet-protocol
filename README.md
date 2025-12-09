# Light Wallet Protocol Canonical files

This repository contains the canonical Protobuf definitions for the Zcash Light Wallet protocol.

## Rationale
Before the creation of this repository, copies of wallet RPCs `.proto` files would exist in several
repositories across the Zcash ecosystem. This posed a challenge for protocol developers,
wallet maintainers and infrastructure providers who would have to look up for the _Ad Hoc_
canonical files for their own use and changes would be hard to propagate and communicate.

This repository IS NOT a specification of the Zcash Light Client protocol. The Zcash Light Client
Protocol is described in [ZIP-307](https://zips.z.cash/zip-0307).

These files are the Protocol Buffers used in that ZIP using [proto 3](https://protobuf.dev/programming-guides/proto3/).

## How to use these files

We recommend using `git subtree` of the `main` branch  or tagged versions of this repository.

```git subtree -p lightwallet-protocol/ pull git@github.com:zcash/lightwallet-protocol.git main --squash```


### Example: YourProject
We assume YourProject is a git repository

````
$ cd YourProject

$ git subtree -p lightwallet-protocol/ pull git@github.com:zcash/lightwallet-protocol.git main --squash

$ tree .

├── lightwallet-protocol
│   ├── LICENSE
│   └── walletrpc
│       ├── compact_formats.proto
│       └── service.proto
... (other directories)
````

## Current  implementations
### Servers
- [Lightwalletd (Go Lang)](https://github.com/zcash/lightwalletd/) 
- [Zaino (RustLang)](https://github.com/zingolabs/zaino)
### Clients
- Zashi [[iOS](https://github.com/Electric-Coin-Company/zcash-swift-wallet-sdk/) | [Android](https://github.com/Electric-Coin-Company/zcash-android-wallet-sdk/)]
- [Zingo Lib CLI](https://github.com/zingolabs/zingolib/)
- [Zcash dev-tool](https://github.com/zcash/zcash-devtool) 
- [Ywallet](https://github.com/hhanh00/zwallet)


## Discussing and developing the Zcash Light Client Protocol

Light client protocol development is steered by the [Light Client Working Group](https://github.com/zcash/lcwg).

This workgroup meets bi-weekly and its invite-only but you can reach out through the [this channel](https://discord.com/channels/809218587167293450/809250822579028008)
of the Zcash R&D Discord server.

