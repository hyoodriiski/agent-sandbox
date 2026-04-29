# agent-sandbox

> Fork of [kubernetes-sigs/agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox)

A sandboxed environment for developing, testing, and running AI agents with Kubernetes-native tooling.

## Overview

`agent-sandbox` provides a controlled execution environment for AI agents, enabling safe experimentation and deployment within Kubernetes clusters. It offers:

- **Isolated execution**: Run agents in sandboxed containers with resource limits
- **Kubernetes-native**: Leverages Kubernetes primitives for scheduling and lifecycle management
- **Extensible**: Plugin architecture for custom agent runtimes
- **Observable**: Built-in metrics, logging, and tracing support

## Prerequisites

- Go 1.22+
- Python 3.10+ (for Python SDK)
- Kubernetes 1.28+ cluster (or [kind](https://kind.sigs.k8s.io/) for local development)
- `kubectl` configured with cluster access

## Getting Started

### Installation

```bash
# Clone the repository
git clone https://github.com/your-org/agent-sandbox.git
cd agent-sandbox

# Install Go dependencies
go mod download

# Install Python SDK (optional)
pip install agent-sandbox
```

### Quick Start

```bash
# Build the project
make build

# Run tests
make test

# Deploy to a local kind cluster
make deploy-local
```

## Development

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on contributing to this project.

### Local Development Setup

```bash
# Set up pre-commit hooks
make setup-dev

# Run linters
make lint

# Run unit tests
make test-unit

# Run integration tests (requires cluster)
make test-integration
```

## CI/CD

This project uses GitHub Actions for continuous integration. See `.github/workflows/` for pipeline definitions.

| Workflow | Trigger | Description |
|----------|---------|-------------|
| `ci.yml` | Push / PR | Build and test |
| `check.yml` | Push / PR | Lint and format checks |
| `pypi-publish.yml` | Release | Publish Python SDK to PyPI |

## License

Apache License 2.0 — see [LICENSE](LICENSE) for details.

## Acknowledgements

This project is a fork of [kubernetes-sigs/agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox), maintained by the Kubernetes SIGs community.
