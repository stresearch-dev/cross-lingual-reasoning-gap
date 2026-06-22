# Cross-Lingual Reasoning Gap

Measuring how large language model reasoning accuracy changes when grade-school math problems (GSM8K) are translated from English into Indic languages — Hindi, Sanskrit, and Tamil — and whether chain-of-thought prompting helps equally across them.

## Status
🟡 Pilot in progress

## Research question
Do LLMs reason as well in Indic languages as in English on the same problems? Does the gap scale with how low-resource the language is? Does chain-of-thought close or widen it?

## Languages
English (baseline) · Hindi (high-resource) · Tamil (mid) · Sanskrit (low-resource)

## Models evaluated
Gemini Flash · Llama (via Groq) · Sarvam-1 — all via free tiers

## Method
- Benchmark: GSM8K test set
- Translation: IndicTrans2 + manual verification (Hindi, Sanskrit by author)
- Conditions: direct answer vs chain-of-thought
- Metric: exact-match on final numeric answer

## Repository structure
- `data/` — original and translated problem sets
- `src/` — translation and inference pipelines
- `results/` — accuracy tables and analysis
- `notebooks/` — experiments (also published on Kaggle)

## Reproducibility
All code and translated data are open. See `LICENSE`.

## Author
Shubham Tibrewal · [ORCID](https://orcid.org/0009-0002-7453-2897)
