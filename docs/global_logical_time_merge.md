# Global Logical-Time Merge

Implemented in `src/scheduler_gol.ds`.

## Deterministic Merge Function

`L_global = f(L_node, Node_ID)` is represented by a stable key model:

- `global_time_key(local_logical_time, node_id)`
- `global_time_merge_pair(...)`
- `global_time_merge_three(...)`
- `global_logical_time_reconcile(cluster_epoch, local_logical_time, node_id)`

The merge rules are deterministic and wall-clock independent.
