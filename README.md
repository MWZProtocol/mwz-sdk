# mwz-sdk

**PUBLIC REPOSITORY**

Public developer SDK and integration contract for MWZProtocol DEX and Warzone Markets.

This repository is the intentionally public boundary between MWZProtocol and:

- MemeWarzone Launchpad
- external projects and integrations
- wallet integrations
- aggregators and routing partners
- future integration partners

## What's Here

This repository is intended to expose only approved public integration material, including:

- public API clients and types
- market-data interfaces
- trading quote and execution interfaces
- transaction builders intended for external users
- approved public ABI and IDL artifacts
- public event type definitions
- examples and integration guides
- TypeScript/JavaScript SDK packages

## What's NOT Here

This repository must not contain:

- private backend implementation
- route-signing keys or signer material
- internal abuse/safety thresholds
- private security scoring
- database implementation
- privileged/admin endpoints
- infrastructure secrets or credentials
- private operational configuration

## Public / Private Boundary

```text
PRIVATE IMPLEMENTATION
mwz-dex / mwz-protocol-core / mwz-infrastructure / mwz-docs
        ↓
approved versioned public contract
        ↓
mwz-sdk + public APIs + approved ABI/IDL/events
        ↓
MemeWarzone Launchpad / external integrations
```

External consumers must not import directly from private MWZProtocol repositories. They consume only the public SDK, documented APIs, approved ABI/IDL artifacts, and documented events.

## Getting Started

See [Getting Started](./getting-started/) for the current integration status and examples.

## Package Namespace

Reserved namespace: `@mwzprotocol/*`

Planned package layout:

- `@mwzprotocol/core` — shared public types and utilities
- `@mwzprotocol/markets` — market-data client
- `@mwzprotocol/trading` — quote and execution interfaces
- `@mwzprotocol/evm` — approved EVM integration helpers
- `@mwzprotocol/solana` — approved Solana integration helpers
- `@mwzprotocol/react` — optional React bindings

These package names describe the intended public surface. Do not assume a package is published until a tagged release and registry publication are explicitly available.

## Versioning

**PRE-RELEASE:** interfaces may change until the first stable `v1.0.0` release.

Public artifacts must be versioned deliberately. Private repository changes do not automatically become public SDK changes.

See [Versioning](./versioning/) for stability rules as they are finalized.

## Security

Never report vulnerabilities through public issue content if they could expose users or infrastructure. Follow [SECURITY.md](./SECURITY.md).

## License

MIT License. See [LICENSE](./LICENSE).
