# QORE Documentation

This repository publishes the official, searchable documentation website for QORE — a bounded quantum development environment for authoring, simulation, visualization, compiler review, and reproducible evidence.

## Official documentation map

- [Start here](https://qoredocs.vercel.app/guides-getting-started.html)
- [Studio and Explorer](https://qoredocs.vercel.app/features-studio.html)
- [Quantum Lab](https://qoredocs.vercel.app/features-quantum-lab.html)
- [Forge](https://qoredocs.vercel.app/features-forge.html)
- [Research Ledger](https://qoredocs.vercel.app/features-research-ledger.html)
- [QI Assistant](https://qoredocs.vercel.app/features-assistant.html)
- [API and architecture](https://qoredocs.vercel.app/reference-api.html)
- [Quantum foundations](https://qoredocs.vercel.app/quantum-foundations.html)
- [Deployment and security](https://qoredocs.vercel.app/operations-deployment.html)

## Scope

QORE is a local-first, evidence-driven quantum IDE. It parses a constrained circuit-building subset into QORE-IR, simulates it with Qiskit Aer, visualizes state and measurement evidence, evaluates compiler candidates, and archives reproducible experiment snapshots.

The generated website contains 38 dedicated pages grouped into start guides, workspace features, technical reference, operations, and quantum concepts. Source Markdown is retained under `content/`; HTML, search data, navigation, responsive styling, and diagrams are generated from the main QORE repository.

QORE currently uses an account-free browser workspace. The documentation clearly distinguishes browser persistence, SQLite evidence, anonymous workspace isolation, and the limits of that model.
