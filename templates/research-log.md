# Research Log — Template

Copy this file for each research session. Fill it in **during** the session, not from memory afterward. Store completed logs in the encrypted notes storage of the research environment — never in personal cloud accounts or unencrypted files.

---

## Session

- **Date:**
- **Researcher:**
- **Research question:** *(one sentence — what are you trying to answer?)*
- **Session goal:** *(what would a successful session produce?)*

## Sources consulted

| # | Source (publisher / title) | Date published | Tier (see 03-source-hierarchy.md) | What it contributed |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

## Findings

- **Finding 1:** *(one sentence)*
  - Evidence:
  - Confidence: High / Medium / Low
  - Defensive implication:
- **Finding 2:**
  - Evidence:
  - Confidence: High / Medium / Low
  - Defensive implication:

## Dead ends and exclusions

*(Sources that did not help, claims you could not verify, material you deliberately excluded and why — for example, "stopped upon encountering victim data, did not collect.")*

-

## Incidents / boundary notes

*(Anything unexpected: a wrong click, an unsolicited message, a source whose legality was unclear, a step you stopped. If nothing happened, write "None.")*

- None

## Next steps

-

## Confidence summary

- **Overall confidence in this session's findings:** High / Medium / Low
- **What would raise confidence:** *(e.g., a second independent source, a newer advisory)*

---

## Filled example (SYNTHETIC — illustrative only, not observed data)

### Session

- **Date:** 2026-11-05
- **Researcher:** B. Harris
- **Research question:** What indicators do public sources associate with credential-stuffing campaigns against small e-commerce login pages?
- **Session goal:** A short list of defender-visible indicators with at least two public sources behind each.

### Sources consulted

| # | Source (publisher / title) | Date published | Tier | What it contributed |
|---|---|---|---|---|
| 1 | CISA advisory (SYNTHETIC citation — illustrative) | 2026-09-14 | Tier 1 | Recommended mitigations for credential stuffing; rate limiting and MFA emphasis |
| 2 | Vendor threat report (SYNTHETIC citation — illustrative) | 2026-10-02 | Tier 2 | Observed indicator patterns: high failed-login rates from distributed sources |
| 3 | Academic measurement study (SYNTHETIC citation — illustrative) | 2025-06-01 | Tier 3 | Base-rate context on how common credential stuffing is against login endpoints |

### Findings

- **Finding 1:** Credential-stuffing campaigns against e-commerce login pages show bursts of failed logins from many sources in a short window.
  - Evidence: Vendor report (source 2) describes distributed failed-login bursts; CISA advisory (source 1) lists the same pattern among its detection guidance.
  - Confidence: High
  - Defensive implication: Alert on failed-login velocity per account and per source; enforce MFA on login.
- **Finding 2:** Attackers in these campaigns commonly use previously breached credential pairs rather than guessing passwords.
  - Evidence: Academic study (source 3) measured reuse of breached pairs; vendor report (source 2) corroborates.
  - Confidence: Medium
  - Defensive implication: Monitor breach-notification feeds for your user base; force password resets where a breach matches a customer email.

### Dead ends and exclusions

- One news article repeated a vendor claim without a source; excluded as evidence, kept only as a pointer.

### Incidents / boundary notes

- None

### Next steps

- Look for a second Tier 1 or Tier 2 source confirming Finding 2 before using it in a write-up.

### Confidence summary

- **Overall confidence in this session's findings:** Medium
- **What would raise confidence:** A second independent source for Finding 2.
