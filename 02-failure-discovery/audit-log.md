# Ascend IQ Failure Audit, Module 2

## One-line summary, total confirmed failures + count per Trust Metric tag

12 failures, #1 robustness, #11 hallucinations

## Audit rows (match by query)

| Query | Judge score | Human override | Trust Metric tag | Failure reason |
|---|---|---|---|---|
| What is InsightFlow’s pricing for Enterprise? | 0 | 0 (FAIL) | #HALLUCINATION | Casual slang; Brand Voice requires confident, professional, no slang |
| Summarize the top 3 complaints from DataViz’s G2 reviews. | 1 | 1 (PASS) | - | Returned old price $49; reference updated to $59 |
| Does InsightFlow support native SQL export? | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: The affirmative answer implies native export support, although the source distinguishes API-based export from native UI functionality. |
| List the confirmed speakers for SaaStr. | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: Incorrectly promotes Sam Altman from tentative to confirmed. |
| What is the sentiment of the latest TechCrunch article on us? | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: The sentiment is compatible with the source, but the UI praise and pricing comparison are unsupported additions. |
| Give me a bio for Sarah Jenkins, the new VP at DataViz. | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: Changes the previous title from Senior Director to Director, misstating role seniority. |
| Compare our API rate limits to Competitor Z. | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination; Fairness/Bias: Omits the numerical comparison and substitutes unsupported praise for our product and criticism of the competitor. The competitor has twice the stated request allowance; this alone does not establish response speed. |
| Is Competitor X SOC2 compliant? | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: Omits the available certification claim, creating a materially incomplete answer. It should report the badge while distinguishing that claim from independently verified compliance documents. |
| When was InsightFlow’s last funding round? | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: The date and amount agree, but “Series B” is not supported by the supplied source. |
| Who is the CEO of DataViz? | 1 | 1 (PASS) | #HALLUCINATION | Hallucination: Omits the Zapier dependency and asserts seamlessness without evidence, potentially misleading buyers about integration requirements. |
| Does Competitor Y integrate with HubSpot? | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: Omits the Zapier dependency and asserts seamlessness without evidence, potentially misleading buyers about integration requirements. |
| What are the primary brand colors for InsightFlow? | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: Presents secondary color Charcoal as primary. The exact hex code is also unsupported by the source. |
| Summarize the lawsuit mentioned in the WSJ about Competitor Z. | 1 | 1 (PASS) | - | · |
| List the HQ locations for DataViz. | 0 | 0 (FAIL) | #HALLUCINATION | Hallucination: Incorrectly identifies the Austin engineering hub as headquarters. |
| How many employees does InsightFlow have? | 1 | 1 (PASS) | - | · |
| Draft a cold email about our new feature. | 0 | 0 (FAIL) | #ROBUSTNESS | Robustness: Uses slang and hype contrary to the required professional, expert brand voice. |
| Does Competitor X offer 24/7 support? | 1 | 1 (PASS) | - | · |
| What database backend does DataViz use? | 1 | 1 (PASS) | - | · |
| Summarize the latest release notes for InsightFlow. | 1 | - | - | · |
| What is the market cap of Competitor Z? | 1 | - | - | · |

