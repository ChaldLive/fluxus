# 🌊 Fluxus Familia

Welcome to **Fluxus**, a modular, service-oriented architecture built in Rust with clarity, composability, and purpose. Fluxus is more than a system—it's a living, breathing _familia_ of services that flow together to orchestrate complex tasks with elegance and precision.

## ✨ Philosophy

Fluxus is designed around a few core principles:

- **Flow over friction**: Services communicate seamlessly via well-defined contracts.
- **Modularity with meaning**: Each subservice (aka _Fluxling_) has a clear role and autonomy.
- **Delegation with dignity**: The central orchestrator (_Fluxus Core_) delegates tasks intelligently, not blindly.
- **Extensibility by design**: New capabilities can be added without disrupting existing flow.
- **Observability and introspection**: Every part of the system can be monitored, queried, and understood.

## 🧩 Architecture Overview

Fluxus is composed of several key components:

| Component        | Description                                                                 |
| ---------------- | --------------------------------------------------------------------------- |
| `fluxus-core`    | The brain of the system. Handles delegation, routing, and orchestration.    |
| `fluxling-*`     | Modular subservices. Each handles a specific domain (e.g. claims, recipes). |
| `fluxus-api`     | Public-facing API layer. Exposes endpoints for external clients.            |
| `fluxus-schema`  | Shared types and contracts. Ensures consistency across the familia.         |
| `fluxus-cli`     | Command-line interface for devs and operators.                              |
| `fluxus-observe` | Monitoring, logging, and introspection tools.                               |

## 🧠 Core Concepts

- **Claims**: Assertions or requests made by users or services. Evaluated and routed by `fluxus-core`.
- **Recipes**: Declarative task blueprints. Define how a claim should be fulfilled.
- **Delegation**: The act of assigning a claim to the most appropriate fluxling.
- **Introspection**: Ability to query the system about its current state, decisions, and history.

## 🛠️ Tech Stack

- **Rust**: For performance, safety, and fearless concurrency.
- **gRPC / HTTP**: For inter-service communication.
- **PostgreSQL**: For persistent state and metadata.
- **Prometheus + Grafana**: For metrics and observability.
- **Docker / Nix**: For reproducible builds and deployments.

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/fluxus-familia/fluxus.git
cd fluxus

# Build the core
cargo build --workspace

# Run the orchestrator
cargo run -p fluxus-core
```
