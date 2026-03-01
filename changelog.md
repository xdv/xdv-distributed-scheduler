# Changelog

## 0.1.1 - XDV-041 Core Implementation

- Implemented XDV-041 contracts in `src/scheduler_contracts.ds`.
- Implemented global logical-time merge and deterministic placement in `src/scheduler_gol.ds`.
- Implemented deterministic conflict resolution in `src/scheduler_dce.ds`.
- Implemented RDAP contract/signature/order paths in `src/scheduler_rdap.ds`.
- Implemented deterministic node-failure recovery in `src/scheduler_recovery.ds`.
- Added XDV-041 behavior tests in `src/scheduler_tests.ds`.
- Added aggregate recovery test entrypoint `tests/scheduler_failure_recovery_e2e.ds`.
- Updated project README and docs to reflect active implementation status.

## 0.1.0 - Initial Skeleton

- Created project scaffold for XDV Distributed Scheduler.
- Added State.toml, README.md, and docs/test placeholders.
- Imported LICENSE from xdv-os/LICENSE.
