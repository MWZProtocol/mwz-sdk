# mwz-sdk

**PUBLIC REPOSITORY**

Public developer SDK for integrating with MWZProtocol DEX and Warzone Markets.

This is the official public contract between MWZProtocol and:
- MemeWarzone Launchpad
- External projects and integrations
- Wallet integrations
- Aggregators and routing partners
- Future integration partners

## What's Here

✅ Public API clients and types
✅ Market data interfaces
✅ Trading quote generation
✅ Transaction builders for external users
✅ Public ABI and IDL artifacts
✅ Event type definitions
✅ Examples and integration guides
✅ TypeScript/JavaScript SDK packages

## What's NOT Here

❌ Private backend implementation
❌ Internal route signing keys
❌ Internal abuse/safety rules
❌ Private security scoring
❌ Database implementation
❌ Admin endpoints
❌ Secrets or credentials

## Public/Private Boundary

```
PRIVATE IMPLEMENTATION (mwz-dex, mwz-protocol-core, mwz-infrastructure)
        ↓
MWZProtocol services/protocol
        ↓
PUBLIC VERSIONED CONTRACT (mwz-sdk)
        ↓
External integrations/consumers
```

External consumers must NOT import directly from:
- mwz-dex
- mwz-protocol-core
- mwz-infrastructure
- mwz-docs

They consume only:
- mwz-sdk packages
- Public APIs
- Public ABI/IDL artifacts
- Documented events

## Getting Started

See [Getting Started Guide](./getting-started/) for integration examples.

## Package Namespace

Official namespace: `@mwzprotocol/*`

Published packages include:
- `@mwzprotocol/core` - Core types and utilities
- `@mwzprotocol/markets` - Market data client
- `@mwzprotocol/trading` - Trading quote and execution
- `@mwzprotocol/evm` - EVM contract interactions
- `@mwzprotocol/solana` - Solana program interactions
- `@mwzprotocol/react` - React hooks and components

## API Status

⚠️ **PRE-RELEASE**: Interfaces and APIs may change until v1.0.0 is released.

See [Versioning](./versioning/) for stability guarantees.

## License

MIT
