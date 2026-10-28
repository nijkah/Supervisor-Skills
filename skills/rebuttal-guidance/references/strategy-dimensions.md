# Rebuttal Strategy Dimensions (Y Vector)

Ten strategy dimensions distilled from historical successful/unsuccessful rebuttals, scored on a 1–5 scale.
**overpromise_risk** and **vague_future_work** are risk dimensions (higher scores mean greater risk).

## The ten dimensions

| Dimension | Meaning | Writing guidance |
|-----------|---------|------------------|
| **direct_address** | Address the core concern directly | Give each W/Q its own heading; do not merge them |
| **specific_evidence** | Use numbers, figures, tables, and comparisons | Do not claim "significantly improve" without numbers |
| **new_experiment_strength** | New experiments precisely address the concern | Explain how the new experiment relates to the main conclusion |
| **clarification_quality** | Clear explanation of misunderstandings, grounded in the manuscript | 2–4 sentences + a Section/Table pointer |
| **controlled_concession** | Acknowledge valid limitations without conceding too much | Follow acknowledgment immediately with the corresponding improvement or narrowed scope |
| **structure_quality** | Clear W/Q structure that reviewers can follow | Subheadings and numbered lists |
| **tone_confidence** | Confident, respectful, non-defensive tone | Avoid defensive wording such as "you misunderstood" |
| **paper_grounding** | Anchor claims to specific locations in the paper/appendix | Do not introduce claims absent from the manuscript |
| **overpromise_risk** ↓ | Make deliverable commitments without overpromising | Avoid unrealistic wording such as "fully solve" |
| **vague_future_work** ↓ | Answer now when possible instead of deferring to future work | Deferral to future work signals evasion |

## Mindset-specific priorities

Once a mindset is matched, read its cluster in `mindset-library.md`:

1. **rule_diff Top 3**: the three dimensions with the largest differences between successful and unsuccessful groups (positive = higher in the successful group).
2. **Cohen's d effects**: d > 0.8 indicates strong discrimination for that mindset.
3. **success_patterns / failure_patterns**: concrete strategy descriptions distilled by an LLM.

Principle: strengthen dimensions with positive differences; use caution with negative differences (higher values in the unsuccessful group may signal overcompensation).

## Effective strategy combinations (interactions)

The data analysis identified synergy in these combinations, with higher success rates when both dimensions score highly:

- `direct_address` + `specific_evidence`: direct response + concrete evidence, the core combination.
- `specific_evidence` + `paper_grounding`: evidence anchored to the manuscript provides the strongest credibility.
- `new_experiment_strength` + `specific_evidence`: new experiments need concrete numbers.
- `tone_confidence` + low `overpromise_risk`: confidence without exaggeration.

## Per-concern strategy annotation

```
R1.W2 → Prioritize: specific_evidence, paper_grounding, clarification_quality
         Avoid: high overpromise_risk, vague_future_work
```
