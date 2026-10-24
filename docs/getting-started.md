# Getting started

## What QORE does

QORE combines an editable workspace, constrained Qiskit circuit authoring, local Aer simulation, interactive state visualizations, optimization validation, terminal diagnostics, and an experiment ledger. It is designed for learning, algorithm prototyping, and evidence-based review.

## Run locally

From the QORE repository root:

```powershell
.\.venv\Scripts\python.exe -m uvicorn qore.main:app --host 127.0.0.1 --port 8000
```

Open `http://127.0.0.1:8000`. For frontend hot reload, start Vite separately with `pnpm dev` in `frontend/`.

## First Bell-state experiment

```python
from qiskit import QuantumCircuit

qc = QuantumCircuit(2, 2)
qc.h(0)
qc.cx(0, 1)
qc.measure([0, 1], [0, 1])
```

Run the circuit in Quantum Lab. With an ideal simulator, the measured distribution should contain `00` and `11`, while `01` and `10` remain absent. Use a fixed seed to reproduce sampled counts.

## Core workflow

1. Create a project in Explorer.
2. Write a supported circuit program.
3. Parse and run it through Quantum Lab.
4. Inspect distributions, State World, Bloch views, amplitude and unitary data.
5. Preserve the run in Quantum Ledger.
