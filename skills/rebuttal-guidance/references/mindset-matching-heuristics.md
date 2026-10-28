# Reviewer Mindset Matching Heuristics

Score each signal in the review text (1 = low, 5 = high), then match the profile against the mindset clusters.

## Behavioral signal scoring table

| Signal | Typical high (5) wording | Typical low (1) wording |
|--------|-------------------------|------------------------|
| **Openness** | "willing to raise", "if addressed", "open to" | "reject", "not convincing", "final decision" |
| **Severity** | "fundamental flaw", "fatal issue", "strong reject" | "minor concern", "small issue" |
| **Constructiveness** | "I suggest", "would strengthen if", "recommend adding" | Pure rejection with no path to improvement |
| **Specificity** | References to Table 2, Sec. 3, or equation numbers | "overall not convincing", without specific pointers |
| **Skepticism** | "not convinced", "insufficient evidence", "doubtful" | Neutral wording with no expressed doubt |
| **Harshness** | "reject", "misleading", "wrong", "unacceptable" | Polite, tactful wording |
| **Actionability** | "add experiment", "compare to X", "ablation needed" | No actionable suggestions |

## Six mindset profiles at a glance (current data-driven six-cluster version)

| Mindset | Typical signal combination | Reference score-increase rate | Core response strategy |
|---------|----------------------------|-------------------------------|------------------------|
| **Precise Constructive** | High constructiveness + high specificity + high actionability | ~36% | Structured point-by-point responses with specific manuscript pointers |
| **Mild Skeptic** | Low severity + low actionability, vague wording | ~19% | Resolve confusion directly, with confidence and without overexplaining |
| **Experiment-Oriented** | Frequent evidence_gap concerns and repeated requests for comparisons | See mindset-library | Add experiments or explain why existing results suffice |
| **Highly Skeptical and Severe** | High skepticism + high severity + low score | ~7-15% | Hard evidence first; narrow claims and acknowledge limitations |
| **Harsh with Multiple Concerns** | High harshness + many concerns + a long review | ~12% | New experiments + direct manuscript references + explicit commitments |
| **Other** | No clear match | - | Identify the single most prominent signal first |

See [mindset-library.md](mindset-library.md) for detailed statistics (score-increase rates and Cohen's d effects).

## Matching procedure

1. Score 5–7 signals and record the exact phrases that justify each score.
2. Compare the signal combination with the table above and choose the closest mindset.
3. If two mindsets are close, label them **primary + secondary**.
4. Confidence: at least three aligned signals → **high**; a very short or generic review → **low**.

## How confidence affects the output

| Confidence | Action |
|------------|--------|
| High | Use the mindset's success_patterns directly to guide the strategy |
| Medium | List primary + secondary and explain the strategy differences |
| Low | Use general strategies and state that the mindset judgment is uncertain |
