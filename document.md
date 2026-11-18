# Document-side contract: cell execution state

The REST endpoint only requests execution.
Its results are delivered by the server writing to the cell in the shared (CRDT) document, and clients see them through normal document synchronization.

## Fields written by the server

For each executed code cell the server writes:

- `execution_state`: whether the cell is running.
- `execution_count`: from the kernel.
- `outputs`: nbformat outputs built from IOPub messages.
