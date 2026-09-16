# Hi, I'm Sergi 👋

**AI Engineer — I build agents and RAG systems with an evaluation-first mindset · Web3 Security Researcher**

I build real LLM systems: tool-calling agents and RAG pipelines over specialized domains,
plus the evaluation tooling to measure them independently. Everything I publish is
local-first (local LLMs, no paid APIs), CI-verified and reproducible.

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

## Applied AI — industry bridge

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

Also see: [python-industrial-portfolio](https://github.com/eLSeR17/python-industrial-portfolio)
— 8 industrial Python projects (QA, vibration, fatigue, process control).

## Stack

Python · Docker · pytest · GitHub Actions · local LLMs (Ollama) · RAG (ChromaDB, hybrid retrieval) ·
evals (LLM-as-judge, regression guard) · MCP · tool calling · observability

## Contact

- [LinkedIn](https://www.linkedin.com/in/sergio-l%C3%B3pez-52669a184/)

---

Every claim in these repos is reproducible: tests, evals and CI are part of the repos.