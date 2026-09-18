# Hi, I'm Sergi 👋

**AI Engineer — evaluation-first agents & RAG · Web3 Security Researcher · Industrial Engineer (Electrical & Automation)**

I build **real LLM systems**: tool-calling agents and RAG pipelines over specialized
domains, plus the evaluation tooling to measure them independently — measurable
quality, not vibes. I'm also a **Web3 smart-contract security researcher** (Solidity
auditing, top-3 in a public DeFi audit). And I bring an **industrial engineering
background** — Electrical & Automation, with PLC/SCADA commissioning on a real
production line (Mercedes-Benz) — so the systems I build are grounded in plant-floor
reality: robustness, cost control and honest validation.

Everything I publish is local-first (local LLMs, no paid APIs), CI-verified and reproducible.

Based in Vitoria-Gasteiz, Spain.

## The portfolio trilogy

One coherent story, three independent repos: build agents, build verifiable RAG systems, and guarantee their quality from the outside.

### 1. [alpha-agent](https://github.com/eLSeR17/alpha-agent) — the agent

[![CI](https://github.com/eLSeR17/alpha-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/alpha-agent/actions/workflows/ci.yml)

A tool-calling agent for investment queries: real function calling, guardrails and evals
built in.

### 2. [smart-contract-rag](https://github.com/eLSeR17/smart-contract-rag) — the context

[![CI](https://github.com/eLSeR17/smart-contract-rag/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/smart-contract-rag/actions/workflows/ci.yml)

A production RAG system over real smart contract audits, with its own eval pipeline —
golden dataset, LLM-as-judge and a regression guard. Includes a documented experiment
on semantic grounding.
**Live demo**: [ask the audit corpus](https://smart-contract-rag-3wnnafjfnjku54baybdec2.streamlit.app/) — grounded, cited answers over 10 real Trail of Bits reports, deployed on Streamlit Community Cloud.

### 3. [evalforge](https://github.com/eLSeR17/evalforge) — the QA layer

[![CI](https://github.com/eLSeR17/evalforge/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/evalforge/actions/workflows/ci.yml)

The evaluation layer: audits the two projects above as black-box subjects, using golden
datasets, a dual judge (deterministic + LLM-as-judge) and a regression guard with
semantic exit codes. Live evaluation reports are part of the repo.

> The three form a V: `evalforge` audits the other two from the outside — there is no
> hidden dependency between `alpha-agent` and `smart-contract-rag`.


### 4. [quantum-rag](https://github.com/eLSeR17/quantum-rag) — RAG over 240+ quantum computing papers, with measurable quality

[![CI](https://github.com/eLSeR17/quantum-rag/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/quantum-rag/actions/workflows/ci.yml)

Retrieval-augmented generation over 240+ arXiv papers (quantum error correction & quantum
machine learning), with hybrid BM25 + dense retrieval and evidence-first answers whose
grounding is verified (never claimed without supporting chunks). Evaluated with its own
12-case golden set: recall@8 **1.000**, MRR 0.674, faithfulness 0.62. Runs on CPU only,
no paid APIs, and ships a CI gate with 4 jobs (tests on 3.11 + 3.12, lint, and a security
job that audits every dependency and scans for leaked secrets).

**Live demo**: [ask the quantum literature corpus](https://quantum-rag.streamlit.app/) —
240+ arXiv papers, grounded and cited answers, deployed on Streamlit Community Cloud.

## Web3 security — smart-contract auditing

Solidity security auditing with **proven results in public contests and paid audits**:

- 🥉 **3rd place** — **Boost Core Incentive Protocol** — public Sherlock audit
  (DeFi): permissionless growth-engine risk, economic-attacker modeling and flow
  analysis
- 💰 **$2K prize** — **Chainlink Payment Abstraction** — audit of the
  payment-abstraction component at the core of Chainlink's billing system
- Independent researcher, 2024 — present

The auditor mindset transfers directly to AI systems: threat modeling, economic
flow analysis and validating findings against real code are the same disciplines
behind my evaluation-driven agent pipeline —
[architecture writeups here](https://github.com/eLSeR17/ai-agent-systems-portfolio).

## Applied AI — industry bridge

> Industrial engineer (Electrical & Automation) with hands-on commissioning on the
> Mercedes-Benz (Vitoria) production line — Siemens Step7, TIA Portal, WinCC — and
> 4 years of engineering at Daisalux (emergency lighting). The projects below apply
> plant-floor discipline (robustness, process safety, silent-failure prevention)
> to modern AI stacks.

### 5. [pdm-agent](https://github.com/eLSeR17/pdm-agent) — predictive maintenance with anti-hallucination

[![CI](https://github.com/eLSeR17/pdm-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/pdm-agent/actions/workflows/ci.yml)

ML + LLM pipeline on NASA C-MAPSS and UCI Steel Plates: RandomForest baselines, then a
local LLM agent that interprets work orders and validates its own hypotheses with an
anti-hallucination layer. Honest metrics, reproducible, no SOTA claims.

### 6. [plc-ai-agent](https://github.com/eLSeR17/plc-ai-agent) — AI for PLC diagnostics & SCL code generation

[![CI](https://github.com/eLSeR17/plc-ai-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/plc-ai-agent/actions/workflows/ci.yml)

An OPC UA + MCP + local-LLM agent that reads a real S7-1500 (or a bundled simulator)
and drafts IEC 61131-3 SCL code through deterministic templates. The LLM picks the
template and parameters — it never writes code freely; a validator and a human review
gate stand between the agent and the controller. 100% local, no cloud, no API keys.

### 7. [pcb-ai-agent](https://github.com/eLSeR17/pcb-ai-agent) — AI for KiCad PCB design & firmware generation

[![CI](https://github.com/eLSeR17/pcb-ai-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/pcb-ai-agent/actions/workflows/ci.yml)

A fully local agent for KiCad designs: it parses netlists and schematics, audits
boards with evidence-grounded rules (every finding cites the exact ref — no LLM
guesses) and cross-checks netlist vs schematic so parts cannot silently diverge.
It also generates STM32 HAL / Arduino init firmware from deterministic templates,
compiled against 100%-own HAL stubs with real gcc/g++ in CI — generated code is
proven to compile before any human review. 493 tests, CI green (3.11, 3.12,
security + compile gate). 100% local, no cloud, no API keys.

Also see: [python-industrial-portfolio](https://github.com/eLSeR17/python-industrial-portfolio)
— 8 industrial Python projects (QA, vibration, fatigue, process control).

## Computer vision & optimization

### 8. [sudoku-vision-solver](https://github.com/eLSeR17/sudoku-vision-solver) — solve a Sudoku from a single photo

[![CI](https://github.com/eLSeR17/sudoku-vision-solver/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/sudoku-vision-solver/actions/workflows/ci.yml)

Take a photo of an unsolved Sudoku and get the same photo back with the solution
overlaid in green. OpenCV grid detection with homography warp, an MNIST-trained MLP
(784→256→10) for digit recognition, and a pure-Python optimal solver (bitmasks +
MRV + forward checking, no dependencies). A consistency-repair pass re-reads
misread digits under rotation — verified on a rotated photo of Arto Inkala's
"world's hardest Sudoku", returning the exact published solution. 62 tests,
CI green (3.11, 3.12, security).

## Stack

Python · Docker · pytest · GitHub Actions · local LLMs (Ollama) · RAG (ChromaDB, hybrid retrieval) ·
evals (LLM-as-judge, regression guard) · MCP · tool calling · observability · computer vision (OpenCV) · ML (scikit-learn) · EDA (KiCad) · firmware (gcc/g++ stubs)

## Contact

- [LinkedIn](https://www.linkedin.com/in/sergio-l%C3%B3pez-52669a184/)

---

Every claim in these repos is reproducible: tests, evals and CI are part of the repos.