---
name: grill-docs
description: Do your normal research, then grill every claim against ALL sources — not just the one it came from. Cross-document verification catches what single-source reading misses. Only deliver what survives.
---

## Source Count Rules (read first)

- **0 sources** → Stop. This skill does nothing. Answer normally.
- **1 source** → Run Phase 1 only (single-source integrity). Skip Phase 2 and 3 entirely. Deliver with: "⚠️ Only one source available — cross-document verification not performed."
- **2+ sources** → Run all three phases. This is where the skill earns its value.

Do NOT guess source count. Count the actual sources you retrieved.

---

## Before You Grill

Do your normal research first. Find sources, read them, synthesize a draft answer. Every factual claim in the draft must cite which source it came from. If you cannot cite a source for a claim, it is not a claim — it is speculation. Remove it before grilling.

---

## Phase 1: Source Integrity

**Goal**: Verify you read each source correctly before comparing sources against each other.

For each claim, grill it against the document it came from:

1. **Misrepresentation** — Did I rephrase the source in a way that changes or distorts its meaning? Quote the source verbatim next to my claim. If the source doesn't say what I said — fix it.

2. **Omission** — What did the source say about this topic that I left out? Is there relevant nuance, a caveat, or a counterexample I didn't mention? Add it back.

3. **Precision drift** — Did I state something as precise (a number, a guarantee, a "never" or "always") that the source states more loosely? If the source says "typically" and I said "always" — fix it. Match the source's precision.

4. **Version/context scope** — Is this claim version-specific or context-dependent, but I stated it as a general fact? If the source says "in Next.js 15" and I dropped that qualifier — add it back.

**Gate**: Fix every claim that fails Phase 1 before moving to Phase 2. Do NOT proceed to Phase 2 with broken claims. If a claim cannot be fixed, remove it now.

---

## Phase 2: Cross-Document Grilling

**Goal**: Every claim must face the full document set — not just the source it came from. Other documents may confirm, contradict, or expose gaps.

For each claim, grill it against ALL documents:

- Another source confirms it → **VERIFIED** (cite which source, quote the confirming text)
- Another source says something different → **CONTRADICTED** (quote both, note which is more authoritative and why)
- No other source mentions it → **ORPHANED** (search for more documents; if still orphaned after searching, mark SINGLE-SOURCE)

### Reverse Pass (do NOT skip)

For each document, ask: _"What does this document say that NONE of my claims captured?"_ One document often fills a gap another left. Extract any new claim, then run it through Phase 1 and Phase 2 like any other claim.

### Second-Source Stress Test

For every claim still standing after the reverse pass, ask: _"If I found one more independent source, would this claim hold?"_ If you are unsure — the claim is SINGLE-SOURCE. Flag it. Do not present it as verified fact.

---

## Phase 3: Resolve

Sort every claim into exactly one verdict:

| Verdict           | Meaning                                                                                    |
| ----------------- | ------------------------------------------------------------------------------------------ |
| **SURVIVED**      | Passed Phase 1 and Phase 2                                                                 |
| **FIXED**         | Was wrong or imprecise, now corrected (show **before → after**)                            |
| **REMOVED**       | Could not be verified, or contradicted beyond resolution (show **why**)                    |
| **SINGLE-SOURCE** | Only one document mentions it, no corroboration found (flag it)                            |
| **ESCALATED**     | Sources contradict and you cannot resolve → present **both sides** to the user with quotes |

### Challenge Your Corrections

Before delivering, ask:

- Did I introduce new claims that are not backed by any source?
- Did I overcorrect into vagueness? (Example: changing "always X" to "sometimes X" without source support for "sometimes")

### Grilling Table (mandatory)

You MUST include this table in your answer. The answer is not complete without it:

```
| # | Claim | Source | Phase 1 | Phase 2 | Final |
|---|-------|--------|---------|---------|-------|
| 1 | <claim text> | <source> | SURVIVED / FIXED (before→after) / REMOVED | VERIFIED by <source> / CONTRADICTED by <source> / ORPHANED | SURVIVED / FIXED / REMOVED / SINGLE-SOURCE / ESCALATED |
```

### Completion Checklist

Before delivering, verify every item:

- [ ] Every claim passed Phase 1 or was fixed/removed
- [ ] Every claim was checked against ALL documents in Phase 2 (not just its source)
- [ ] Reverse pass completed for every document (no document left unchecked)
- [ ] Second-source stress test completed for every surviving claim
- [ ] Every claim has exactly one final verdict
- [ ] Grilling table is included in the answer
- [ ] Corrections challenged — no new unbacked claims, no overcorrection into vagueness
- [ ] For ESCALATED claims: both sides quoted so the user can decide
