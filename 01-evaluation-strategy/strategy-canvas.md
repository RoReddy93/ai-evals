# AI Evaluation Strategy Canvas

> Repo file `ai-evals/01-evaluation-strategy/strategy-canvas.md` (the repo is your submission).
> Becomes the Strategy Canvas slide of the final pitch deck you assemble in Module 6.

## 1. Product Strategy, The Context

**Target user:** VP-level Strategists and Product Leaders at Fortune 500 companies who pay a premium for verified market intelligence.

**Key use case:** Rapidly extracting specific, verified insights (e.g., comparing competitor pricing models or summarizing G2 reviews) without manual data digging.

**Value proposition:** Personalized, instant answers based on verified data, dramatically reducing the time spent finding and synthesizing information for high-stakes decisions and strategic roadmaps.

## 2. Measurements, The Execution

**User promise.** For VP-level enterprise strategists, Ascend IQ delivers source-supported answers to competitor-research questions, reducing research time versus manual search and synthesis. We target delivery within five seconds for 95% of supported queries, with additional verification time when needed.

**Top 3 trust metrics:**
- **Latency**, Response speed (P95 / P99). Slow kills engagement.
- **Hallucination Rate**, % of outputs that are confidently false or fabricated.
- **Fairness**, Quality consistency across user groups, geos, languages.

**Why these three:** • Hallucination, VP-level clients pay $50k+ for verified data; one fabricated stat ends the contract.
• Latency, <5s response is the only thing that beats manual digging.
• Fairness, consistent factual quality across English, German & French underpins our European Enterprise expansion.

## 3. Strategic Trade-Offs, The Cost

### Trade-off 1 · Hallucination Rate ↔ Latency
We prioritize factual reliability over the five-second latency target when additional verification is necessary. Our users rely on competitor intelligence for consequential roadmap and investment decisions, so an unsupported pricing claim creates greater risk than a modest delay. If verification takes longer, we communicate progress; if evidence remains insufficient, we explicitly say so.

### Trade-off 2 · Fairness ↔ Latency
We allow additional retrieval and verification time for German and French queries when testing shows this improves factual accuracy or citation support. European customers pay for the same dependable intelligence as English-speaking customers, so faster responses should not come at the expense of a lower quality standard. We measure completion and abandonment by language to ensure the added wait remains acceptable.

---
_Generated from the AI Evaluation Strategy Canvas, M1 lab tool, AI Evals Certification._