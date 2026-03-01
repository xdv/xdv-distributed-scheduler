# XDV Distributed Scheduler

Version: 0.1.0
Status: active
Language: Dust Programming Language (DPL)

## Specification Alignment

Primary specification: XDV-041 in `xdv-spec`.

Implemented focus for this milestone:

1. Global logical-time merge and placement.
2. Deterministic conflict resolution.
3. Multi-node failure recovery tests.

## Modules

- `src/scheduler_contracts.ds`
  Normative constants and validation for domain/capability/policy/node constraints.

- `src/scheduler_gol.ds`
  Global Orchestration Layer (GOL): logical-time merge and deterministic placement.

- `src/scheduler_dce.ds`
  Deterministic Coordination Engine (DCE): canonical conflict arbitration and decision tokening.

- `src/scheduler_rdap.ds`
  Remote Domain Allocation Protocol (RDAP): contract packing, signature marker, ordering key.

- `src/scheduler_recovery.ds`
  Deterministic node-failure recovery and reallocation policies.

- `src/scheduler_tests.ds`
  Scheduler behavior tests for XDV-041 requirements.

- `src/main.ds`
  Bootstrap/startup validation and smoke entrypoints.

## Build

```bash
dust check xdv-distributed-scheduler/src
```

## Test

```bash
dust check xdv-distributed-scheduler/src/scheduler_tests.ds
dust check xdv-distributed-scheduler/tests/scheduler_failure_recovery_e2e.ds
```

## Notes

- Logical-time merge is deterministic and Node_ID-stable.
- Placement decisions are replay-stable with deterministic tie-break rules.
- Conflict resolution is canonicalized and reproducible.
- Failure recovery remains deterministic under single-node and multi-node failures.
