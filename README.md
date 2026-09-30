# Clinical-Decision-Benchmark
The benchmark tests whether a model can move beyond simple association findings and reach the expert conclusion that inflammatory markers but are not yet validated as standalone clinical screening or diagnostic markers for osteoporosis because most evidence is observational, heterogeneous, and non-causal.
# Description

A benchmark designed to test whether a model can go beyond simplistic association-based reasoning and arrive at an evidence-based clinical conclusion.

This project focuses on a clinically meaningful decision question: whether inflammatory parameters, such as the Systemic Immune-Inflammation Index (SII), should currently be used as clinical markers for osteoporosis.

The benchmark tests whether a model can:
- read and reason over multiple research articles
- distinguish association from causation
- assess the quality and limitations of evidence
- weigh conflicting findings and confounding factors
- produce a clinically defensible recommendation

The key objective is not to identify a single “statistically significant” association, but to determine whether the evidence is strong enough to support real clinical use.

## Why this benchmark matters

Inflammatory blood markers such as SII, neutrophil-to-lymphocyte ratio (NLR), platelet-to-lymphocyte ratio (PLR), and dietary inflammatory index (DII) are often reported as associated with reduced bone mineral density and osteoporosis risk. However, many such findings come from observational studies with substantial confounding, cross-sectional designs, and inconsistent subgroup effects.

This benchmark evaluates whether a model can recognize that:
- inflammatory markers may be biologically relevant
- some studies suggest an association with bone loss
- the evidence is not yet strong enough to justify routine standalone clinical use
- DXA and validated fracture-risk tools remain the accepted clinical standards

## Benchmark question

Should inflammatory parameters, such as SII, currently be used as clinical markers for osteoporosis?

A strong answer should discuss:
- supporting evidence
- contradictory findings
- study limitations
- confounding and selection bias
- whether the relationship is causal or correlational
- whether inflammatory markers are useful:
  - as standalone markers
  - as adjunctive markers
  - or as research tools only

## Repository contents

- `CDB.ipynb` — notebook implementing the benchmark workflow using the Gemini API
- `pdf_folder/` — directory containing the source scientific articles used as evidence
- `README.md` — project overview and usage guide
- `.env` — environment file containing your API key (not committed in shared repos)

## Setup

This project uses the Google GenAI Python SDK and `python-dotenv`.

### 1) Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
