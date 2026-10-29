# Selective draft diagnostics

This is the operational bridge between a draft and Roy Peter Clark's 55-tool catalog. It is a reasoning aid, not a rewriting checklist.

## Procedure

1. Confirm the source packet, claim ledger, and story contract. If provenance or story fidelity fails, stop and route the draft back to that gate.
2. Preserve an untouched baseline and inspect the whole piece. State the intended reader change, each major paragraph's job, and what the reader must understand to follow the next paragraph. Record only consequential gaps, not a commentary on every sentence. See Coherence below.
3. Identify the exact passage and observable symptom. Assign a code from `references/draft-diagnostic-map.json` when one fits. Retrieve zero to three candidate **definitions**, not just IDs, from the canonical `writing-tools-registry.json`. Use `python scripts/writing_tools.py --ids 24 22` from the plugin root, or read those records directly. Consult [source limits](writing-tools-sources.md). An unmapped symptom may use a justified registry candidate or no Clark tool; do not force a code.
4. For each candidate, explain how its actual principle addresses this passage, the predicted reader effect, meaning/voice risk, and why another candidate would not help. Tool 2 concerns sentence-edge emphasis, not generic thesis insertion; Tool 8 concerns a pattern and break, not deleting any connective sentence. Tools 51–55 remain `Inferred`; prefer a verified core principle when it fits equally well.
5. Test the smallest revision against the baseline, including preservation as an option. Record exact before/after and a diff or precise change description, then check premise, chronology, claim strength, ownership, qualifications, and intentional rhetoric. Reread the whole piece. Label the method honestly: `text-only cadence review`, `human read-aloud`, or `audio-assisted review`; identify actual evidence for the latter two rather than claiming an audible pass from text inspection.
6. Choose `keep`, `reject`, `no change`, `owner decision`, or `return to story lock`. Tool count and edit count are never quality scores.

When no material friction is found, record no change without manufacturing candidate retrieval. If candidates were considered for a finding, keep the total at three or fewer, including rejected candidates. Do not hide a larger checklist in the receipt's rejected list.

## Diagnostic codes

Use the machine-readable map as the source of candidate relationships. Common symptoms include `MEANING_LATE` (the governing meaning arrives too late), `AGENCY_BLURRED` (the actor or action is unclear), `JARGON_OR_ABSTRACTION` (the reader cannot picture the claim), `PACE_FLAT` (a unit creates no reason to continue), and `VOICE_GENERIC` (the passage survives an identity swap). A passage can have no code when no material friction is observed.

## Coherence before polish

For a consequential transition, ask: What question did the previous paragraph raise? Does this paragraph answer it, develop it, contrast with it, or supply a needed step? Name the missing relationship. Repeating a keyword or adding “That matters” does not supply a reason.

Choose among reordering existing material, deleting a digression, making a source-supported connection explicit, or asking the owner for missing reasoning. A bridge is not always another sentence. Never invent a cause, motive, chronology, or personal lesson to smooth a transition. If repair changes the governing idea, return to story lock.

For instructional and searchable pieces, test prerequisites and answer order instead of demanding a scene or suspense. For personal narrative, preserve the owner's actual decision and consequence; do not replace them with a universal lesson just because it sounds polished.

## Phase routing and voice

The registry's `phases` field routes all 55 tools. Tools 40–50 are working practices, not edits to impose on finished copy. Retrieve a relevant phase with `python scripts/writing_tools.py --phase research` when preparation or collaboration is the diagnosed issue. Core source support does not make the adaptation an experimentally proven method.

Use [voice feedback](voice-feedback.md) with the approved owner packet. Examples for David are scoped evidence, not universal rules. If a revision improves surface ease but weakens ownership, reject it or ask the owner; do not average away the loss.

## Receipt minimum

The review receipt retains baseline and candidate hashes, coherence finding, passage and symptom, code when applicable, 0–3 candidates with supplied definitions, predicted effect, risk, rejected candidates, exact before/after, invariant check, whole-piece review method/result, and disposition. Keep this brief for simple edits. These are inspectable editorial decisions, not private chain-of-thought or proof of reader benefit.

For a file-backed revision, `python scripts/editorial_diff.py <baseline> <candidate>` reports current hashes and actual text changes. Inspect that output against the receipt; the script does not verify the editor's interpretation or owner approval.
