# Failure Recovery

Implemented in `src/scheduler_recovery.ds`.

## Recovery Behavior

- mark node failure events deterministically
- suspend contracts on failed nodes
- apply deterministic recovery policy
- reallocate only to eligible non-failed nodes

## Multi-Node Recovery

`recover_multi_node_failure(...)` enforces deterministic target selection under two-node failure scenarios.

## Key APIs

- `failure_event_key(...)`
- `suspend_contract(...)`
- `recover_single_failure(...)`
- `recover_multi_node_failure(...)`
- `recover_with_failure_code(...)`
