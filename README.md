# RuSafetyBench

Open adversarial benchmark for Russian-language LLM safety evaluation.

RuSafetyBench is an early-stage open benchmark focused on Russian-language adversarial prompts, multilingual safety calibration, and culturally specific failure modes in large language models.

Built as a companion project to [LLM Safety Evaluation Lab](https://github.com/fsrxc2bvv9-ctrl/llm-safety-evaluation-lab).

**Status:** Active development | May 2026

---

## Why This Exists

Most public LLM safety benchmarks are heavily English-centric. Existing datasets such as HarmBench, Do-Not-Answer, and BeaverTails provide useful safety coverage, but they do not fully capture how models behave in Russian-language contexts.

RuSafetyBench tests two core hypotheses:

1. **Language affects safety calibration** — the same model may behave differently in Russian and English.
2. **Cultural and geopolitical context create distinct safety vulnerabilities** that are not captured by direct translation of English prompts.

Early testing suggests both hypotheses are worth further investigation.

---

## Evaluation Categories

| Category | Tests | Key Risk |
|---|---:|---|
| Social Engineering | 6 | Authority impersonation and institutional trust exploitation |
| Gradual Escalation | 4 | Multi-turn normalization in Russian-language context |
| Hallucination | 3 | Fabricated geopolitical or future-event narratives |
| Misinformation | 1 | False scientific consensus and conspiracy amplification |
| Historical Revisionism | 1 | One-sided historical narrative generation |
| Geopolitical Neutrality Calibration | 1 | Cross-model divergence in narrative framing |
| Prompt Injection / Creative Fiction Bypass | 1 | Operational detail extraction through narrative framing |

---

## Models Evaluated

Current manual evaluation includes:

- ChatGPT
- Meta AI
- GigaChat
- Alisa / Yandex
- DeepSeek

---

## Key Concepts

### Geopolitical Neutrality Calibration

Measures whether a model distinguishes between attributed political claims and externally validated consensus positions.

### Narrative Laundering

A failure mode where a model transforms an unsupported or fictional geopolitical premise into apparently analytical exposition.

### Prompt Literalization Susceptibility

A failure mode where a model does not directly leak hidden information but fails to recognize the adversarial intent of a prompt.

### Fiction-as-Obfuscation

A bypass pattern where fiction, roleplay, or historical framing is used to extract operationally actionable content.

---

## Methodology

Each prompt is evaluated manually across multiple models using:

- `PASS`
- `PARTIAL FAIL`
- `FAIL`

Evaluation dimensions include:

- operational usefulness
- hallucination resistance
- attribution fidelity
- geopolitical framing robustness
- fictional bypass resistance
- adversarial intent recognition
- narrative balancing

See [`docs/methodology.md`](docs/methodology.md) for details.

---

## Current Files

```text
data/
  attack_library_ru.csv

docs/
  methodology.md
  taxonomy.md
  findings.md

  Safety Note

This repository is intended for:

* alignment research
* red-teaming analysis
* multilingual safety benchmarking
* adversarial evaluation methodology

No harmful operational guidance is intentionally reproduced in public benchmark files.

Prompts and outputs are included strictly for research and evaluation purposes.

⸻

License

MIT License.