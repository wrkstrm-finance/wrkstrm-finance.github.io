# swift-tradier-lib

Swift package wrapping the [Tradier Brokerage API](https://documentation.tradier.com/brokerage-api).

TradierLib provides account/trading/market-data models and client-side utilities used across Wrkstrm
apps, plus adapters that map Tradier types into `CommonBroker`.

## Swift Package

- Package: `swift-tradier-lib`
- Products / modules:
  - `TradierLib`
  - `TradierBrokerageCommonAdapters`
  - `TradierLibManagedObjects`
  - Executable: `tradier-json-perf-cli`
- Platforms: iOS 17, macOS 15, macCatalyst 17, tvOS 16, watchOS 9

## Utilities

### tradier-json-perf-cli

Benchmarks decoding throughput using canonical Tradier payload fixtures.

Build/run:

```bash
swift build --product tradier-json-perf-cli
swift run tradier-json-perf-cli --dir <payload-dir>
```

## Conventions

- Use explicit `CodingKeys` mappings (no implicit snake_case conversions).
