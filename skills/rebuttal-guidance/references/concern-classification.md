# Concern Classification

Classify each Weakness / Question before choosing a response strategy.

## Classification table

| Type | Signals in the reviewer's wording | Priority strategy dimensions | Recommended template |
|------|----------------------------------|------------------------------|----------------------|
| **misunderstanding** | "seems", "unclear whether", or a clear contradiction with the manuscript | clarification_quality + paper_grounding | Template A |
| **evidence_gap** | "more experiments", "ablation", "only one dataset" | new_experiment_strength + specific_evidence | Template B |
| **novelty** | "incremental", "similar to X", "limited contribution" | specific_evidence + explicit differentiation; controlled_concession when needed | A or C |
| **baseline_fairness** | "unfair comparison", "weak baseline", "missing SOTA" | Additional comparisons + explanation of the experimental protocol | Template B |
| **scope_claim** | "overclaim", "overstated", "not supported by evidence" | controlled_concession to narrow the claim | Template C |
| **writing_clarity** | "hard to follow", "notation", "organization" | Revised wording + examples + manuscript pointers | Template A |
| **theory** | "proof", "assumption", "bound", "convergence" | Equation/proof pointers or acknowledgment of limitations | A or C |
| **efficiency** | "complexity", "scalability", "overhead" | Complexity analysis + measured latency | Template B |
| **other** | No clear match above | Restate the concern, then reclassify | Depends on content |

## Handling Weaknesses vs. Questions

| | Weakness | Question |
|--|----------|----------|
| Reviewer mindset | "There is a flaw here" | "I did not understand / please confirm" |
| Response focus | Evidence + revisions when needed | Brief answer + Section/Table pointer |
| Common mistake | Explanation without action | Excessive apology |

## Quick keyword classification

```
novelty:     novel, contribution, incremental, original, marginal
experiments: experiment, baseline, ablation, dataset, evaluation
writing:     clarity, unclear, confusing, notation, presentation
theory:      proof, theorem, assumption, bound, convergence
efficiency:  scalable, complexity, computation, overhead, efficient
scope:       limitation, generalize, broader, overclaim, overstated
```

## Compound concerns

If one Weakness combines novelty + evidence_gap, split it into two sub-concerns and give each its own strategy.
Prioritize **the concern that matters most to the reviewer** (usually in the first paragraph).
