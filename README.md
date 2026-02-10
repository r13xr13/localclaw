# LocalClaw — Local-First Intelligence Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Docker Pulls](https://img.shields.io/docker/pulls/yourusername/localclaw.svg?logo=docker)](https://hub.docker.com/r/yourusername/localclaw)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)

**Release Date:** 3/1/26  
**Runtime:** Docker, Python 3.10+

LocalClaw is a **local-first intelligence platform** designed for security professionals and privacy-conscious users who want full control over their tools, data, and execution environment.

It runs on your machine, uses local models by default, and integrates online capabilities in a way that remains inspectable, controllable, and user-owned.

---

## What Is LocalClaw?

LocalClaw is a self-hosted AI-driven system for analysis, research, automation, and knowledge management.

It is built to:
- Replace cloud-dependent AI and analysis tools
- Centralize workflows into a single local platform
- Provide powerful online capabilities without surrendering control
- Operate transparently, with no hidden services or telemetry

LocalClaw is not a SaaS replacement.  
It is an **operator-owned system**.

---

## Who Is LocalClaw For?

### Security and Technical Professionals
LocalClaw is designed with professionals in mind:

- Analysts
- Engineers
- Researchers
- Security practitioners
- Power users who want full visibility and control

It assumes comfort with containers, configuration, and local tooling.

---

### Privacy-First Daily Users
LocalClaw is equally usable by daily users who care about privacy:

- Writers and researchers
- Developers and students
- Anyone who does not want personal data leaving their machine
- Users who want modern AI tools without surveillance

The same architecture that supports professional workflows also protects everyday use.

---

## Design Principles

LocalClaw is built on a small number of non-negotiable principles:

- Local-first execution
- User-owned data and memory
- Transparent service boundaries
- No hidden network activity
- Online access that is visible and controllable
- Defaults that are powerful, not neutered

Privacy comes from **architecture**, not feature removal.

---

## Default Capabilities

LocalClaw ships with the following **enabled by default**:

### Local AI Engine
- Quantized local language models
- llama.cpp-compatible backends
- User-controlled model selection

### Online Research (SearXNG)
- Integrated SearXNG for web search
- Aggregated sources with reduced tracking
- Queries and results visible and auditable
- No third-party cloud AI services

### Editor Integration (Zed)
- Zed editor integration for writing and coding
- Local AI assistance via LocalClaw
- Online research and enrichment available inline
- No external brokers or relays

### Container Management (Portainer)
- Portainer included for visibility and control
- Inspect containers, volumes, and logs
- Start, stop, or isolate services as needed
- No opaque background processes

### Automation and Tooling
- Workflow orchestration
- Task execution with guardrails
- Clear confirmation for impactful actions

---

## Interfaces

### Graphical Interface (GUI)
- Runs locally on the host
- Not exposed externally
- Central place for workflows, history, and configuration

### Terminal Interface (TUI)
- Full-featured command-line interface
- Scriptable and automation-friendly
- Designed for daily professional use

### Editor Interface
- Tight integration with Zed
- AI-assisted writing and development
- Local-first with optional online enrichment

---

## Architecture Overview (Conceptual)

LocalClaw is composed of:

- A local AI inference service
- A coordination and memory layer
- Online research services (self-hosted)
- Tool execution services
- User interfaces (GUI, TUI, editor)
- Container management and observability

Each component is isolated, inspectable, and replaceable.

---

## Installation

### Requirements
- Docker and Docker Compose
- Python 3.10+ (for development)
- Approximately 10–15 GB disk space

---

### Homebrew (macOS and Linux)

```bash
brew install localclaw

