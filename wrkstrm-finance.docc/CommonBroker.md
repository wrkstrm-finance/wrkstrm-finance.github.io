# CommonBroker

A universal Swift brokerage package abstracting over multiple broker APIs.

The core idea is to model brokerage features as **small capability-oriented services** (auth, accounts,
quotes, streaming, positions, etc.). Each broker implementation can declare which services it supports,
allowing clients to select brokers interchangeably based on the capabilities they need.

## Swift Package

- Package: `common-broker`
- Product / module: `CommonBroker`
- Platforms: iOS 17, macOS 15, tvOS 17, watchOS 10

### Key dependencies

- `wrkstrm-main` (`WrkstrmMain`)
- `common-log` (`CommonLog`)
- `wrkstrm-foundation` (`WrkstrmFoundation`)
- `wrkstrm-networking` (`WrkstrmNetworking`)

## Capability matrix

See `BrokerServiceMatrix.md` in the package for a per-broker capability listing.

## Design notes

- Prefer explicit `CodingKeys` mappings for snake_case payloads.
- Avoid `.convertFromSnakeCase` / `.convertToSnakeCase` strategies.

(These conventions are important when you need stable encoders/decoders across multiple brokers.)
