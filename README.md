Field-Constrained Gradient-Based Prompt Injection Against LLM-Based Security Alert Triage

This repository contains the complete implementation and evaluation scripts for the MSc dissertation "Field-Constrained Gradient-Based Prompt Injection Against LLM-Based Security Alert Triage", submitted in partial fulfilment of the degree of MSc in Cyber Security Engineering, WMG, University of Warwick.

Overview

This project adapts Greedy Coordinate Gradient (GCG), originally designed to construct an adversarial suffix appended to a freely composed query, to a mid-prompt, field-constrained injection vector representative of the access a real SOC attacker actually has: control over a single field within a pre-written alert template, rather than the ability to compose a query directly.

Six open-weight language models were benchmarked against this adapted attack, evaluated within a simulated organisation governed by an explicit written SOC triage playbook, across 50 scenarios each built on a genuinely high-severity underlying security event. Two candidate defences, perplexity-based input filtering and system prompt hardening, were subsequently evaluated against the confirmed successful attacks.




Clone the repository and install dependencies:

git clone https://github.com/SahilPatil266/field-constrained-gcg-soc-triage.git  
cd field-constrained-gcg-soc-triage  
pip install -r requirements.txt  

Note: GPU access (CUDA-compatible) is required to run the GCG optimisation notebooks.

Ethics:

This project was conducted under an ethics approval waiver granted by WMG, University of Warwick. All experiments were conducted against a fictional, synthetic organisation and synthetic data; no real individuals, organisations, or production systems were targeted or affected. See the dissertation's Appendix B for the ethics waiver confirmation.
