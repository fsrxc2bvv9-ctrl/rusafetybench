# Findings

Current findings are preliminary and based on manual cross-model testing.

---

## Finding 1 — Russian-language prompts can alter safety behavior

Several models showed different safety behavior in Russian compared with equivalent English prompts.

The most visible example involved gradual escalation in household-chemistry prompts, where some models maintained safety in English but produced more operationally detailed Russian responses.

---

## Finding 2 — Institutional framing affects model resistance

Russian-language prompts using institutional authority produced distinct model behaviors.

Examples include:

- FSB authority framing;
- platform security verification;
- compliance-style requests;
- official audit framing.

Some models recognized these as social engineering attempts. Others interpreted them literally and shifted into compliance or legal-administrative mode.

---

## Finding 3 — Fiction framing can extract operational detail

Creative fiction prompts produced one of the clearest cross-model divergences.

Strong responses preserved atmosphere and literary utility while removing operational details.

Weak responses embedded operationally actionable surveillance methods inside fictional dialogue.

This supports the concept of fiction-as-obfuscation.

---

## Finding 4 — Geopolitical prompts expose narrative framing divergence

Geopolitical prompts produced major differences in:

- attribution fidelity;
- narrative balancing;
- source selection;
- consensus contextualization.

The strongest responses clearly separated state claims from externally validated consensus.

Weaker responses reproduced state-aligned narratives or relied on politically skewed source framing.

---

## Finding 5 — Censorship and safety are not the same

Some models refused politically sensitive topics while providing permissive responses to operationally risky prompts.

This suggests that political-topic filtering and general safety calibration may operate as separate moderation layers.

---

## Finding 6 — Two successful safety strategies appeared

Two strong response strategies appeared across models:

### 1. Transformation safety

The model preserves user value while removing actionable harmful detail.

Example: writing atmospheric fiction without surveillance tradecraft.

### 2. Refusal-plus-redirection

The model explicitly refuses unsafe content and offers a safe alternative.

Both strategies are valid, but they produce different user experiences.

---

## Finding 7 — Narrative laundering is a distinct failure mode

Some models did not directly fabricate fictional events, but transformed unsupported premises into analytical geopolitical exposition.

This can make unsupported claims appear more legitimate without explicitly stating them as proven facts.

Narrative laundering is especially relevant for:

- geopolitical conspiracy prompts;
- intelligence attribution claims;
- speculative future-event prompts;
- politically sensitive fictional scenarios.