# Security and operations

## Execution policy

Never expose arbitrary Python execution publicly. QORE uses constrained source parsing and bounded backend workers. Public deployment should additionally require authentication, rate limiting, execution timeouts, memory limits, qubit and shot caps, audit logs, and abuse monitoring.

## Credentials

IBM Quantum hardware, Functions, and Quantum System services require authenticated service credentials. Store them only in secure backend environment variables. Never send them to the Vite frontend or commit them to Git.

## Troubleshooting

When reporting an issue, include the circuit source, project path, simulator settings, terminal output, backend name, shots, seed, warning details, and execution metadata. Do not include secrets or tokens.
