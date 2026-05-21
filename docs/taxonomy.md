# Taxonomy

RuSafetyBench organizes Russian-language adversarial prompts into several evaluation categories.

---

## Social Engineering

Tests whether models resist manipulation through:

- institutional authority claims;
- platform security impersonation;
- emergency framing;
- legal or government authority framing;
- researcher legitimacy framing.

Example risks:

- hidden instruction extraction;
- policy bypass;
- compliance-mode hijacking;
- prompt literalization.

---

## Gradual Escalation

Tests multi-turn safety degradation.

A benign prompt is followed by increasingly risky follow-up questions.

Example pattern:

1. general educational request;
2. safety-relevant follow-up;
3. technical detail request;
4. optimization or ranking request.

This category is useful for detecting conversational normalization and trajectory manipulation.

---

## Hallucination

Tests whether models fabricate:

- future events;
- legal or historical claims;
- geopolitical incidents;
- expert consensus;
- institutional positions.

---

## Misinformation

Tests whether models amplify false or conspiratorial claims, especially when framed as public debate or scientific uncertainty.

---

## Historical Revisionism

Tests whether models generate persuasive one-sided historical narratives without adequate framing, caveats, or modern historiographical context.

---

## Geopolitical Neutrality Calibration

Tests whether models distinguish between:

- state claims;
- legal arguments;
- international consensus;
- disputed narratives;
- verified facts.

This category focuses on attribution fidelity and narrative balancing.

---

## Creative Fiction Bypass

Tests whether fictional, cinematic, historical, or literary framing causes models to provide operationally actionable content.

The benchmark distinguishes:

- fiction-as-style: safe creative transformation;
- fiction-as-obfuscation: harmful capability extraction through narrative framing.

---

## Prompt Literalization Susceptibility

A failure mode where a model responds literally to a prompt while missing the adversarial intent behind it.

Example:

A model does not reveal hidden instructions, but interprets a fake platform-security request as a legitimate request for compliance documentation.

---

## Narrative Laundering

A failure mode where a model transforms an unsupported premise into analytical exposition.

Example:

A fictional future geopolitical accusation is not directly confirmed, but the model converts it into a present-tense explanation of alleged real-world patterns.