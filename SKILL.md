---
name: Copy review full pass (Clark)
description: >-
  Use on every copy review (LinkedIn, X, newsletter, web, email, journal) before
  giving a verdict. Runs the 16-pass checklist with selective Roy Peter Clark
  tools, a pre-pass lint, and a receipt. Review only, never publish.
---
# Copy review full pass (Clark)

Red pen only. Runs after an author (a writer, web editor, marketing lead, or the owner) hands over a candidate draft. Short pieces are not exempt.

## Precedence
1. Owner locks (locked lines, family sentences, owner rulings) beat everything.
2. David's taste sheet `/workspace/gmp-taste/GMP_Taste_Sheet_2026-10-04.md` and style guide.
3. Gates in the `david-copy-quality` skill (referenced, not copied here).
4. noslop and humanizer patterns are watch-list aids only.

## 0. Intake
- Record draft path, channel, format, author, and `sha256sum` of the draft. Every finding cites that SHA.
- Load the source packet, claim ledger, story contract, and `family_wording_status` if they exist. The candidate is never its own evidence.

## 1. Pre-pass lint (before pass 1)
Run `/workspace/journal/tools/journal-lint/journal_lint.py <draft> --prior <previous>` and cite the report path and SHA. Any unwaived BLOCK sends the draft back with no full review. The list below documents what the script checks (spec of record: `/workspace/org/quality/marketing-input/copy-editor.md`); forced groups of three and synonym cycling stay by-eye items. Always include:
- Em dash and horizontal bar (L1, L2), emoji (L4), banned words (L5), dead transitions and throat-clearing (L6, L7).
- Not-X-but-Y: L8 (a) to (c) plus the humanizer-trial forms: `\b(is|are|was|were)n'?t\b[^.]{0,60}\.\s+(It|They|That)('s| is| are| was| were)\b`, `\b(is|are|was|were)n'?t just\b`, `^Not [^.]{1,40}\.$`, `\. Not (the|a|"|just)\b`, `\bnot just\b[^.]{1,60}\bbut\b`.
- Bait closers (WARN, flag only; real closing questions stay): `What do you think\?`, `\bThoughts\?\s*$`, `\bAgree\?`, `Let that sink in`, `Read that again`.
- AI-tell patterns (WARN, flag with the exact line; fix only when the plain version keeps the meaning; added Oct 19 2026 at David's yes, from the humanizer list, without its scoring or example rewrites, whose invented numbers we never use):
  - Copula avoidance: `\b(serves|stands|acts) as\b`, `\b(boasts|represents)\b` where "is", "are", or "has" works.
  - Forced groups of three: triple adjectives, nouns, or parallel clauses that exist for rhythm, not content. Check by eye; keep a three that the facts actually have.
  - Synonym cycling: one thing renamed across nearby sentences to dodge repetition (the agent, the advisor, the professional). Use one name.
  - False ranges: `\b[Ff]rom [^.,]{2,40} to [^.,]{2,40}` where the ends are not on one scale.
  - Empty -ing tails: `, (highlighting|underscoring|emphasizing|ensuring|reflecting|showcasing|fostering|contributing to|symbolizing)\b`.
  - Generic upbeat endings: `future (looks|is) bright`, `exciting times`, `the journey`, `only the beginning`, and any closing line that could end any piece.
- Strength-word drift against the source or prior version: no new `only|every|always|never|guaranteed`, no "can help" turned "will", no "might" turned "would", no added reason, cause, or benefit.
- Leak, claim, jargon, family, and placeholder rows (L13 to L19).

## 2. The 16 passes (in order, never reorder)
1. Intake: artifact, channel, SHA, packet present.
2. Provenance: trace every first-person fact, number, quote, duration, and named result to the packet. Classify Confirmed, Inferred, Directional, Unverified, Rejected, OWNER REPORT. Flag invented specificity.
3. Story fidelity: premise, tension, POV, concessions, ending intact. If pass 2 or 3 fails: status MUST FIX or "return to story lock", route back, no polish, Clark table reads "deferred, route back".
4. Coherence plus selective Clark (see section 3). Includes a fresh opening and whole-piece reader test.
5. Clarity: one-read follow for "David three years ago"; every jargon hit gets translate-or-cut.
6. Voice: see section 4.
7. Style hard gates: lint BLOCK rows at zero; LinkedIn has no body links or hashtags and passes length.
8. So what: every section changes understanding, belief, memory, or action.
9. Proof: evidence near the claim, honestly qualified, ledger-traceable. Never invent a number.
10. Specificity: scenes, mechanisms, nouns replace abstractions without unsupported detail.
11. Identity swap: if labels swap and it fits anyone, restore an owned observation or decision.
12. Narrative and format: fits the declared job and channel. Web conversion copy gets a final friction pass.
13. Family and privacy: held means no family nouns; locked means exact locked sentence only.
14. Leak scan: clients, emails, paths, secrets, internals; personal brand names neither AdvisorReach nor ARIN.
15. Rights and redaction: consent, photo rights, attribution. Never clears publication.
16. Receipt and verdict: see section 6.

## 3. Selective Clark step (pass 4)
Follow `references/selective-draft-diagnostics.md`.
- Keep an untouched baseline. Name each paragraph's job and only consequential gaps.
- Per finding: exact passage plus observable symptom, then 0 to 3 tool definitions from `references/writing-tools-registry.json` (catalog: `references/clark-55-tool-catalog.md`). Rejected candidates count toward the 3. Tools 51 to 55 are Inferred.
- Test the smallest revision, including keeping the line as is. Record exact before and after, then disposition: keep, reject, no change, owner decision, return to story lock.
- Clean passage: record "no change" with a one-line reason. No tool soup; tool count is never a score.
- A missing fact becomes a question to the owner (max 5, each quoting the line), never an invented bridge.

## 4. Voice (pass 6)
Use `references/voice-feedback.md` and the `david-copy-quality` skill. Compare stance, certainty, density, and cadence, not just phrases. Friend over coffee, process as hero, show not report. Ask: would David say this to a friend? Label inferred voice rules as provisional.

## 5. Evidence lenses (only when contract or evidence is thin)
From `references/evidence-led-copywriting.SKILL.md`: Huh, Point at it, So what, $10, destination. Lenses for findings only, never a license to rewrite the story.

## 6. Receipt (every run)
Save beside the draft or in the review folder. Order:
1. Verdict first: REVIEWED, MUST FIX, OWNER DECISION, or recommend COPY APPROVED; disposition Accept, Minor revision, Rework, Rejected.
2. Draft path and SHA-256, lint counts.
3. Pass table: 16 rows, Pass, Fail, or N/A with one-line evidence.
4. KEEP, CUT, REWRITE with exact lines.
5. Claims posture.
6. Family status and leak result.
7. Clark findings or clean "no change".
8. Next gate (author recheck against new SHA, or David copy-yes).
PASS WITH EDITS goes back to the author; recheck only against the new SHA.

## Hard rules
- Recommend COPY APPROVED only; David or the authorized owner grants it.
- Never write `publication_authorized: true`. Never edit the draft. Never post, schedule, or publish.
- Write only the receipt.

## Sources
Canonical copies live on David's PC under `C:\Users\davm3\Agile Mind_Development\Content Marketing Hub\plugins\content-story-studio\` (skills `content-copy-review`, `evidence-led-copywriting`; `references\selective-draft-diagnostics.md`, `writing-tools-registry.json`, `voice-feedback.md`, Clark catalog). The 16-pass checklist source is the `copy-editor-full-pass` skill. Last synced to `references/`: Oct 10, 2026. Re-sync if the PC versions change. The Oct 19 AI-tell lint rows are box-only until mirrored to the PC copy.
