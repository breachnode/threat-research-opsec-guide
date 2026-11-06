# Source Hierarchy: Where to Look, in Order

Not all sources are equal. This hierarchy tells you where to look first, and what each kind of source can and cannot prove. Work down the list in order; only go further when the higher sources do not answer the question.

## The hierarchy

### Tier 1 — Government advisories and law-enforcement reporting

**Examples:** CISA advisories and alerts, FBI Internet Crime Complaint Center (IC3) reports and public service announcements, U.S. Secret Service and Europol public advisories.

**What it proves:** authoritative descriptions of observed campaigns, techniques, and recommended mitigations; the closest thing to ground truth in public reporting.

**What it cannot prove:** it is selective — agencies publish what they choose to publish, often months after the fact, and rarely with full technical detail. Absence from an advisory is not evidence a threat does not exist.

**How to use it:** treat it as the baseline. If CISA has published on a technique, that publication is the citation of record for the technique's existence and for the recommended controls.

### Tier 2 — Vendor threat-intelligence reports

**Examples:** published research from major security vendors and threat-intelligence firms (annual threat reports, campaign write-ups, vulnerability research).

**What it proves:** detailed technical analysis, indicators, and campaign timelines, usually with strong sourcing from the vendor's own telemetry.

**What it cannot prove:** vendors have commercial incentives — reports can emphasize threats their products address, and telemetry is limited to what their customers and sensors see. Two vendors describing the same campaign can disagree on scope and attribution.

**How to use it:** cross-check across at least two independent vendors before treating a claim as established. Note the vendor's data source (telemetry, honeypots, customer incidents) and its limits. Prefer reports that publish indicators and methodology over reports that only publish conclusions.

### Tier 3 — Academic research

**Examples:** peer-reviewed papers on fraud, authentication, underground economies, and measurement studies from universities and research institutes.

**What it proves:** rigor — methodology, sample sizes, and limitations are stated explicitly. Measurement studies (for example, large-scale studies of credential-stuffing traffic) are often the best evidence for how common a technique actually is.

**What it cannot prove:** academic work is slow — a paper may describe a landscape that is already a year old. And measurement studies describe what researchers could observe, which is a subset of what exists.

**How to use it:** use academic work for base rates, definitions, and methodology. When a vendor report and an academic paper disagree on prevalence, the academic measurement is usually the better estimate.

### Tier 4 — Breach disclosures and court records

**Examples:** company breach notifications, SEC filings describing incidents, indictments, plea agreements, and trial exhibits that describe fraud operations.

**What it proves:** concrete, verified instances — a named company, a dated incident, a described method, and often a dollar figure. Court records in particular are valuable because the claims in them were tested in an adversarial process.

**What it cannot prove:** disclosures describe one incident, not the landscape. A single breach disclosure does not establish that a technique is common, and companies disclose what the law requires — no more.

**How to use it:** use disclosures as case studies and as anchors for timelines. Never generalize from one disclosure to the whole threat landscape.

### Tier 5 — Reputable security journalism and OSINT

**Examples:** established security news outlets, well-sourced investigative reporting on cybercrime, and published OSINT analysis from known researchers.

**What it proves:** timely coverage of emerging threats, often with primary-source interviews and leaked documents — sometimes the first public record of a new technique.

**What it cannot prove:** journalism is not peer-reviewed and not always technically precise. A headline's claim and the article's actual evidence are often two different things. Single-source reporting should be treated as a lead, not a finding.

**How to use it:** read the article, not the headline. Check whether the article cites primary sources, names its sources' limitations, and links to underlying reports. If it does not, treat it as a pointer to investigate, not as evidence.

### Tier 6 — Primary observation (read-only, last resort)

**What it is:** directly observing publicly accessible threat activity — for example, reading a public report of a phishing kit's structure, or observing a scam website that is already publicly documented.

**What it proves:** very little on its own. An observation without context cannot establish prevalence, attribution, or intent.

**What it cannot prove:** almost everything that matters — and it carries the highest legal, security, and ethical risk of any tier. Primary observation is never the first step, and it is never a substitute for the five tiers above.

**How to use it:** only when the research question cannot be answered from Tiers 1–5, only in a read-only posture, and only within the rules in `04-safe-collection.md` and the red lines in `legal-boundaries/red-lines.md`. If you find yourself doing primary observation regularly, your research question is probably too broad — narrow it.

## Evaluating any single source

Before citing a source, run it through these checks:

| Check | Question to ask |
|---|---|
| **Provenance** | Who produced this, and how did they get their information? |
| **Recency** | When was it published, and is the data still current? Threat reporting ages fast — a 2023 report on phishing kits is history, not current intelligence. |
| **Corroboration** | Does at least one independent source say the same thing? A single-source claim is a lead, not a finding. |
| **Method** | Does the source explain how it reached its conclusions? "Our telemetry shows" without numbers is weaker than a report with sample sizes and time windows. |
| **Bias** | What does the source gain from this claim? A vendor selling a product, a journalist chasing a scoop, and an agency justifying a budget all have incentives. |
| **Scope** | Does the source claim more than its evidence supports? "Attackers are using X" is different from "we observed X in 12 incidents over 6 months." |

## Confidence ratings

Every finding in a write-up carries a confidence rating based on the sources behind it:

- **High:** corroborated by Tier 1 or Tier 2 sources, or by two independent sources at any tier, with methodology stated.
- **Medium:** supported by a single credible source, or by multiple lower-tier sources that agree.
- **Low:** single lower-tier source, uncorroborated, or based on an inference from the evidence rather than direct evidence. Low-confidence findings are still worth recording — but they must be labeled low, and they must not drive recommendations on their own.

A finding with no source is not a finding. Cut it or label it clearly as an analyst's hypothesis, not as fact.

## What this hierarchy deliberately excludes

- **Illicit marketplaces and forums.** They are not sources for this methodology. No marketplace names, links, or handles appear in this repo, and no finding should rest on material taken from them.
- **Leaked or stolen datasets.** A dataset of stolen credentials is not a source — it is victim data. Reading, downloading, or analyzing it is out of scope for defensive research.
- **Anonymous claims without provenance.** "Someone on the internet said" is not evidence, no matter how confident the claim sounds.
