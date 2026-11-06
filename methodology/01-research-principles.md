# Research Principles

Threat research is a governed activity, not a hobby. These principles come first; every other file in this repo is these principles applied to a specific situation. If a research idea conflicts with a principle here, the principle wins.

## 1. Public sources first

Start with what is already public: vendor threat-intelligence reports, government advisories, academic papers, breach disclosures, and reputable security journalism. In most cases the public record already answers the question. Going further — toward primary collection from illicit sources — should be the exception, never the default, and only ever in a read-only posture (see `04-safe-collection.md`).

**Why:** public sources are lawful, citable, and verifiable. A finding built on public reporting can be shown to a hiring manager, a compliance reviewer, or a court. A finding built on material that can only have come from participating in illicit activity cannot.

## 2. Define the question before you collect

Every research session starts with a written question, not a browse. Examples of good questions:

- *"What indicators do credential-stuffing campaigns against e-commerce login pages share, according to public reporting from the last 12 months?"*
- *"Which defensive controls do public sources most often credit with stopping card-testing attacks on small merchants?"*

A written question does three things: it keeps collection bounded, it makes the session reproducible, and it gives you a test for whether a source is relevant. If a source does not help answer the question, it does not belong in the log.

## 3. Never transact, never contact, never test

- **No transactions.** Do not buy, sell, or exchange anything with threat actors. Do not pay for data, samples, or access.
- **No contact.** Do not message, email, or otherwise communicate with threat actors — not to ask questions, not to verify a claim, not "just to see."
- **No testing against live systems.** Do not test fraud techniques, credential stuffing, or card-testing methods against any live system — not a target's, not a "test" merchant's, not your own production system. Testing belongs in a lab you own, against systems you own, with synthetic data.

These are the red lines. They are restated in `legal-boundaries/red-lines.md` because they matter that much.

## 4. Minimize exposure

Touch as little as possible, for as short as possible. Collect the minimum needed to answer the question, then stop. Do not download material you do not need. Do not create accounts you do not need. Do not linger in places where the only thing to observe is wrongdoing.

Exposure is risk: legal risk, security risk (malicious files are common in illicit spaces), and reputational risk. A researcher who minimizes exposure is a researcher who can explain, precisely, what they did and why.

## 5. Separate fact from assessment

Every finding has two layers, and they must never be blurred:

- **Fact:** what a source says, or what was directly observed. Cite the source. Quote it accurately.
- **Assessment:** what you think it means, how confident you are, and what a defender should do about it. Label it as assessment.

A common failure in junior threat research is presenting an inference as an observed fact. The write-up standards in `05-writeup-standards.md` enforce the separation: every claim carries either a source citation or an explicit confidence label.

## 6. Document everything, as you go

If it is not written down, it did not happen — and if it cannot be reproduced from your notes, it is not research, it is a story. Log every session with the template in `templates/research-log.md`: the question, the sources consulted, what you found, and your confidence level. Write the log during the session, not from memory afterward.

Documentation protects you twice: it proves the work was done responsibly, and it lets a future reader (including a future you) verify the finding instead of trusting it.

## 7. The defender test

Before writing up any finding, ask one question: **"Would this help a defender detect, prevent, or respond to this threat?"**

- If yes, write it — with indicators, controls, and sources.
- If no — if the material is only interesting because it describes wrongdoing in detail — cut it. Curiosity is not a justification.

This test is the difference between threat intelligence and a tour of the underground. The brief in a companion project of mine (*underground-economy-threat-brief*) applies it to every entry: each attacker behavior is paired with the control that stops it. A behavior with no defensive pairing does not belong in the write-up.

## 8. Assume your work will be read by a skeptic

A hiring manager. A background investigator. A compliance reviewer. An opposing counsel. Write as if all four will read every word — because for published research, they might. That means:

- No exaggeration. No invented metrics, clients, or findings.
- No claims you cannot source or defend.
- No language that could be read as admiration for the adversary. Describe threat actors accurately and neutrally; the focus stays on defense.
- Synthetic examples are always labeled synthetic. Real examples are always cited.

## 9. When in doubt, stop and ask

Uncertainty is a signal, not a failure. If you are unsure whether a source is lawful to read, whether a collection step crosses a line, or whether a finding is safe to publish — stop, document where you stopped and why, and ask someone qualified (a lawyer for legal questions, a senior analyst or your employer for policy questions). Stopping is always the defensible choice. Continuing through doubt is not.

---

**The short version:** public sources first, question first, never transact/contact/test, touch as little as possible, separate fact from assessment, document everything, and only publish what helps a defender. The rest of this repo is implementation detail.
