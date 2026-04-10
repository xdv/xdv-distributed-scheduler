# XDV Distributed Scheduler Tests

Deterministic tests and fixtures for `xdv-distributed-scheduler`.

## Covered Behaviors

- global logical-time merge and deterministic placement
- deterministic conflict resolution and decision recording
- remote allocation contract signing/order semantics
- single-node and multi-node failure recovery

## Entrypoints

- `src/scheduler_tests.ds`
- `tests/scheduler_failure_recovery_e2e.ds`

## Run

```bash
dust check xdv-distributed-scheduler/src
dust check xdv-distributed-scheduler/tests/scheduler_failure_recovery_e2e.ds
```
