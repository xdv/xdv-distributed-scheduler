# Placement Model

Implemented in `src/scheduler_gol.ds`.

## Inputs

- domain requirements
- capability scope
- policy weight
- node-local capacities (K/Q/Phi)
- local logical-time and node identity

## Deterministic Tie-Breaking

When scores are equal, lower `Node_ID` is selected.

## Key APIs

- `placement_score(...)`
- `place_process_two_nodes(...)`
