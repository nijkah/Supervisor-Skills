# Rebuttal Guidance Completeness Checklist

Check each item before telling the user the guidance is complete.

## Completeness checks

| # | Check | Pass |
|---|-------|------|
| 1 | Every W/Q in the user's input has a corresponding guidance block | ☐ |
| 2 | Every concern has a type label | ☐ |
| 3 | The matched mindset cluster and confidence are stated | ☐ |
| 4 | Every concern has recommended strategy dimensions | ☐ |
| 5 | No experimental numbers are fabricated (data not verified against the paper are marked [TO VERIFY]) | ☐ |
| 6 | Clarification concerns are clearly distinguished from those requiring new experiments | ☐ |
| 7 | Defensive wording is flagged in the tone guidance | ☐ |
| 8 | Overpromising is flagged for items with high overpromise_risk | ☐ |

## Tone red flags (must be flagged in the guidance)

- "You misunderstood / You missed / This is trivial": aggressive; rewrite.
- "Significantly / clearly / undoubtedly": empty assertions without supporting numbers.
- "We will fully address in future work": signals evasion when no current action is taken.
- Excessive apology ("We sincerely apologize for..."): weakens the argument.

## Special guidance for reviewers with low openness

If the matched mindset has a **historical score-increase rate < 15%** (see mindset-library.md):

- Tell the user that persuasion through wording alone has limited success; prioritize one decisive new experiment.
- Suggest a realistic goal: clarify the central misunderstanding + provide one minimal, credible piece of new evidence.
- Do not encourage an overly long rebuttal: concise, strong responses are preferable to exhaustive coverage.

## Common mistakes

| Failure pattern | Symptom | Correction |
|-----------------|---------|------------|
| Overlong clarification | Five paragraphs explaining an evidence_gap, with no new data | Reduce to two sentences and point to new results |
| Blanket concession | Excessive concessions on scope_claim | Follow the acknowledgment immediately with an argument that the contribution holds within a bounded scope |
| Evading novelty | Answering "not novel enough" with "our method is more practical" | Give specific technical differences from the closest related work |
| Ignoring Questions | Treating a Q as a W and responding with a lengthy proof | A Q usually needs only 2–3 sentences + a pointer |
