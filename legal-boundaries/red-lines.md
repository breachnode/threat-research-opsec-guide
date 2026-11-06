# Red Lines

These are hard lines. They are not guidelines, they are not "best practices," and there is no exception for curiosity, for a deadline, or for "just this once." If a research step would cross one of these lines, stop.

## 1. No transactions

Do not buy, sell, trade, or exchange anything with threat actors. Do not pay for data, samples, tools, or access — in any currency, including cryptocurrency. Do not accept payment from a threat actor for any reason. A transaction turns a researcher into a participant, and it creates a financial record linking you to illicit activity.

## 2. No contact with actors

Do not message, email, call, or otherwise communicate with threat actors — not to ask questions, not to verify a claim, not to warn them, not "just to see what happens." Do not reply to unsolicited messages from actors. Contact is interaction, and interaction is participation.

## 3. No downloading stolen data

Do not download, possess, store, or analyze stolen credentials, card data, personal information, or any dataset that contains victim data — even partial, even "redacted," even "for research." There is no defensive purpose that requires holding real stolen data. Public reporting and synthetic examples cover every legitimate research need.

## 4. No testing fraud techniques against live systems

Do not test card-testing, credential stuffing, account-takeover, or any other fraud technique against any live system — not a target's system, not a merchant's system, not a "test" account on a production service, not your own production system. Testing belongs in a lab you own, against systems you own, with synthetic data. If you cannot build that lab, you cannot do that test.

## 5. No unauthorized access

Do not access any system, network, account, or dataset without authorization. Do not guess or test credentials. Do not exploit a vulnerability to gain entry. Do not use someone else's access, session, or credentials — even if they were offered to you. "The door was open" is not authorization.

## 6. No creating accounts on illicit platforms

Do not create accounts on illicit marketplaces, forums, or messaging channels used primarily for wrongdoing — not to observe, not to "lurk," not to verify a public report. Account creation is participation, and it creates a record of your presence. If a public report is insufficient, the answer is to narrow the research question, not to join the platform.

## 7. No impersonation

Do not pretend to be someone you are not — not a customer, not a victim, not another researcher, not law enforcement — in order to gain information or access. Impersonation is deception, and it can violate fraud and identity laws independently of anything else you do.

## 8. No handling of real victim data — ever

Restated because it is the line most often rationalized: if material contains real personal data belonging to a real victim, do not read it, copy it, store it, or reproduce it — not even in part, not even "anonymized" by you. If you encounter it, stop, note the encounter in your research log, and report it through proper channels if appropriate (see `methodology/04-safe-collection.md`). Your redaction of victim data does not make it yours to hold.

## 9. No paying for access or information

Do not pay for subscriptions, memberships, or "premium" access to illicit sources. Do not pay a source for information. Payment is a transaction (see line 1) and it funds the activity you are researching.

## 10. No operational detail in write-ups

Do not publish instructions, walkthroughs, tool configurations, or step-by-step detail that would enable someone to commit wrongdoing — even if you learned it from a public source. Describe what a technique *looks like to a defender* and what stops it. The moment a write-up tells a reader *how to do it*, it has crossed from threat intelligence into enablement.

## If a line is crossed

Lines get crossed by accident — a wrong click, a misleading link, an unexpected download. The response is always the same:

1. **Stop immediately.** Do not continue the session.
2. **Contain.** Roll back the research VM to the last clean snapshot. Delete anything that should not have been collected. Do not open it, do not inspect it further.
3. **Document.** Record what happened in the research log: what you did, how it happened, what you did to contain it. Honest documentation is what separates an accident from a cover-up.
4. **Disclose if required.** If the incident involves a legal or policy obligation — for example, if you work for an employer with an incident-reporting policy, or if you believe a crime may have been committed — disclose it to the appropriate party. When in doubt, ask a lawyer.
5. **Learn from it.** Change the method so it cannot happen the same way again, and write the change down.

## The test

Before any research step, ask: **"Could I describe this step, in full, to a hiring manager, a background investigator, and a lawyer — and would all three be comfortable with it?"** If the answer is no, or if you are not sure, do not take the step.
