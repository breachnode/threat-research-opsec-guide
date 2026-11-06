# Write-up Standards: Writing Findings for Defenders

A finding is only as good as its write-up. These standards govern every finding that leaves the research environment — whether it is published, shared with an employer, or shown to a hiring manager.

## The standard finding structure

Every finding uses the same shape. No exceptions — the structure is what makes findings comparable, reviewable, and usable.

1. **What** — what the threat or technique is, in one or two plain sentences.
2. **Evidence** — what public sources say about it, with citations. Facts only.
3. **Assessment** — what it means, labeled as assessment, with a confidence rating (High / Medium / Low — see `03-source-hierarchy.md`).
4. **So what (defensive implication)** — why a defender should care: who is targeted, what the impact is, how it fits into a larger campaign.
5. **Defensive action** — the controls, detections, or process changes that address it. Every finding must have at least one defensive action, or it does not belong in the write-up.
6. **Sources** — full citations, with publication dates and links to the public originals.

Use the blank template in `templates/finding-writeup.md`. It enforces this structure.

## Sanitize everything

Before a write-up leaves the research environment, strip it of anything that could identify a real person, a real victim, or a specific live operation:

- **No real personal data.** No names, emails, usernames, phone numbers, account numbers, or addresses belonging to real victims or real actors.
- **No marketplace names, links, or handles.** Describe the *type* of venue in general terms if the finding requires it ("a carding marketplace" is acceptable; naming one is not).
- **No operational detail.** Describe what a technique *looks like to a defender* — the indicators, the artifacts, the observable behavior. Never describe how to carry it out, what tools to use, or how to reach the people who do it.
- **No screenshots from illicit sources.** Ever. Public-source screenshots only, with metadata stripped (see `04-safe-collection.md`).
- **No prices, volumes, or vendor details** from illicit activity. Even aggregate figures taken from illicit sources are out of scope — they cannot be verified, and repeating them adds nothing a defender can act on.

If removing a detail makes the finding weaker, the finding was built on the wrong detail. Rebuild it from public sources.

## Label synthetic examples — always

When a finding needs an example indicator, log entry, or scenario to be understandable, write a synthetic one and label it unambiguously:

> **SYNTHETIC EXAMPLE (illustrative only, not observed data):** ...

Rules for synthetic examples:

- They must be **clearly labeled** at the point of use, not just in a footnote.
- They must be **plausible but invented** — realistic enough to teach, obviously not a claim about a real event.
- They must **never be presented as observed data**, even casually. "For example, an attacker might…" is fine. "We observed…" is not, unless you actually observed it through a lawful public source and can cite it.
- They must contain **no real data**: no real domains, no real IPs, no real names, no real card or account numbers. Use clearly fictional placeholders (e.g., `example-merchant.test`, `203.0.113.0/24` — the documentation ranges reserved for this purpose).

## Separate fact from assessment

This is the most common failure in junior threat writing, so it bears repeating:

- **Fact:** "CISA's advisory of [date] states that threat actors are using [technique] against [target type]." — with a citation.
- **Assessment:** "This suggests the technique is likely to appear against small e-commerce merchants next, because [reasoning]. Confidence: Medium." — labeled as assessment, with the reasoning visible.

Never write an assessment in the voice of a fact. Never cite your own inference as if a source said it. If a reader cannot tell which sentences are sourced facts and which are your judgment, the write-up has failed.

## Tone

- **Neutral and professional.** Describe threat actors accurately without admiration, excitement, or moralizing. The adversary is a problem to be solved, not a character to be admired.
- **Plain language.** Write for a defender who may not share your vocabulary. Define terms on first use. Short sentences beat long ones.
- **No hype.** Do not inflate prevalence, impact, or novelty. "Observed in public reporting" is stronger than "surging" or "exploding" — and it is true.

## Cite properly

Every factual claim carries a citation with:

- Author or publisher
- Title
- Publication date
- Link to the public original

If a claim has no public source, it has three options: find one, reframe it as a general defensive principle (and label it as such), or cut it. "I know this is true" is not a citation.

## Review before publishing

No finding is published without a self-review against this checklist:

- [ ] Does it follow the standard structure (what / evidence / assessment / so what / defensive action / sources)?
- [ ] Is every factual claim cited to a public source?
- [ ] Is every assessment labeled, with a confidence rating and visible reasoning?
- [ ] Are all examples labeled synthetic, or cited to public reporting?
- [ ] Is there any real personal data, marketplace name, link, handle, or operational detail? (If yes, remove it.)
- [ ] Does every behavior described have a paired defensive action? (If not, cut the behavior or add the control.)
- [ ] Would this embarrass you in front of a hiring manager, a background investigator, or a compliance reviewer? (If yes, cut it.)
- [ ] Is the tone neutral and professional throughout?

A finding that fails any item is not ready. Fix it or cut it — never publish around a failed check.
