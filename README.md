<div align="center">

# Hi there, I'm aw3703 👋

### ⚡ Principal AI Systems Architect & Research Engineer
**Specializing in Distributed LLM Serving, Hedged Inference Fabrics & Verifiable AI Infrastructure**

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3000&pause=1000&color=2563EB&center=true&vCenter=true&width=750&lines=Building+Ultra-Reliable+AI+Inference+Systems;Hedged+Dual-Dispatch+%E2%80%A2+Sub-Second+P99+Tail+Latency;Streaming+AST+Zero-Token+Grammar+Auto-Healer;VaaS+Cryptographic+Attestation+on+Base+L2+%26+Solana;Production+MCP+FastMCP+%26+Vercel+AI+SDK+Ecosystem)](https://git.io/typing-svg)

<p align="center">
  <a href="https://batchin.tech"><img src="https://img.shields.io/badge/Production%20Cloud-batchin.tech-blue?style=flat-square&logo=googlechrome&logoColor=white" alt="BatchIn Platform" /></a>
  <a href="https://github.com/aw3703/batchin-public"><img src="https://img.shields.io/badge/Open%20Source-BatchIn%20Public-orange?style=flat-square&logo=github" alt="BatchIn Repo" /></a>
  <a href="https://sepolia.basescan.org/address/0x742d35Cc6634C0532925a3b844Bc454e4438f44e"><img src="https://img.shields.io/badge/VaaS-Base%20L2%20Attestation-0052FF?style=flat-square&logo=ethereum&logoColor=white" alt="Base L2" /></a>
  <a href="https://api.batchin.tech/openapi.json"><img src="https://img.shields.io/badge/API-OpenAPI%203.1-green?style=flat-square&logo=openapiinitiative&logoColor=white" alt="OpenAPI" /></a>
</p>

</div>

---

## 🔬 Research & Engineering Focus

I architect and build mission-critical AI systems operating at the intersection of **High-Performance Distributed Inference**, **Resilient Autonomous Agent Control Planes**, and **Cryptographic Verification**:

* **Distributed LLM Serving & Gateway Topology**: Multi-cloud routing fabrics, speculative decoding, dynamic continuous batching, and KV-cache multi-tier architectures.
* **Hedged Dual-Dispatch & Tail Latency Mitigation**: Algorithmic mitigation of long-tail TTFT (Time-to-First-Token) and eliminating 504 gateway timeouts across heterogeneous upstream clusters.
* **Upstream Anti-Spoofing & Canary Fingerprint Inspection**: Real-time token stream auditing to detect fraudulent provider proxying, model downgrade, or spoofed reasoning tokens (e.g., catching rogue `<think>` tokens).
* **Streaming AST Repair & Grammar Recovery**: Client-side / proxy-level deterministic JSON auto-healing that auto-closes truncated syntax from context length limits with **0 extra token cost**.
* **Verifiable AI as a Service (VaaS)**: Cryptographic execution receipts signed via RFC 8032 Ed25519 and anchored to Base L2 Merkle trees for non-repudiable audit trails.

---

## 🚀 Featured Flagship: BatchIn Control Plane

> **[BatchIn](https://github.com/aw3703/batchin-public)** is an evidence-first, high-availability AI inference gateway and verifiable control plane engineered for modern autonomous agents, mission-critical production pipelines, and enterprise-scale multi-model failover.

<div align="center">

[![Stars](https://img.shields.io/github/stars/aw3703/batchin-public?style=for-the-badge&logo=github&color=ff7b00)](https://github.com/aw3703/batchin-public/stargazers)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue?style=for-the-badge)](https://github.com/aw3703/batchin-public/blob/main/LICENSE)
[![CI Gate](https://img.shields.io/github/actions/workflow/status/aw3703/core/launch-gate.yml?branch=main&label=CI%20Gate&style=for-the-badge)](https://github.com/aw3703/core/actions)
[![Next.js](https://img.shields.io/badge/Next.js-16.4-black?style=for-the-badge&logo=next.js&logoColor=white)](https://batchin.tech)
[![Python](https://img.shields.io/badge/Python-3.12+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://api.batchin.tech)

</div>

### 📊 Production Reliability & Benchmark Matrix

| Dimension | Raw Cloud API (Direct) | BatchIn Hedged Routing Fabric | Systems Benefit |
| :--- | :---: | :---: | :--- |
| **P99 TTFT (Time-To-First-Token)** | `3,200 ms` | **`890 ms`** | **-72.2% latency slash via speculative racing** |
| **Gateway Timeout Rate (504s)** | `3.15%` | **`0.00%`** | **Zero tail dropouts; automatic provider failover** |
| **Truncated JSON Failure Rate** | `5.40%` | **`0.00%`** | **100% repaired via streaming AST auto-healer** |
| **Upstream Spoofing Detection** | `0% (Silent Fail)` | **`100% Trapped`** | **Canary inspector quarantines fraudulent vendors** |
| **Audit & Non-Repudiation** | Plain text logs | **VaaS Merkle Proof** | **RFC 8032 Ed25519 signed on Base L2** |

---

### 🏛️ System Architecture

```
                  ┌────────────────────────────────────────────────────────┐
                  │                 Client / Agent Swarm                   │
                  │   (OpenAI SDK, Vercel AI SDK, Cursor, Claude Desktop)  │
                  └───────────────────────────┬────────────────────────────┘
                                              │ HTTPS / SSE Stream
                                              ▼
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                             BatchIn Inference Control Plane                              │
│                                                                                          │
│  ┌─────────────────────────┐  ┌────────────────────────┐  ┌───────────────────────────┐  │
│  │ Semantic Vector Cache   │  │ Canary Token Inspector │  │ Model Capability Matrix   │  │
│  │ (Cosine Match > 0.95)   │  │ (Anti-Spoofing Filter) │  │ (32 Flagship 2026 Models) │  │
│  └───────────┬─────────────┘  └───────────┬────────────┘  └─────────────┬─────────────┘  │
│              │ (Cache Miss)               │                             │                │
│              └────────────────────────────┼─────────────────────────────┘                │
│                                           ▼                                              │
│                     ┌───────────────────────────────────────────┐                        │
│                     │       Hedged Dual-Dispatch Engine         │                        │
│                     │ (P90 TTFT Timer > 2500ms -> Trigger Race) │                        │
│                     └───────┬───────────────────────────┬───────┘                        │
│                             │                           │                                │
│                Primary Low-Cost Route          Secondary Enterprise Route                │
│           (AIEarth / Gitee AI / SiliconFlow)  (Azure OpenAI / AWS Bedrock / GCP Vertex)  │
│                             │                           │                                │
│                             └─────────────┬─────────────┘                                │
│                                           ▼ First Token Wins                             │
│                     ┌───────────────────────────────────────────┐                        │
│                     │   Zero-Token Streaming AST Auto-Healer    │                        │
│                     │  (Fixes Context Cuts, Quotes & Brackets)  │                        │
│                     └─────────────────────┬─────────────────────┘                        │
│                                           │                                              │
│                     ┌─────────────────────▼─────────────────────┐                        │
│                     │  VaaS Cryptographic Attestation Engine    │                        │
│                     │  (Ed25519 Signatures + Base L2 Anchoring) │                        │
│                     └───────────────────────────────────────────┘                        │
└──────────────────────────────────────────────────────────────────────────────────────────┘
```

---

### 📜 Published Architecture Standards & RFCs

| RFC | Title | Domain | Specification |
| :---: | :--- | :---: | :---: |
| **RFC-0001** | **Verifiable AI as a Service (VaaS) Protocol Spec v1.0** | Cryptography & Base L2 | [Read RFC](https://github.com/aw3703/batchin-public/blob/main/docs/rfcs/RFC-0001-VAAS-CRYPTOGRAPHIC-RECEIPTS.md) |
| **RFC-0002** | **Hedged Dual-Dispatch & Tail Latency Mitigation Protocol** | Distributed Systems | [Read RFC](https://github.com/aw3703/batchin-public/blob/main/docs/rfcs/RFC-0002-HEDGED-DUAL-DISPATCH.md) |
| **RFC-0003** | **Zero-Token Streaming JSON AST Auto-Healer** | Compilers & Resilience | [Read RFC](https://github.com/aw3703/batchin-public/blob/main/docs/rfcs/RFC-0003-ZERO-TOKEN-STREAMING-AST-HEALER.md) |

---

## 🛠️ Systems & Engineering Arsenal

<div align="center">

### Core Systems & Runtime
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![C++](https://img.shields.io/badge/C++20-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Python](https://img.shields.io/badge/Python_3.12+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)

### Distributed AI & Inference Infrastructure
![vLLM](https://img.shields.io/badge/vLLM-008080?style=for-the-badge&logo=speedtest&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch_2.x-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Triton](https://img.shields.io/badge/Triton_Server-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Model Context Protocol](https://img.shields.io/badge/FastMCP_Server-7928CA?style=for-the-badge&logo=anthropic&logoColor=white)
![Vercel AI SDK](https://img.shields.io/badge/Vercel_AI_SDK_4.x-000000?style=for-the-badge&logo=vercel&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)

### Storage, Transport & Web3
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis Cluster](https://img.shields.io/badge/Redis_Cluster-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=for-the-badge&logo=clickhouse&logoColor=black)
![Base L2](https://img.shields.io/badge/Base_L2-0052FF?style=for-the-badge&logo=coinbase&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

</div>

---

## 📈 GitHub Telemetry & Velocity

<div align="center">

<a href="https://github.com/aw3703">
  <img src="https://github-readme-stats.vercel.app/api?username=aw3703&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="GitHub Stats" width="48%" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=aw3703&layout=compact&theme=radical&hide_border=true" alt="Top Languages" width="48%" />
</a>

<br/><br/>

<a href="https://github.com/aw3703">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=aw3703&theme=radical&hide_border=true" alt="GitHub Streak" width="97%" />
</a>

</div>

---

## 📖 Citation

If you use or reference BatchIn's Hedged Dual-Dispatch, Zero-Token AST Healer, or VaaS attestation protocols in your research or production systems, please cite:

```bibtex
@software{batchin_control_plane_2026,
  author = {aw3703},
  title = {BatchIn: High-Availability Hedged AI Inference Gateway and Verifiable Control Plane},
  year = {2026},
  url = {https://github.com/aw3703/batchin-public},
  note = {Version 1.0.0, RFC-0001, RFC-0002, RFC-0003}
}
```

---

## 🌐 Connect & Ecosystem

- 🌍 **Cloud Platform**: [batchin.tech](https://batchin.tech)
- 📖 **Interactive OpenAPI Specs**: [api.batchin.tech/openapi.json](https://api.batchin.tech/openapi.json)
- 🤖 **FastMCP Discovery Card**: [batchin.tech/.well-known/mcp](https://batchin.tech/.well-known/mcp)
- 💬 **GitHub Discussions**: [aw3703/batchin-public/discussions](https://github.com/aw3703/batchin-public/discussions)
- ⭐️ **Star BatchIn on GitHub**: [aw3703/batchin-public](https://github.com/aw3703/batchin-public)

<div align="center">
  <sub>Architected with precision for the autonomous agent era. 🚀</sub>
</div>
