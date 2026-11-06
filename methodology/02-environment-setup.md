# Environment Setup: Compartmentalization

Compartmentalization is the single most important operational-security practice in threat research. Its purpose is simple: **nothing from the research activity should be able to touch your personal life, your job applications, or your employer's systems — and nothing from those should be able to touch the research.**

This file covers principles and categories. It does not give step-by-step instructions for any specific tool, and it deliberately does not describe how to reach illicit spaces.

## The core rule

**One research environment, separate from everything else.** That means:

- A **dedicated research machine or virtual machine (VM)** used only for threat research. Not your daily laptop. Not the machine you use for job applications, banking, or personal email.
- **Separate identities.** The research environment uses research-only accounts and identifiers. No personal email, no personal social accounts, no real name attached to research browsing profiles unless the work is being published under your real name — and even then, the *accounts* stay separate from personal ones.
- **No personal accounts, ever.** Do not sign in to personal email, personal cloud storage, personal social media, or personal banking from the research environment. A single sign-in can link the research activity to your real identity and to your personal data.
- **Encrypted storage for notes.** Research notes live in encrypted storage on the research environment (for example, an encrypted volume or an encrypted notes application). Notes are the most sensitive thing you produce: they record what you looked at and when. Treat them accordingly.
- **Snapshots and rollback.** Keep the research VM on snapshots so you can roll back to a known-clean state after a session — or after any encounter with suspicious content. If something in the research environment behaves oddly, assume compromise and rebuild from the snapshot rather than investigating on the live system.

## Why a dedicated environment matters

1. **Security.** Illicit spaces are heavily seeded with malicious files, deceptive downloads, and browser exploits. A dedicated VM that can be discarded limits the blast radius to a system that holds nothing personal.
2. **Privacy.** Research browsing is fingerprintable. Keeping it in a separate environment prevents that fingerprint from being associated with your personal identity.
3. **Legal hygiene.** If your research is ever questioned, a clean separation between research activity and personal activity makes it possible to show exactly what was done, where, and with what. A mixed environment makes that impossible.
4. **Professional hygiene.** An employer doing a background check should find published, sanitized work — not a tangle of personal accounts and research browsing in the same browser history.

## What the research environment contains — and what it does not

**It contains:**

- A clean, up-to-date operating system in a VM or on a dedicated machine.
- A browser configured for research: hardened settings, no saved personal credentials, no personal extensions.
- A notes system with encryption, and the blank templates from this repo (`templates/`).
- A reference library of *public* sources: saved threat-intel reports, advisories, and papers — all from legitimate publishers.

**It does NOT contain:**

- Personal files, photos, or documents.
- Credentials for personal accounts.
- Raw research notes from other projects, session artifacts, bookmarks to illicit sources, or anything downloaded from an illicit source.
- Any real stolen or victim data — not even "for reference." There is no research purpose that requires holding real stolen data, and holding it creates legal and ethical exposure with no defensive value.

## Privacy tooling — at the category level

Researchers and journalists legitimately use privacy-focused tooling to read public sources safely — for example, a privacy-focused research operating system run from a dedicated machine, or the Tor network for anonymous reading of public material. These tools are legitimate when used to *read public information safely*. They are not a license to transact, contact actors, or access illicit markets, and this guide does not describe how to use them for any such purpose. If you use privacy tooling, use it for the same reason a journalist does: to keep your reading private, not to hide wrongdoing.

## Session discipline

- **Start clean.** Begin each session from a known-clean snapshot.
- **Work the question.** Open only what the research question requires (see `01-research-principles.md`). Log sources as you go.
- **End clean.** Export only sanitized notes to your write-up workspace. Roll back or snapshot the VM. Do not leave the research browser logged in to anything, and do not leave downloaded material sitting in the environment.
- **Retention and deletion.** Keep research logs and sanitized write-ups; delete everything else on a schedule. Old browsing data, cached files, and downloaded material you no longer need are liability, not assets. Decide the retention period in advance (for example, 90 days for working notes) and stick to it.

## A note on employer and shared machines

Never do threat research on an employer's machine or network without explicit written permission, and never on a shared or family machine. Employer systems are monitored, and research activity on them can create problems for you and for your employer. If you are employed in a security role, your employer's acceptable-use policy and any threat-intel program rules govern — this guide does not override them.

## Checklist: before your first session

- [ ] Dedicated VM or machine, separate from personal use
- [ ] No personal accounts signed in anywhere in the environment
- [ ] Encrypted storage for notes, with the blank templates copied in
- [ ] Browser hardened, no personal credentials saved
- [ ] Snapshot taken of the clean state
- [ ] Retention/deletion schedule decided and written down
- [ ] Employer acceptable-use policy checked (if employed)
