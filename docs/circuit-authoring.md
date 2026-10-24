# Circuit authoring

## Supported source model

QORE intentionally does not execute arbitrary Python. It accepts a constrained AST subset that builds one `QuantumCircuit`. This protects the workstation while allowing circuit authoring.

Supported constructors are `QuantumCircuit`, `QuantumRegister`, and `ClassicalRegister`. Basic numeric arithmetic, `pi`, literal index lists, and finite `for range(...)` loops are accepted.

Supported circuit methods include the gate set implemented by QORE IR plus `measure`, `measure_all`, and `barrier`. The compiler rejects imports outside the permitted Qiskit circuit constructors, double-underscore names, arbitrary functions, shell access, network access, filesystem access, and circuit method keyword arguments.

## Registers and endianness

Qiskit classical bitstrings use little-endian classical indices: highest index appears on the left. Always inspect QORE’s bitstring convention panel when comparing a circuit diagram with measurement output.

## Qiskit packages

QORE installs Qiskit, Aer, IBM Quantum Runtime client, and selected published research add-ons. Add-ons are available to backend engineering workflows; they do not make arbitrary source safe to execute in the browser.
