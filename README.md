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

### 3. [evalforge](https://github.com/eLSeR17/evalforge) — the QA layer

[![CI](https://github.com/eLSeR17/evalforge/actions/workflows/ci.yml/badge.svg)](https://github.com/eLSeR17/evalforge/actions/workflows/ci.yml)

The evaluation layer: audits the two projects above as black-box subjects, using golden
datasets, a dual judge (deterministic + LLM-as-judge) and a regression guard with
semantic exit codes. Live evaluation reports are part of the repo.

> The three form a V: `evalforge` audits the other two from the outside — there is no
> hidden dependency between `alpha-agent` and `smart-contract-rag`.

## Stack

Python · Docker · pytest · GitHub Actions · local LLMs (Ollama)

## Contact

- [LinkedIn](https://www.linkedin.com/in/sergio-l%C3%B3pez-52669a184/)

---

Every claim in these repos is reproducible: tests, evals and CI are part of the repos.