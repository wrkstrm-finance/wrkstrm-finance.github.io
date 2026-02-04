# swift-public-brokerage-lib

Swift-native client + models for the **Public.com brokerage API**.

This package provides a minimal async client, typed request/response models, and optional adapters
that map Public.com concepts into the neutral `CommonBroker` service surfaces.

## Swift Package

- Package: `swift-public-brokerage-lib`
- Products / modules:
  - `PublicBrokerageLib`
  - `PublicBrokerageCommonAdapters`
  - Executable: `public-lib-mark`
- Platforms: iOS 17, macOS 15, tvOS 16, watchOS 9

### Notable features

- OAuth refresh-token flow with automatic access token refresh
- Typed models for accounts, instruments, quotes, and orders
- Polling-based quote streaming via `AsyncStream` (Public does not provide a websocket feed)
- Optional `CommonBroker` adapter target

## Configuration

The library expects standard OAuth/env configuration (see the package README), typically:

- `PUBLIC_REFRESH_TOKEN`
- `PUBLIC_CLIENT_ID`
- `PUBLIC_CLIENT_SECRET`
- `PUBLIC_ACCOUNT_ID`

## Conventions

- Use explicit `CodingKeys` mappings (no implicit snake_case conversions).
