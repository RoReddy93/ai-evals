# Ship/Hold Memo · Ascend IQ

> **Decision:** 🚀 SHIP

**To:** [CPO] · cc Eng Lead · Trust & Safety  
**From:** [Rohit Reddy] · AI Evals Cohort · [10/19/2026]

## The Answer

I recommend we SHIP Ascend IQ to enterprise customers in the next sprint, contingent on the documented mitigation plan, to protect $4.2M in at-risk renewal revenue.

## The Arguments

### 1. Hallucination risk on financial summaries is contained but not eliminated.

Our P0 risk, fabricated financial figures in monthly enterprise summaries, was the most critical failure mode surfaced in our Module 2 audit. After the M3 eval suite + M4 hard-gate, the failure rate dropped from 9.2% to 2.1%. This is below our gate threshold of 3%, but above the 1% "zero-incident" bar enterprise leadership has signaled.

### 2. Bias remains a P1 we're explicitly accepting under a 30-day audit window.

Our Coverage Matrix from M5 shows the regional bias eval has 78% coverage, short of our 90% bar. The Eval Playbook mandates a 30-day post-launch audit with Trust & Safety as the escalation owner. We've sized this risk: any variance above 2% halts new enrollments until a fix lands.

### 3. Revenue exposure compounds if we hold for the perfect launch.

Three enterprise accounts ($4.2M ARR) have flagged Ascend IQ as a non-negotiable contract requirement for Q3 renewal. Holding for another sprint risks losing them to a rival who has publicly marketed a less-rigorous but shippable competitor. The trust debt we accept here is smaller than the revenue debt of inaction.

## Evidence · Trust Metrics

```
- Hallucination rate: 2.1% (Gate: < 3%) ✓ PASS · Source: eval suite, n=400
- Factual grounding: 97.8% (Gate: > 95%) ✓ PASS · Source: golden-set audit, 200 items
- Regional fairness variance: 1.7% (Gate: < 2%) ✓ PASS · Source: M5 Coverage Matrix
- Bias coverage: 78% (Bar: > 90%) ⚠ ACCEPTED RISK · Mitigation: 30-day post-launch audit
- Latency P95: 1.4s (Gate: < 2.0s) ✓ PASS · Source: production canary
```

## Business Risk

SHIP path: ~$4.2M renewal revenue protected; reputational risk capped at 30-day audit window with documented mitigation.
HOLD path: 3 enterprise contracts (~$4.2M ARR) at high churn risk in Q3; competitive window closes in 8 weeks.

## Next Step · Decision Needed

Decision needed by EOD Friday. If approved, we ship to canary on Monday with the 30-day bias audit committed. Trust & Safety reviews the audit results in the Sept 30 QBR with go/halt authority on continued enrollment.

## Reflection

_Defining "good enough" for hallucination was the hardest part, without the M1 Strategy Canvas and M2 severity ranking, our M4 gate would have been an arbitrary number. The discipline forced trade-offs the team had been silently disagreeing about for weeks._
