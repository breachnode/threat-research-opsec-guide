# Threat-Research OPSEC & OSINT Methodology Guide

**Author:** Barry Harris — Greensboro, NC — bhar856@wgu.edu — [linkedin.com/in/barryha](https://www.linkedin.com/in/barryha)

**Background:** CompTIA CySA+ (Apr 2025), CompTIA PenTest+ (Jun 2025), CompTIA Security+ (Jul 2024), Google Cybersecurity Certificate (Mar 2025), ISC2 Certified in Cybersecurity (Mar 2025). Currently pursuing a BS in Cybersecurity and Information Assurance at Western Governors University (May 2023–Present).

## What this is

A methodology guide for investigating fraud and dark-web threats safely and legally — how to set up a compartmentalized research environment, how to collect open-source intelligence on threat activity without crossing legal or ethical lines, and how to handle and document findings responsibly.

The one-line version: **dark-web threat intelligence research — studying how carding, fraud, and identity-theft operations work so organizations can detect, prevent, and respond to them.**

This guide is about the *discipline* of researching threats, not about accessing illicit spaces. It will not tell you how to reach illicit markets, how to transact with threat actors, or how to carry out an attack. If that is what you are looking for, this is the wrong repo.

## Who it is for

- **Junior threat-intelligence, SOC, and fraud analysts** who need a governed way to learn about adversary methods.
- **Hiring managers** evaluating how a researcher works — this guide is deliberately written so a reader can judge the author's judgment, not just their curiosity.
- **Small-business owners and defenders** who want to understand the threat landscape well enough to defend against it.

## How to use this guide

1. **Start with `methodology/01-research-principles.md`.** The principles are the whole game; the rest of the repo is those principles applied.
2. **Set up the environment before you collect anything** (`methodology/02-environment-setup.md`). Compartmentalization is not optional.
3. **Collect from public sources in the order given** (`methodology/03-source-hierarchy.md`), and collect safely (`methodology/04-safe-collection.md`).
4. **Write findings for defenders** (`methodology/05-writeup-standards.md`), using the blank templates in `templates/`.
5. **Know the red lines** (`legal-boundaries/red-lines.md`) — and stop the moment you approach one.

## Scope and limits

- This guide covers **research methodology only**: environment setup, source evaluation, safe collection, and defensive write-ups.
- It does **not** cover penetration testing, vulnerability exploitation, incident response, or malware analysis. Those are separate disciplines with their own rules.
- It contains **no operational detail for wrongdoing**: no instructions for committing fraud, no instructions for reaching or using illicit markets, no marketplace names or links, no vendor handles, and no real stolen or victim data of any kind.
- All examples in this repo are either **synthetic (labeled as such)** or drawn from **public threat-intelligence reporting, law-enforcement advisories, or academic research**, with the source cited.

## Disclaimer

This material is **defensive threat-intelligence research**. All examples are synthetic or drawn from public reporting, and nothing in this repository is intended to enable wrongdoing. The legal-boundaries section is **general information, not legal advice** — the author is not a lawyer. Laws vary by jurisdiction and change over time; consult a qualified attorney before undertaking any research activity you are unsure about. If anything in this guide conflicts with your employer's policies or applicable law, the law and your employer's policies win.

## Repository structure

```
threat-research-opsec-guide/
├── README.md                        # This file
├── methodology/
│   ├── 01-research-principles.md    # The principles that govern everything else
│   ├── 02-environment-setup.md      # Compartmentalization: dedicated research setup
│   ├── 03-source-hierarchy.md       # Where to look, in order, and what each source proves
│   ├── 04-safe-collection.md        # How to collect safely: read-only, no interaction
│   └── 05-writeup-standards.md      # How to write findings for defenders
├── legal-boundaries/
│   ├── what-is-legal.md             # General principles (not legal advice)
│   └── red-lines.md                 # Hard red lines — never cross these
├── templates/
│   ├── research-log.md              # Blank session log template
│   └── finding-writeup.md           # Blank sanitized finding template
└── resources.md                     # Public resources for further reading
```

## The interview question this repo answers

Employers ask: *"How do you do this research?"* The honest answer this repo is built around:

> "Public threat-intelligence reporting, law-enforcement advisories, and academic research, plus a sandboxed research environment for reading public sources safely. I don't transact, I don't contact actors, and I don't handle stolen data."

Everything in this guide exists to make that answer true — and provable.
