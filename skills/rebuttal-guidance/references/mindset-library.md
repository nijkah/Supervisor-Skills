# Reviewer Mindset Library (Skill Snapshot)

## Table of Contents

- [Cluster 3: Precise Constructive](#cluster-3-precise-constructive)
- [Cluster 4: Mild Skeptic](#cluster-4-mild-skeptic)
- [Cluster 0: Authoritative Negativist](#cluster-0-authoritative-negativist)
- [Cluster 5: Harsh Dismissive](#cluster-5-harsh-dismissive)
- [Cluster 1: Gentle Constructive](#cluster-1-gentle-constructive)
- [Cluster 2: Concise Affirmative](#cluster-2-concise-affirmative)

> Auto-generated from `data/behavior/mindset_library.json`.

Model method: `behavior_space_kmeans_llm`, with six mindset clusters.

---

## Cluster 3: Precise Constructive

**Profile**: These reviewers focus on feasibility and concrete details. They offer clear, actionable suggestions and cite specific literature or methods. Their criticism is moderately severe but highly constructive, and they are relatively open to persuasion. Their main aim is to help the authors improve the paper rather than dismiss the work.

| Metric | Value |
|------|-----|
| Sample share | 9.5% (95 reviews) |
| Historical score-increase rate | 36.1% |
| Acceptance rate | 43.2% |
| Successful rebuttal samples | 44 |

### Identifying signals

- Identify missing details such as parameter sizes, equation forms, or implementation steps.
- Cite specific literature or methods to identify contradictions with prior work or shortcomings.
- Request explicit changes, such as "please clarify" or "provide the specific form".

### Rule-statistic differences (Top 3)

- **Explicit revision commitments**: Success 65.9% vs. failure 81.8% (Δ -15.9)
- **Direct quotation / point-by-point correspondence**: Success 77.3% vs. failure 66.7% (Δ +10.6)
- **New experiments / new results**: Success 61.4% vs. failure 51.5% (Δ +9.9)

### Strategy vector effects (Cohen's d)

**Substantially higher in the successful group (Cohen's d):**
- `structure_quality`: Successful mean 4.614 / Unsuccessful mean 3.157 (d=1.107)
- `paper_grounding`: Successful mean 4.386 / Unsuccessful mean 2.98 (d=1.074)
- `clarification_quality`: Successful mean 4.636 / Unsuccessful mean 3.235 (d=1.07)

**Higher in the unsuccessful group (risk dimensions):**
- `vague_future_work`: Successful mean 1.386 / Unsuccessful mean 2.333 (d=-0.727)
- `overpromise_risk`: Successful mean 1.295 / Unsuccessful mean 1.745 (d=-0.432)

### Success patterns (LLM-derived)

- **Structured, direct responses**: Number or title the response to each weakness, quote the review, and provide concrete explanations or evidence instead of general discussion.
- **Concrete evidence and manuscript grounding**: Support arguments with new experiments, figures, tables, or quantitative results, and cite specific manuscript locations to strengthen credibility.
- **Confident, restrained tone**: Respond positively and confidently while remaining constructive. Avoid defensiveness and overpromising, and specify completed improvements when acknowledging limitations.
- **Controlled concessions and commitments**: Acknowledge limitations while clearly describing completed improvements or future directions; avoid vague "future work" statements and excessive promises.

### Failure patterns (LLM-derived)

- **Vague future-work promises**: Phrases such as "future work" or "we plan" without concrete action or evidence make responses seem inadequate or evasive.
- **Overpromising or generalities**: Promising many improvements without a specific plan or evidence, or answering only with broad statements, seems unrealistic or untrustworthy.
- **Long, unstructured explanations**: Lengthy responses that do not directly quote the reviewer's specific concerns make key information hard to locate and reduce persuasiveness.
- **Overexplaining or evading the central issue**: Long theoretical explanations of technical concerns, without new evidence or a direct acknowledgment of limitations, leave reviewers unconvinced.

### Key strategy

Structured, direct responses + concrete evidence + a confident, restrained tone.

---

## Cluster 4: Mild Skeptic

**Profile**: These reviewers are mild in tone and not sharply critical, but offer few specific or constructive suggestions. They express confusion or point out apparent omissions rather than analyze issues deeply or propose actionable improvements. Their stance may be neutral or slightly negative; reluctance to reject harshly leads to moderate scores and vague concerns.

| Metric | Value |
|------|-----|
| Sample share | 20.5% (205 reviews) |
| Historical score-increase rate | 18.7% |
| Acceptance rate | 47.3% |
| Successful rebuttal samples | 99 |

### Identifying signals

- Open with vague doubts such as "I am confused" or "If I'm understanding correctly".
- Identify problems without specific revision suggestions or alternatives.
- Write brief comments with little in-depth technical analysis of methods or results.

### Rule-statistic differences (Top 3)

- **Moderate acknowledgment**: Success 54.5% vs. failure 66.2% (Δ -11.7)
- **Clarification**: Success 53.5% vs. failure 64.6% (Δ -11.1)
- **Explicit revision commitments**: Success 59.6% vs. failure 49.2% (Δ +10.4)

### Strategy vector effects (Cohen's d)

**Substantially higher in the successful group (Cohen's d):**
- `tone_confidence`: Successful mean 4.535 / Unsuccessful mean 3.0 (d=1.246)
- `direct_address`: Successful mean 4.515 / Unsuccessful mean 3.048 (d=1.116)
- `clarification_quality`: Successful mean 4.404 / Unsuccessful mean 2.943 (d=1.148)

**Higher in the unsuccessful group (risk dimensions):**
- `vague_future_work`: Successful mean 1.616 / Unsuccessful mean 2.543 (d=-0.687)
- `overpromise_risk`: Successful mean 1.404 / Unsuccessful mean 2.219 (d=-0.685)

### Success patterns (LLM-derived)

- **Confident, direct responses**: Address concerns confidently, without ambiguity or excessive apology, and demonstrate command of the work.
- **High-quality clarification and manuscript grounding**: Give clear, specific explanations supported by the manuscript, figures, tables, appendices, or concrete experimental evidence; avoid empty explanations.
- **Controlled concessions and concrete evidence**: Balance acknowledgment of limitations immediately with specific evidence, such as new data, analysis, or a manageable improvement plan. Avoid empty promises and excessive concessions.

### Failure patterns (LLM-derived)

- **Excessive concessions and vague future work**: Repeatedly acknowledging shortcomings without concrete improvements, or offering vague future-work promises, suggests low confidence and little substantive action.
- **Long, unfocused explanations**: Spending too much space clarifying misunderstandings or adding background instead of addressing the issue leads to lengthy, off-topic responses that slow the reviewer down.
- **Excessive clarification without manuscript grounding**: Extensive explanations without specific manuscript references, such as tables or appendices, feel unsupported and fail to persuade.

### Key strategy

Respond directly and confidently, anchor the response in manuscript evidence, make controlled concessions, and avoid vague promises.

---

## Cluster 0: Authoritative Negativist

**Profile**: These reviewers are confident and demanding, often pointing out weaknesses from a position of authority and citing specific literature or technical details to support negative judgments. Their style is direct and concise, often using lists or short sentences. They focus on flaws and limitations and are not very receptive to the authors' defenses.

| Metric | Value |
|------|-----|
| Sample share | 20.4% (204 reviews) |
| Historical score-increase rate | 14.7% |
| Acceptance rate | 27.9% |
| Successful rebuttal samples | 62 |

### Identifying signals

- List criticisms in short sentences or bullets, such as "Unclear text encoder".
- Cite literature or technical details to dismiss the contribution, such as "has been studied in [1]".
- State directly that claims are too strong or unsupported, such as "claims are too strong".

### Rule-statistic differences (Top 3)

- **Explicit revision commitments**: Success 51.6% vs. failure 66.2% (Δ -14.6)
- **Direct quotation / point-by-point correspondence**: Success 72.6% vs. failure 58.8% (Δ +13.8)
- **New experiments / new results**: Success 46.8% vs. failure 40.0% (Δ +6.8)

### Strategy vector effects (Cohen's d)

**Substantially higher in the successful group (Cohen's d):**
- `clarification_quality`: Successful mean 4.419 / Unsuccessful mean 2.794 (d=1.198)
- `direct_address`: Successful mean 4.613 / Unsuccessful mean 3.0 (d=1.112)
- `tone_confidence`: Successful mean 4.452 / Unsuccessful mean 2.858 (d=1.177)

**Higher in the unsuccessful group (risk dimensions):**
- `vague_future_work`: Successful mean 1.419 / Unsuccessful mean 2.603 (d=-0.801)
- `overpromise_risk`: Successful mean 1.323 / Unsuccessful mean 2.333 (d=-0.767)

### Success patterns (LLM-derived)

- **Confident, direct responses**: Address specific concerns head-on with a confident, direct tone; avoid evasion and vague wording.
- **High-quality clarification and manuscript grounding**: Give clear, substantive explanations anchored in manuscript text, theoretical foundations, or additional experiments, demonstrating a deep understanding of the work.
- **Controlled concessions and concrete evidence**: Acknowledge valid concerns or limitations while supporting the core contribution with experimental data, theoretical analysis, or new evidence; avoid empty promises.

### Failure patterns (LLM-derived)

- **Vague future work or overpromising**: Answering criticism with "we will address this in future work" or exaggerated promises, without immediate evidence or a specific plan, appears to evade the main issue.
- **Dismissive or defensive responses**: Downplaying specific criticism or making excuses such as "the bug does not affect the results" or "we are not pursuing SOTA", without serious treatment and detailed explanation, intensifies distrust.
- **Weak novelty defense**: Asserting that the method is different without concrete comparisons or evidence fails to rebut concerns about insufficient novelty.

### Key strategy

Respond directly and confidently, support the response with manuscript grounding and concrete evidence, and avoid vague promises.

---

## Cluster 5: Harsh Dismissive

**Profile**: These reviewers use a harsh, dismissive tone, with strong criticism but little constructiveness. They rarely offer actionable improvements and are difficult to persuade. They focus on apparent flaws, such as writing quality, misleading motivation, or methodological limitations, while citing few specific details. Their overall style is concise, direct, and negative.

| Metric | Value |
|------|-----|
| Sample share | 9.8% (98 reviews) |
| Historical score-increase rate | 13.8% |
| Acceptance rate | 27.6% |
| Successful rebuttal samples | 30 |

### Identifying signals

- Use strong negative phrases such as "not well-written", "misleading", and "limited".
- Criticize without constructive suggestions or specific directions for improvement.
- Use concise, direct wording, often listing issues in short sentences or bullets.

### Rule-statistic differences (Top 3)

- **New experiments / new results**: Success 60.0% vs. failure 34.3% (Δ +25.7)
- **Explicit revision commitments**: Success 43.3% vs. failure 60.0% (Δ -16.7)
- **Clarification**: Success 63.3% vs. failure 77.1% (Δ -13.8)

### Strategy vector effects (Cohen's d)

**Substantially higher in the successful group (Cohen's d):**
- `direct_address`: Successful mean 4.5 / Unsuccessful mean 2.691 (d=1.241)
- `tone_confidence`: Successful mean 4.4 / Unsuccessful mean 2.603 (d=1.307)
- `clarification_quality`: Successful mean 4.333 / Unsuccessful mean 2.588 (d=1.212)

**Higher in the unsuccessful group (risk dimensions):**
- `vague_future_work`: Successful mean 1.433 / Unsuccessful mean 2.574 (d=-0.721)
- `overpromise_risk`: Successful mean 1.533 / Unsuccessful mean 2.309 (d=-0.551)

### Success patterns (LLM-derived)

- **Confident, direct responses**: Address criticism directly and confidently, without avoiding the central issue, and demonstrate a deep understanding of the work.
- **Concrete supporting evidence**: Provide new experiments, quantitative results, or specific data rather than relying only on explanations or promises.
- **Clear, structured explanations**: Organize responses with bullets or headings to improve readability, and give high-quality clarification for each criticism.
- **Controlled concessions**: After acknowledging some weaknesses, immediately emphasize the contribution or improvements rather than dismissing the entire work.

### Failure patterns (LLM-derived)

- **Vague future-work promises**: Replacing current evidence with "we will address this in future work" fails to meet the reviewer's demand for immediate validation.
- **Overpromising risk**: Exaggerating the method's capabilities or promising unrealistic effects deepens the reviewer's distrust.
- **Excessive concessions and self-negation**: Readily accepting criticism and making sweeping changes to terminology or positioning weakens the perceived contribution and suggests a lack of confidence.

### Key strategy

Respond directly and confidently, replacing vague promises with concrete evidence.

---

## Cluster 1: Gentle Constructive

**Profile**: These reviewers primarily aim to help the authors improve the paper rather than find faults. Their style is gentle and specific, often using questions or suggestions to propose improvements. They value actionability, show low severity, and are relatively open to persuasion. They appreciate the contribution and baselines while raising constructive questions about details.

| Metric | Value |
|------|-----|
| Sample share | 34.5% (345 reviews) |
| Historical score-increase rate | 13.4% |
| Acceptance rate | 50.4% |
| Successful rebuttal samples | 177 |

### Identifying signals

- Ask gentle questions such as "It would be helpful if..." or "Is this still true...".
- Explicitly organize comments into "Strengths" and "Questions", with a clear structure and positive opening.
- Give specific, actionable suggestions, such as adding a particular task or analysis, instead of general criticism.

### Rule-statistic differences (Top 3)

- **New experiments / new results**: Success 56.5% vs. failure 46.6% (Δ +9.9)
- **Clarification**: Success 60.5% vs. failure 68.6% (Δ -8.1)
- **Moderate acknowledgment**: Success 54.2% vs. failure 61.0% (Δ -6.8)

### Strategy vector effects (Cohen's d)

**Substantially higher in the successful group (Cohen's d):**
- `tone_confidence`: Successful mean 4.593 / Unsuccessful mean 3.398 (d=1.036)
- `direct_address`: Successful mean 4.689 / Unsuccessful mean 3.512 (d=0.985)
- `clarification_quality`: Successful mean 4.492 / Unsuccessful mean 3.349 (d=0.963)

**Higher in the unsuccessful group (risk dimensions):**
- `overpromise_risk`: Successful mean 1.35 / Unsuccessful mean 2.018 (d=-0.637)
- `vague_future_work`: Successful mean 1.542 / Unsuccessful mean 2.157 (d=-0.51)

### Success patterns (LLM-derived)

- **Confident, direct responses**: Address each specific question directly and confidently, avoiding ambiguity, evasion, and excessive apology.
- **Concrete supporting evidence**: Use new experiments, quantitative results, data, or specific manuscript references instead of empty promises to address the central concerns.
- **Controlled concessions**: Acknowledge valid points or limitations while clearly explaining the position, core contribution, or existing evidence; avoid wholesale self-negation.
- **High-quality clarification and structure**: Give clear, structured explanations using headings, numbering, or paragraphs, with specific manuscript references such as tables and sections to improve readability and persuasiveness.

### Failure patterns (LLM-derived)

- **Overpromising risk**: Promising extensive future work or improvements that cannot be verified immediately, such as "we will address this in future work", without concrete action plans leads reviewers to doubt feasibility.
- **Vague future work**: Substituting vague plans such as "will be explored" for a specific answer leaves the central concern unresolved and weakens persuasion.
- **Unconfident defenses**: Hesitant or excessively apologetic wording, with no direct, targeted explanation, makes reviewers doubt the authors' confidence or leaves the response disconnected from the question.

### Key strategy

Respond directly and confidently, support the response with concrete evidence, and avoid empty promises.

---

## Cluster 2: Concise Affirmative

**Profile**: These reviewers give brief, broad positive assessments with few concrete details or actionable suggestions. They may think the paper is already good enough to require little criticism, or they may have invested limited effort in reviewing, resulting in general feedback.

| Metric | Value |
|------|-----|
| Sample share | 5.3% (53 reviews) |
| Historical score-increase rate | None% |
| Acceptance rate | 52.8% |
| Successful rebuttal samples | 27 |

### Identifying signals

- Write very brief reviews, usually only one or two sentences.
- Use general positive words such as "rigorous", "strong", or "good" without specific support.
- Identify no specific problems or improvement directions, showing very low constructiveness.

### Rule-statistic differences (Top 3)

- **New experiments / new results**: Success 48.1% vs. failure 65.0% (Δ -16.9)
- **Clarification**: Success 59.3% vs. failure 75.0% (Δ -15.7)
- **Explicit revision commitments**: Success 74.1% vs. failure 60.0% (Δ +14.1)

### Strategy vector effects (Cohen's d)

**Substantially higher in the successful group (Cohen's d):**
- `tone_confidence`: Successful mean 4.731 / Unsuccessful mean 3.44 (d=1.136)
- `clarification_quality`: Successful mean 4.654 / Unsuccessful mean 3.48 (d=1.043)
- `direct_address`: Successful mean 4.808 / Unsuccessful mean 3.64 (d=1.008)

**Higher in the unsuccessful group (risk dimensions):**
- `overpromise_risk`: Successful mean 1.154 / Unsuccessful mean 1.6 (d=-0.646)
- `vague_future_work`: Successful mean 1.423 / Unsuccessful mean 1.64 (d=-0.24)

### Success patterns (LLM-derived)

- **Confident, direct responses**: Answer each question directly and affirmatively, without ambiguous or defensive language, and show a clear understanding of the issue.
- **High-quality clarification**: Provide clear, grounded explanations tied to manuscript content or cited literature rather than relying only on new experiments; demonstrate deep understanding.
- **Controlled concessions**: Acknowledge limitations while clearly showing completed improvements or concrete plans. Avoid empty promises and stand by the core contribution.
- **Manuscript grounding**: Anchor responses tightly to the manuscript with specific section, figure, table, or revision pointers to improve credibility and verifiability.
- **Structured responses**: Use numbering or paragraphs so the reviewer can track each answer, improving clarity and professionalism.

### Failure patterns (LLM-derived)

- **Overpromising risk**: Promising a future code release or many experiments without specific evidence in the rebuttal appears unreliable or distracting.
- **Vague future work**: Deferring key issues with phrases such as "will be explored in future" instead of addressing them in the rebuttal appears to evade the central criticism.
- **Too many untargeted new experiments**: Additional experiments that do not directly address the central concern are redundant or off-topic and suggest that the authors missed the key issue.
- **Defensive argument**: Arguing about terminology or definitions instead of addressing the issue makes the authors seem unreceptive or evasive.

### Key strategy

Respond directly and confidently, provide high-quality clarification, make controlled concessions, and avoid overpromising.

---
