# Architecture

## System flow

`Author → constrained AST parser → QORE IR → isolated worker → Qiskit Aer → evidence model → Lab / Forge / Ledger`

## Backend

`backend/qore/main.py` owns the FastAPI boundary and request guards. `quantum.py` parses a safe circuit-building subset, converts it to QORE IR, runs simulation, calculates metrics, produces QASM, and validates optimization equivalence. `runtime.py` and `worker.py` provide bounded subprocess execution. `store.py` persists projects, runs, and immutable experiments in SQLite.

## Frontend

The React/Vite frontend uses `App.tsx` as the IDE shell. Explorer manages files and projects; Quantum Lab renders output; Forge presents validated transformations; Research presents the Ledger; Terminal exposes diagnostics; State World and Bloch visualizations render state data.

## Data boundaries

The browser receives execution results and user-scoped workspace data. API keys, IBM Quantum credentials, filesystem access, worker controls, and database internals must remain server-side.
