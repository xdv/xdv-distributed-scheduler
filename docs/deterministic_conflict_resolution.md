# Deterministic Conflict Resolution

Implemented in `src/scheduler_dce.ds`.

## Resolution Order

For conflicting requests, DCE applies stable ordering:

1. policy priority weight
2. logical-time precedence
3. node-id tie-break
4. request-id tie-break

This ensures identical outcomes under replay.

## Key APIs

- `resolve_two_request_conflict(...)`
- `resolve_and_record(...)`
- `request_order_key(...)`
