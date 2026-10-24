# Simulation and evidence

## Local execution

QORE uses Qiskit Aer for local statevector and shot-based simulation. Choose a shot count for sampled measurement statistics and a seed for deterministic repeatability.

## Lab views

Distribution compares sampled frequency with ideal probability. State World provides an interactive basis-state view. Bloch views visualize single-qubit reduced states. Amplitude, unitary, and QASM views provide mathematical and interoperability evidence.

## Metrics

Total variation distance measures divergence between sampled and ideal distributions; zero is a perfect match. Metadata includes backend, shots, seed, noise model, execution duration, and timestamp.

## Forge

Optimization candidates are accepted only after QORE proves unitary behavior and terminal measurement mapping remain equivalent within tolerance. This makes transformations reviewable rather than cosmetic.

## Ledger

The Ledger stores source fingerprints, configuration, output, warnings, framework versions, and historical snapshots. Export JSON when an experiment needs external review.
