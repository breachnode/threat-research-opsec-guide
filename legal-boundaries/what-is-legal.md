# What Is Legal: General Principles

> **This page is general information, not legal advice. The author is not a lawyer. Laws vary by jurisdiction, change over time, and apply differently to different facts. Consult a qualified attorney before undertaking any research activity you are unsure about. If anything here conflicts with applicable law or your employer's policies, the law and your employer's policies win.**

## The basic distinction

Threat research is lawful when it stays on the right side of a simple line: **reading and analyzing information that is already public is research; accessing systems or data without authorization, committing fraud, or handling stolen data is not research — it is a crime, regardless of intent.**

A defensive purpose does not make an unlawful act lawful. "I was only researching" is not a defense to unauthorized access, fraud, or possession of stolen data.

## What is generally lawful

- **Reading public reporting.** Vendor threat-intelligence reports, government advisories, academic papers, security journalism, and breach disclosures are published for the public. Reading them, citing them, and analyzing them is lawful.
- **Analyzing your own data.** Logs, alerts, and traffic from systems you own or are authorized to administer are yours to analyze.
- **Studying techniques at a conceptual level.** Learning *about* how an attack works — from public sources — in order to defend against it is the core of threat intelligence.
- **Writing and publishing defensive analysis.** Findings, indicators, and control recommendations based on public sources are lawful to publish, subject to defamation law and to any confidentiality obligations you owe an employer.

## What is generally not lawful

- **Unauthorized access.** Accessing a computer system, network, or account without authorization — including guessing or testing credentials, exploiting a vulnerability to gain entry, or using someone else's access — is unlawful in most jurisdictions (in the United States, see the Computer Fraud and Abuse Act, 18 U.S.C. § 1030). It does not matter that you "only looked" or that you meant no harm.
- **Fraud.** Creating fake accounts to test fraud techniques, submitting false payment information, or conducting transactions designed to test whether a fraud method works is fraud — even in a "test" context, and even if no money is ultimately taken.
- **Handling stolen data.** Downloading, possessing, analyzing, or distributing stolen credentials, card data, or personal information is unlawful in many jurisdictions, even if you did not steal it yourself. "I found it in a public place" does not make stolen data lawful to hold.
- **Impersonation and deception.** Pretending to be someone else to gain access to information or systems, or creating false identities to interact with threat actors, can violate fraud, identity-theft, and computer-access laws.
- **Interfering with systems.** Denial-of-service testing, aggressive scanning, or any action that degrades a system you do not own is unlawful regardless of intent.

## Gray areas — treat as red lines until a lawyer says otherwise

Some activities sit in a gray area: reading a publicly accessible page that was not meant to be public, viewing material that is publicly linked but not published, or collecting information from sources whose legality is unclear. The methodology in this repo treats gray areas as **out of scope**. If a source's legality is unclear, do not use it — the public tiers in `methodology/03-source-hierarchy.md` will answer the question another way.

Other gray areas to be aware of:

- **Terms of service.** Violating a website's terms of service is generally a civil matter, not a criminal one, but it can still lead to account bans, legal demands, and reputational harm. Do not assume a terms violation is consequence-free.
- **Copyright.** Quoting short excerpts of public reports with attribution is generally fair use; copying large portions is not. Cite and link; do not republish whole documents.
- **Export controls and sanctions.** Some security information is subject to export controls or sanctions rules. This rarely affects reading public reporting, but it can affect sharing technical material with certain persons or countries. If your work involves cross-border sharing, check the rules.
- **Employer policy.** Your employer's acceptable-use and security policies are binding on you while employed. A research method this guide permits may still be prohibited by your employer. Employer policy wins.

## Jurisdiction matters

This guide is written from a United States perspective. Other countries have different computer-crime, privacy, and data-handling laws — some stricter, some differently structured. If you live, work, or publish in another jurisdiction, learn its rules before researching. In particular, European data-protection law (GDPR) imposes strict rules on handling personal data, including data that appears in public sources.

## When to get legal advice

Get advice from a qualified attorney — before acting — if:

- You are unsure whether a source is lawful to read or use.
- A research step would involve accessing anything that is not clearly public.
- You have encountered material you think may be stolen data or evidence of a crime.
- An employer, a platform, or a government agency has contacted you about your research.
- You are considering publishing anything that names a real person or organization in connection with wrongdoing.

A short consultation with a lawyer is cheap compared to the cost of a legal problem. "I read a methodology guide" is not a substitute for legal advice.

## The practical rule

If you cannot explain, in one sentence, why a research step is lawful and whose authorization covers it, do not take the step. Lawful research is explainable research.
