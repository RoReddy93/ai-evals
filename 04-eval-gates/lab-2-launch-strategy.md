# Module 4 · Launch Strategy · Section 4.0 Release Criteria

_Generated from the M4 Launch Strategy Builder. Drop this into your PRD as Section 4.0._

## 4.0 Release Criteria

The following thresholds must be met by Model Candidate v1.x before approval for production deploy. Eval Specs from Module 3 define the measurement methodology.

| Severity | Metric | Threshold | Dataset | Method |
|---|---|---|---|---|
| 🔴 Hard (Blocker) | Pricing Hallucination Rate | 0% | `Ascend_IQ_Logs` | https://github.com/RoReddy93/ai-evals/blob/main/03-eval-suites/lab-2-eval-spec.md |
| 🟡 Soft (Review) | Latency (P95) | <2.5s | `Ascend_IQ_Logs` | _[Example Spec]_ |
| 🔵 Advisory (Monitor) | Tone Consistency | >=4/5 | `Ascend_IQ_Logs` | _[Example Spec]_ |

## 4.1 CI Gate Policy

These thresholds run in a GitHub Actions gate on every pull request, replaying deterministic fixtures from the regression golden set (≥ 30 cases). PM owns the policy; Engineering owns the YAML.

> Block the code merge if 2pp drop is observed on the hard gate when measured against golden data. Warn if the drop is 1pp.

## 4.2 Mitigation Plan · Soft Gate

**Selected Lever:** Staged Rollout

> If our Soft Gate fails (Latency exceeds 4s for complex multi-doc summaries), we recommend **Staged Rollout** because we limit the impact to a certain % of the user population, before we can commit to a reasonable latency to all users based on real-world usage data

---

_Lab artifact for Module 4, AI Evals Certification, Product School. Becomes the Eval Gates slide of the Final Project deck._