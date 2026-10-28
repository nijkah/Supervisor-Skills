# Response Templates

Three basic templates for different concern types. **This skill produces a guidance plan, not final rebuttal prose.**

---

## Suggested overall structure

```
[Optional: 2-3 opening sentences with thanks + a summary of revisions]

**R1.W1** [Title]
...

**R1.W2** [Title]
...

**R1.Q1** [Title]
...
```

---

## Template A: Clarify a misunderstanding (misunderstanding / writing_clarity)

```
**R?.W?** [Restate the reviewer's concern in one sentence]

Thank you for the comment. This concern may stem from [specific point of misinterpretation].

**Clarification.** [2–4 sentences with a pointer to Sec. X / Table Y / Appendix Z.]

**Evidence.** [One specific fact or number from the manuscript.]

[If revised] We have added clarification in Sec. X (marked in blue in the revision).
```

**Applicable mindset**: reviewers with high constructiveness respond well to clear clarification.
**Avoid**: explanations longer than four sentences; no pointer to a specific manuscript location.

---

## Template B: Add evidence (evidence_gap / baseline_fairness / efficiency)

```
**R?.W?** [Restate the concern]

We agree that addressing [specific gap] would further strengthen the paper.

**New results.** We have added [experiment/analysis]:
- [Metric] on [dataset]: our method X vs. baseline Y
- See Table N / Appendix M

**Conclusion.** [One sentence explaining how this addresses the concern.]
```

**Applicable mindset**: Experiment-Oriented reviewers and Harsh reviewers with Multiple Concerns respond most positively to new experiments (substantial Cohen's d effects).
**Avoid**: promises of experiments that cannot be completed during rebuttal; numbers that do not come from actual results.

---

## Template C: Acknowledge limitations and narrow scope (scope_claim / novelty / theory)

```
**R?.W?** [Restate the concern]

We acknowledge [specific limitation]. This paper's contribution is bounded to [narrowed scope].

**The contribution still holds.** [1–2 sentences explaining its validity within the narrowed scope.]

**Improvements.** [Revisions/additional analyses completed or planned.]
```

**Applicable mindset**: for Highly Skeptical and Severe reviewers raising scope_claim concerns, narrowing the claim is more effective than arguing.
**Avoid**: conceding without explaining why the contribution remains valuable within the bounded scope.

---

## Guidance block produced by this skill

The agent produces a per-concern guidance plan, not final prose:

```
### R1.W2: [Short concern title]
- **Concern type**: evidence_gap
- **Recommended template**: B
- **Acknowledgment**: Agree that ImageNet evaluation would strengthen the paper
- **Response angle**: Add high-resolution results (do not fabricate numbers)
- **Citable evidence**: CIFAR results in manuscript Table 2; new table (to be added)
- **Tone guidance**: Neutral and confident; avoid defensive wording
- **Avoid**: Long clarification paragraphs with no new numbers
```
