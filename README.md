# RisuAI for LazyCat

This repository packages [RisuAI](https://github.com/kwaroran/Risuai) as a LazyCat application. RisuAI is an AI roleplaying chat client with character cards, multiple model providers, lorebooks, plugins, and extensive conversation controls.

For Chinese documentation, see [README.zh-CN.md](README.zh-CN.md).

## Usage

Open RisuAI from the LazyCat launcher, then configure a model provider and its API credentials in RisuAI settings. Provider availability, account requirements, and API charges are determined by the selected model service.

RisuAI may store model API keys in its application data. Keep access to the LazyCat application restricted to trusted users and devices.

## Persistence

The upstream `/app/save` directory is stored under `/lzcapp/var/save`. Conversations, character cards, settings, and other RisuAI data survive application restarts and upgrades. Back up the LazyCat application data before reinstalling or making major upgrades.

## Image Delivery

The initial package uses `ghcr.1ms.run/kwaroran/risuai:v2026.6.214` for accelerated image access. GitHub Actions discovers releases from `ghcr.io/kwaroran/risuai`, requires the `linux/amd64` source and mirror digests to match, builds a versioned LPK, and publishes it only to the private MiaoMiao store.

## Links

- [RisuAI source](https://github.com/kwaroran/Risuai)
- [RisuAI website](https://risuai.net)
- [LazyCat packaging repository](https://github.com/lazycat-contrib/risuai-lzcapp)
