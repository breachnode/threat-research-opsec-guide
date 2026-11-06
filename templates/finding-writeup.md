# Finding Write-up — Template

Use this template for every finding that leaves the research environment. One finding per file. A finding that cannot fill every section is not ready to publish.

---

## Title

*(Short, descriptive, defender-facing. Example: "Credential-stuffing bursts against e-commerce login pages.")*

## What

*(What the threat or technique is, in one or two plain sentences.)*

## Evidence

*(What public sources say about it, with full citations. Facts only — no assessment in this section.)*

-
-

## Assessment

*(What it means, labeled as assessment. Include your reasoning and a confidence rating: High / Medium / Low.)*

**Confidence:**

## So what — defensive implication

*(Why a defender should care: who is targeted, what the impact is, how it fits into a larger campaign.)*

## Defensive action

*(The controls, detections, or process changes that address it. At least one is required. Be specific enough to act on.)*

-
-

## Sources

*(Full citations: publisher, title, publication date, link to the public original.)*

-
-

## Review checklist

- [ ] Every factual claim is cited to a public source
- [ ] Every assessment is labeled, with a confidence rating and visible reasoning
- [ ] All examples are labeled synthetic, or cited to public reporting
- [ ] No real personal data, marketplace names, links, handles, or operational detail
- [ ] Every behavior described has a paired defensive action
- [ ] Tone is neutral and professional throughout
- [ ] Would survive a hiring manager, a background investigator, and a compliance reviewer reading it

---

## Filled example (SYNTHETIC — illustrative only, not observed data)

### Title

Credential-stuffing bursts against small e-commerce login pages

### What

Credential stuffing is the automated use of previously breached username-and-password pairs to attempt logins at scale. Against small e-commerce sites it typically appears as a burst of failed logins from many distributed sources over a short window.

### Evidence

- CISA advisory (SYNTHETIC citation — illustrative, 2026-09-14) lists distributed failed-login bursts among the detection indicators for credential-stuffing campaigns and recommends rate limiting and multi-factor authentication.
- Vendor threat report (SYNTHETIC citation — illustrative, 2026-10-02) describes the same burst pattern observed across e-commerce login endpoints, with failed-login rates well above baseline during campaign windows.

### Assessment

**Confidence: High.** Two independent sources at different tiers describe the same observable pattern, and the pattern is consistent with the known mechanics of credential stuffing (automated reuse of breached pairs).

The burst pattern is a reliable early indicator because it is visible in ordinary login logs — a defender does not need specialized tooling to see it, only a baseline for normal failed-login rates.

### So what — defensive implication

Small e-commerce merchants are attractive targets because they often lack MFA and rate limiting, and because a compromised customer account can be used for fraudulent purchases, stored-payment abuse, and further credential harvesting. A successful stuffing campaign against a small merchant can produce account takeovers before the merchant notices, because the merchant is not watching failed-login velocity.

### Defensive action

- **Alert on failed-login velocity:** alert when failed logins for a single account exceed an illustrative starting threshold (for example, 5 failures in 10 minutes), and when total failed logins across the site exceed baseline by an illustrative factor (for example, 3× the 7-day average). Thresholds are starting points — tune to your volume.
- **Enforce MFA** on customer accounts, at minimum for accounts with stored payment methods.
- **Rate-limit login attempts** per source and per account, with progressive delays rather than hard lockouts (which attackers can exploit for denial of service).
- **Monitor breach-notification feeds** for your customer base and force password resets where a breach matches a customer email.
- **Log and retain** failed-login data for at least 90 days so a campaign can be recognized in retrospect even if it was missed live.

### Sources

- CISA advisory (SYNTHETIC citation — illustrative). Published 2026-09-14. Link: *[public advisory URL would go here]*.
- Vendor threat report (SYNTHETIC citation — illustrative). Published 2026-10-02. Link: *[public report URL would go here]*.

### Review checklist

- [x] Every factual claim is cited to a public source
- [x] Every assessment is labeled, with a confidence rating and visible reasoning
- [x] All examples are labeled synthetic, or cited to public reporting
- [x] No real personal data, marketplace names, links, handles, or operational detail
- [x] Every behavior described has a paired defensive action
- [x] Tone is neutral and professional throughout
- [x] Would survive a hiring manager, a background investigator, and a compliance reviewer reading it
