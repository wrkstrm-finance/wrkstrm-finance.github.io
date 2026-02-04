# Libraries

Wrkstrm Finance is currently composed of a few focused Swift packages that all orbit the same idea:
**normalize broker-specific APIs into small, testable service surfaces**.

## Packages

- <doc:CommonBroker>
- <doc:SwiftPublicBrokerageLib>
- <doc:SwiftTradierLib>

## Local development (mono)

Most finance packages support a `SPM_USE_LOCAL_DEPS` flag:

- If `SPM_USE_LOCAL_DEPS=1|true|yes` is set, dependencies resolve to **local mono paths**.
- Otherwise, dependencies resolve to **remote Git URLs** (when available).

This makes it easy to work in the mono tree without constantly publishing interim versions.
