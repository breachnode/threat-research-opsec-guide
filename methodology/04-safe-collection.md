# Safe Collection: How to Collect Without Crossing Lines

Collection is where threat research most often goes wrong. The rules here are simple to state and require discipline to follow: **read only, take the minimum, touch nothing live, and stop the moment something feels off.**

## The read-only posture

Threat research collection is **read-only**. You observe and record what public sources publish. You do not:

- Create accounts on illicit platforms or forums.
- Post, comment, reply, or otherwise interact with threat actors or their infrastructure.
- Download files, tools, or datasets from illicit sources.
- Submit credentials, test logins, or probe systems to see if a technique works.
- Click through to infrastructure that a public report links to for the purpose of "verifying" it yourself — the report's verification is sufficient, and your click adds risk without adding evidence.

If a step requires you to *do* something to a live system or a live actor, it is not collection. It is participation, and it is out of scope.

## What to collect — and what not to

**Collect:**

- The text of public reports, advisories, and papers (or links to them — prefer links over local copies when the source is stable).
- Your own notes summarizing what a source says, with a citation and a date.
- Sanitized screenshots of *public* material only — for example, a chart from a vendor report or a diagram from an advisory — with metadata stripped (see below).
- Indicators that are already published in public reporting, with the source cited.

**Do NOT collect:**

- Any real stolen or victim data: card numbers, credentials, personal data, account details — even partial, even "redacted," even "just to check." There is no defensive purpose that requires holding real victim data.
- Screenshots or copies of illicit marketplace listings, forum posts, or actor communications.
- Files downloaded from illicit sources. These are commonly malicious, and downloading them creates both a security risk and a legal problem.
- Anything that could only have come from participating in an illicit transaction.

## Screenshot hygiene

Screenshots are useful for write-ups, but they are also a leak vector. Follow these rules:

1. **Public material only.** Screenshot a vendor report, an advisory, or a news article — never an illicit listing, a forum thread, or a private message.
2. **Strip metadata.** Remove EXIF and other metadata from any image before storing or publishing it. Screenshots can carry timestamps, device information, and location data.
3. **Never capture personal data.** If a screenshot would include a real person's name, email, username, or other personal data, do not take it. If you need the information, summarize it in your own words without the personal data.
4. **Crop to the minimum.** Capture only the part of the screen that supports the finding. Extra context in a screenshot is extra exposure.
5. **Review before publishing.** Look at every image in a write-up as if you were the person in it. If it would embarrass or endanger anyone, cut it.

## Encountering live victim data

Sometimes public reporting links to, or describes, material that contains live victim data. If you encounter it:

1. **Stop.** Do not read further, do not copy it, do not download it.
2. **Do not reproduce it** in notes, screenshots, or write-ups — not even in redacted form.
3. **Note the encounter** in your research log (date, source, and that you stopped upon encountering victim data) and move on.
4. **Report it through proper channels** if appropriate — for example, the FBI's Internet Crime Complaint Center (IC3) for fraud-related material, or the affected organization's abuse contact. Reporting is a defensive act; collecting is not.

## Note-taking hygiene

- Notes live in the encrypted storage of the research environment (`02-environment-setup.md`). They do not live in personal cloud accounts, personal email, or unencrypted files.
- Write notes in your own words. Quoting a public source is fine with a citation; copying large blocks of text from any source is not.
- Separate working notes from publishable write-ups. Working notes may contain half-formed ideas and low-confidence observations. Only sanitized, reviewed write-ups leave the research environment.
- Date every note. Threat reporting ages fast, and an undated note is a liability — it can be mistaken for current intelligence months later.

## Automation and scraping

Do not write scrapers or automated collectors aimed at illicit sources, and do not run automated collection against any site in a way that violates its terms of use. Automated collection against *public, legitimate* sources (for example, polling a vendor's public advisory feed) is acceptable if it respects the source's terms, rate limits, and robots directives — and if the output is stored in the research environment only.

## If something goes wrong

- **You clicked something you should not have:** stop the session, roll back the VM to the last clean snapshot, and note what happened in the research log. Do not try to investigate the mistake on the live system.
- **You downloaded something you should not have:** do not open it. Delete it, roll back the snapshot, and note the incident.
- **You received an unsolicited message from an actor:** do not reply. Record that it happened, block if the platform allows it, and move on. Replying turns an unsolicited contact into an interaction.
- **You are unsure whether a step was lawful:** stop and ask a qualified person (see `legal-boundaries/what-is-legal.md`). Document where you stopped and why.

Mistakes happen. The professional response is to stop, contain, document, and ask — not to push through and hope it works out.
