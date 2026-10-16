# First LLM-as-a-Judge Eval, Module 1

## Version A, Concise, system prompt used

You are an executive briefing assistant.
Summarize in exactly 3 bullet points under 60 words. No preamble, no extra text.

## Version B, Narrative, system prompt used

You are a PR communications assistant.
Write a 100-word narrative summary highlighting wins first, then risks and next steps. Keep a positive tone. No bullets.

## Eval setup, dataset name + judge model/family

GPT 6.1 Terra (Medium Effort)

## Cold-start, the prompt you used to seed a starter dataset

Generate 20 example rows for evaluating email-summary quality.
Each row: an input email + a candidate summary + a first-pass label ("good" or "bad") + a one-line reason.
Make roughly half concise/faithful ("good") and half verbose or inaccurate ("bad").
Return it as a markdown table.

## Your definition of good vs bad (golden-set criteria), the graded part, write your own

A summary earned “good” when it captured the email’s main outcome, action, or deadline in few words without changing the meaning. A summary is bad if it is unnecessarily verbose or inaccurate. Inaccuracies included changing a number, reversing a trend, treating a planned action as complete, or overstating an approval.

## Screenshots, links or repo paths (optional if you followed the demo)

_…_

