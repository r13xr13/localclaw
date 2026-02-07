# Sigil7 (formerly HELIX Intelligence) Dropping soon 

**Sovereign Cyber Intelligence Platform**  
Local AI-powered threat intelligence and red/blue team automation — fully offline, OPSEC-hardened, containerized.

**Built for operators who demand control, precision, and zero external dependencies.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Docker Pulls](https://img.shields.io/docker/pulls/yourusername/sigil7.svg?logo=docker)](https://hub.docker.com/r/yourusername/sigil7) <!-- update if you publish -->
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)

## Overview

Sigil7 is an autonomous, local-first cyber intelligence engine that unifies Kali Linux tools under an AI-driven operator. It reasons, plans, executes tool chains, persists threat knowledge in graphs, generates YAML playbooks, correlates findings with NVD feeds, and produces code/scripts — all without phoning home.

Key pillars:
- **100% offline / air-gapped capable** after setup
- Quantized local LLMs (llama.cpp + models like MythoMax-L2-13B)
- Full Kali tool integration with safe wrappers & parsing
- Neo4j graph brain for IOCs, assets, relationships, kill-chains
- Persistent memory (JSON/YAML + schema validation)
- YAML-driven playbooks (red team, blue team, OSINT, IR)
- Private web enrichment via self-hosted SearXNG + MCP
- Code generation & editing loop (via Zed editor integration)

Designed for red teams, blue teams, incident responders, and bug hunters who want agentic automation without cloud risks or telemetry.

## Features

- Autonomous OSINT profiling, recon → vuln chaining → report generation
- Behavioral threat profiling & network persona reconstruction
- Simulated offensive actions with evasion-aware payloads
- Live NVD/CVE correlation & attack path suggestion
- Operator-supervised or fully autonomous modes
- Secure tool execution (allow-lists, timeouts, no destructive defaults without confirm)
- Persistent multi-session campaigns that never forget
- Zed editor integration for AI-assisted exploit/script writing

## Architecture

## Installation & Quick Start

### Prerequisites
- Docker & Docker Compose
- NVIDIA GPU (optional, for faster inference)
- ~10–15 GB disk space (image + models)

### Docker (recommended)

```bash
# Clone repo
git clone https://github.com/r13xr13/helix-intelligence.git sigil7
cd sigil7

# (Optional) Download models (Mythomax or Qwen) to ./models/
# Example: wget https://huggingface.co/.../MythoMax-L2-13B.gguf -O models/MythoMax.gguf

# Start (adjust docker-compose.yml for your paths/ports)
docker compose up -d

# Enter the main container
docker exec -it sigil7 bash   # or zsh

Inside the container:
# Run Sigil7 engine (adjust to your launcher)
python engine.py --mode supervised --target example.com
# or your custom entrypoint: ./sigil7.sh --model MythoMax.gguf

Dev Container (Zed / VS Code)
•  Open the project folder in Zed or VS Code
•  Accept the “Reopen in Container” prompt (uses .devcontainer/devcontainer.json)
•  Zed Agent Panel connects to local llama.cpp + MCP-SearXNG
Current Status
This is an early release / work-in-progress. Core engine, tool wrappers, graph integration, and local LLM inference are functional. Full autonomy and advanced playbooks are still being hardened.
Security note: Tools run in isolated subprocesses with strict allow-lists. Always use authorized targets only. No internet required after initial model/download setup.
Roadmap (2026)
•  Full LangGraph orchestration with reflection loops
•  More curated Kali tool wrappers (top 50+)
•  Encrypted sensitive memory sections
•  Better Zed/ACP integration for live code-gen
•  Community-contributed safe playbooks
•  Optional darknet/OSINT modules (Tor bridge)
Contributing
Contributions welcome — especially:
•  Safe tool wrappers
•  Playbook YAML examples
•  Bug fixes / hardening
Please open issues/PRs with clear descriptions. Security-related reports → private contact (see SECURITY.md if exists).
License
MIT License — see LICENSE file.
Ethical use only: This tool is for authorized security testing and research. Misuse violates laws and is not condoned.

“Observe. Profile. Execute. Secure.”
— Sigil7 Directive
Questions? Reach out on Mastodon: @r13@infosec.exchange

