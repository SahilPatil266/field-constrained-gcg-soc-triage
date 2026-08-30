Field-Constrained Gradient-Based Prompt Injection Against LLM-Based Security Alert Triage

This repository contains the complete implementation and evaluation scripts for the MSc dissertation "Field-Constrained Gradient-Based Prompt Injection Against LLM-Based Security Alert Triage", submitted in partial fulfilment of the degree of MSc in Cyber Security Engineering, WMG, University of Warwick.

Overview

This project adapts Greedy Coordinate Gradient (GCG), originally designed to construct an adversarial suffix appended to a freely composed query, to a mid-prompt, field-constrained injection vector representative of the access a real SOC attacker actually has: control over a single field within a pre-written alert template, rather than the ability to compose a query directly.

Six open-weight language models were benchmarked against this adapted attack, evaluated within a simulated organisation (Meridian Finch Ltd) governed by an explicit written SOC triage playbook, across 50 scenarios each built on a genuinely high-severity underlying security event. Two candidate defences, perplexity-based input filtering and system prompt hardening, were subsequently evaluated against the confirmed successful attacks.

Repository Structure
├── environment/        # SOC playbook, synthetic employee database, alert template logic
├── scenarios/           # Full 50-scenario dataset
├── models/               # Testing notebooks for all six evaluated models
└── defence_evaluation/  # Perplexity filtering and system prompt hardening evaluation scripts
Models Evaluated
Model	Parameters	Domain-specialised
Qwen2.5-1.5B-Instruct	1.5B	No
Qwen2.5-7B-Instruct	7B	No
Phi-3-mini-4k-instruct	3.8B	No
Mistral-7B-Instruct-v0.3	7B	No
Lily-Cybersecurity-7B-v0.2	7.24B	Yes
Foundation-Sec-8B-Instruct	8B	Yes
Setup
bash
git clone https://github.com/SahilPatil266/field-constrained-gcg-soc-triage.git
cd field-constrained-gcg-soc-triage
pip install -r requirements.txt

GPU access (CUDA-compatible) is required to run the GCG optimisation notebooks. Experiments in the dissertation were run on [insert your actual compute environment, e.g. Google Colab Pro, T4/A100 GPU].

Ethics

This project was conducted under an ethics approval waiver granted by WMG, University of Warwick. All experiments were conducted against a fictional, synthetic organisation and synthetic data; no real individuals, organisations, or production systems were targeted or affected. See the dissertation's Appendix B for the ethics waiver confirmation.
