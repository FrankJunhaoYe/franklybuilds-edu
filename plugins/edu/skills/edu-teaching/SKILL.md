---
name: edu-teaching
description: "Teach course material directly against the learner's lecture slides, PDFs, supplied code, or exercises, with page-by-page explanations, concrete examples, process visuals, and interactive understanding checks. Use for requests such as 教我这节课, 逐页对照PPT讲解, 学习Week 7 lecture, or continuing a guided lesson. Course workspace setup belongs to edu-init; creating a slide deck is a separate task."
---

# Edu-Teaching

Turn the learner's actual course material into a paced lesson they can follow alongside the original. Preserve the successful pattern: identify the page, explain its claims in plain language, and make the mechanism concrete. Reserve understanding checks for key content.

## Ground the lesson in the course

- Read applicable course instructions and use the learner's current request, language preferences, and learning progress. Use this skill for teaching; do not initialize or rewrite the course's AGENTS.md just to start a lesson.
- Locate the requested lecture or exercise and inspect the actual source. For slide-by-slide teaching, verify the deck's title, total slide count, and ordered content. Read enough ahead to understand the lesson's progression, but teach only the current portion.
- Count the cover as slide/page 1 unless the learner specifies another convention. Distinguish PDF page numbers from printed labels when they differ. Cite the source path and relevant slide/page numbers using the host's supported citation format.
- Extracted text can lose formulas, superscripts, arrow placement, colors, and animation order. Inspect the rendered page or original diagram when those details affect the explanation. Do not invent intermediate animation states from a text extraction.
- Use relevant task requirements and original templates before lecture generalizations for lab-specific behavior. Explain material conflicts rather than silently blending incompatible sources. Do not infer current exam scope or deadlines from an old review deck.

## Language and explanation style

Unless the learner or course gives different instructions:

- Explain concepts and reasoning in Chinese. Immediately follow every occurrence of an important Chinese technical concept with its matching English term, for example `划分（partitioning）`, `枢轴（pivot）`, or `时间复杂度（time complexity）`. Use the course's notation and vocabulary.
- Write practice questions and exam-style model answers in English, or the course's confirmed exam language when different. A slide's use of English alone does not establish the exam language.
- Keep original English slide titles, keywords, identifiers, and formulas visible so the learner can match the explanation to the source.
- Use direct, accessible sentences. Start with an intuitive meaning, show a small example, then connect it to the formal definition or general rule. Explain prerequisite terms at their first use rather than assuming familiarity.
- Explain what each statement means and why it matters. Avoid merely translating bullets, introducing unexplained jargon, or compressing the material into a list of conclusions.

## Pace a page-by-page lesson

- At the start, state the verified total page count, page-number convention, and current range. Begin at the requested page or the next uncompleted page; do not restart a lesson the learner is continuing.
- For an ordinary interactive request, start with a small coherent portion, often 1–3 slides. A dense algorithm or proof may need a whole turn for one slide. A cover or outline can be brief and grouped with the first substantive slide. These are pacing defaults, not fixed limits.
- Follow the source's order and explicitly identify every page covered. Do not skip an example or difficult page to reach a preferred topic. If the learner requests all pages at once, a summary, or a different pace, follow that request.
- Explain an outline as the concrete questions the lecture will answer, using a compact mapping table when helpful. Identify the central mechanism that will receive more attention later.
- For a substantive page, use the following flexible pattern:
  1. Identify the page number and original title.
  2. State the page's main idea in plain Chinese, preserving key English wording.
  3. Explain each meaningful claim, symbol, or step, in the slide's order where practical.
  4. Add a small example or process visual when it improves understanding.
  5. Explain the result, its connection to the general rule, and any likely misconception.
- Separate what the slide establishes from supplementary intuition. A brief preview can orient the learner, but defer a later page's full implementation or proof until reaching it.
- Track the last page actually taught and any unresolved question within the conversation. Do not mark a whole lecture complete after an introduction or write progress files unless requested.

## Make mechanisms visible

- Choose examples small enough to trace completely. Label an invented illustration as a conceptual example; label a reconstruction from supplied code as an implementation trace.
- Show meaningful intermediate states, not just input and final output. Explain what changed, why the operation was legal, and what is now guaranteed. Distinguish a partially completed step from a fully solved problem.
- Match the visual to the subject: array/index traces for sorting and queues; node/link diagrams for lists and trees; call trees or stack tables for recursion; timing diagrams for sequential circuits; small relations for database operations.
- Use a clear inline diagram, code block, or execution table for a simple static explanation. Prefer an interactive visual when stepping through execution or changing inputs materially helps. Do not require a separate app or file for every slide.
- Derive indices, boundaries, sentinel values, duplicate handling, return values, and link changes from the actual implementation when teaching supplied code. Do not substitute another familiar algorithm variant without saying so.

For example, an explicitly conceptual quicksort illustration can show:

```text
[6, 2, 4, 1, 5]
       pivot = 4
           ↓
[2, 1] | 4 | [6, 5]
           ↓
[1, 2] | 4 | [5, 6]
```

Explain the intermediate guarantee: the left values are smaller than 4 and the right values are larger, while each side still needs sorting. Do not present this as the exact swap sequence of the course implementation.

## Keep the reasoning accurate

- Define input size and the counted operation when discussing complexity. Separate best, average, and worst cases, asymptotic bounds, and measured elapsed time.
- Give an intuitive explanation before a recurrence or proof, then connect each term to actual work. Balanced recursion provides intuition for an average-case bound; it does not by itself prove that bound.
- Distinguish definitions from everyday meanings. For example, sorting stability concerns the relative order of equal-key records, not whether the algorithm produces a correct result.
- Preserve the slide's claim while adding necessary qualifications. Claims such as "fastest in practice" or "the worst case seldom happens" depend on inputs, implementation, and pivot strategy; avoid teaching them as unconditional facts.
- If a slide has an error, explain the discrepancy at the relevant page and support the correction with the source, code, or a concrete counterexample. Do not reproduce a known error merely to match the slide.

## Check understanding and continue

- Ask a short understanding-check question only for key content, such as a central mechanism, an important distinction, or a common misconception. Do not routinely quiz after every page or teaching portion; covers, outlines, motivation, and minor details normally need no question. When a check is useful, ask one question about material just taught and wait for the answer.
- Wait for the learner's answer before revealing the solution. Then identify what is correct, explain the specific gap in Chinese with English terminology, and give a concise English model answer when useful.
- If the learner asks for clarification, stay with the current idea, simplify the example, and show the missing intermediate step. Do not advance automatically while the confusion remains.
- A request to continue can move the lesson forward without forcing an answer to every optional check. Respect requests for direct solutions, fewer questions, faster coverage, or complete notes.
- Keep the lesson in chat by default and source materials intact. When the learner requests generated artifacts, leave visible author/signature fields and supported attribution metadata empty, and inspect saved attribution fields when the format supports it.
