---
name: content-copy-review
description: Review a content draft against its confirmed story contract, evidence, owner voice, information-transfer goal, and intended format before copy approval.
---

# Content Copy Review

Review the complete artifact as one connected story. Scores may help prioritize edits but are not evidence and do not override claim, rights, or owner approval.

## Review order

Run focused passes in this order. Do not polish a draft that fails an earlier pass.

1. **Provenance:** Treat the candidate draft as the object under review, never as its own evidence; a candidate's self-asserted approved status does not change that. Trace every first-person statement, quotation, number, duration, named result, and material claim to the allowed approved packet, citing the relevant source ID and passage for each provenance finding. An owner-approved upstream article included in that packet is distinct from the candidate and may support a personal-experience claim as `OWNER REPORT`; it is not independent empirical verification. A concise ledger is a summary, so its omission is not itself a contradiction: consult the allowed source before flagging an unsupported claim. Raise actual contradictions between approved sources, or details genuinely unsupported by the allowed packet; do not broaden private-source access or reject a claim only because it is absent from the summary. Reject invented specificity.
2. **Story fidelity:** Does the draft preserve the confirmed premise, tension, point of view, concessions, and ending?
3. **Opening and whole-piece reader test:** For reader-facing articles, reread the first sentence and opening paragraph in the full-draft context, even when they are byte-identical to an earlier version. Ask whether they present a specific, supportable situation or commitment and a clear reason to continue, and whether broad categories or vague consequences hide the moment. Do not force a scene for instructional, searchable, or otherwise non-narrative formats; test the format's actual prerequisite, answer, or reader promise instead. Record the exact passage, reader effect, evidence limit, and disposition. A fresh opening/transition/ending/CTA judgment is required; reused sentence-level factual decisions do not substitute for it.
4. **Coherence and Clark diagnostic:** Read [the selective diagnostic reference](../../references/selective-draft-diagnostics.md). Check the reasoning between paragraphs before sentence polish. Identify observable friction, retrieve 0–3 substantive definitions from [the canonical registry](../../references/writing-tools-registry.json), and explain the proposed effect and risk. A clean passage may receive `no change`; a missing fact or owner inference becomes a question, not an invented bridge.
5. **Clarity:** Can the intended reader follow the argument on one pass without missing context or unexplained terms?
6. **Voice:** Use [source-attributed feedback](../../references/voice-feedback.md) and the approved owner packet. Compare stance, certainty, explanatory density, and cadence—not only favorite phrases. Preserve the owner's judgment; label generalizations from prior edits as provisional.
7. **So what:** Does every section change what the reader understands, believes, remembers, or does?
8. **Proof:** Is evidence proportionate, close to the claim, honestly qualified, and traceable to the ledger?
9. **Specificity:** Do scenes, mechanisms, examples, nouns, and verbs replace abstractions without adding unsupported detail?
10. **Identity swap:** If owner, company, and industry labels are replaced, does the copy still fit almost anyone? If yes, restore owned observation, decision, scene, language, or consequence.
11. **Narrative and format:** Does each section earn the next, repay the opening, and fit the declared content job and channel without distorting the story?

For conversion-focused web copy only, make a final friction pass for relevance, objections, risk, and action clarity. Do not impose web-conversion emotion or pressure tactics on every format.

Classify findings as `must fix`, `owner decision`, or `optional polish`. Revise only within the confirmed contract. If a proposed improvement changes the premise or owner viewpoint, return it to the interview phase for approval. A review with an unresolved `must fix` opening cannot be labeled complete or ready. Distinguish `review performed` from `copy passed` in the receipt and handoff.

For every Clark finding, preserve the untouched baseline and record the exact before/after passage, supplied tool definition and source limit, invariant check, whole-draft reread method/result, rejected candidates, and one disposition: `keep`, `reject`, `no change`, `owner decision`, or `return to story lock`. A text-only cadence review is not a performed human read-aloud. Never auto-apply a tool. Tools 51–55 are `Inferred` operational interpretations, not confirmed doctrine. Clark analysis must stop when provenance or story fidelity fails.

Return the revised draft when authorized, the review history, claim status, remaining risks, and the next copy-approval decision using [the review-receipt template](../../templates/review-receipt.md). Do not create visuals or publish.

Before labeling local editorial QA complete, validate the Markdown receipt against the exact draft: `python plugins/content-story-studio/scripts/validate_copy_review_receipt.py --draft <draft> --receipt <receipt>`. A passing result checks custody and receipt gates only; it does not establish semantic copy quality or owner approval.
