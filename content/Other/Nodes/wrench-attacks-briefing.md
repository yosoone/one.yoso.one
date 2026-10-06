---
publish: true
permalink: /Other/Nodes/wrench-attacks-briefing.md
created: 2026-06-17T19:01:55.000Z
modified: 2026-10-06T05:52:34.394Z
published: 2026-10-06T05:52:34.394Z
---

# Wrench Attacks: Physical Coercion in the Crypto Era

_A sourced briefing on real cases, the traceability paradox, and the role of trusted institutions in security. Figures current as of mid-2026._

---

## What a “wrench attack” is

A wrench attack is a physical-world crime in which attackers use force or the threat of force to compel a crypto holder to surrender access — by revealing a seed phrase or private key, unlocking a device, or authorizing a transfer themselves. It targets the _person_, not the technology. The name comes from a webcomic joke: regardless of how strong the encryption is, an attacker can simply threaten someone with a wrench until they hand over the password.

The key insight is that cryptographic security is irrelevant once the human is the attack surface.

---

## The traceability paradox

Blockchain’s defining feature — a public, permanent, transparent ledger — is also what makes holders into targets. Anyone can see a wallet’s balance. The danger materializes when that wallet gets linked to a real identity and location, via:

- **Leaked KYC data** from exchanges (breaches expose customer names and home addresses)
- **Public address reuse** (donation addresses, human-readable name services, tip jars)
- **Doxxing and social media** (boasting about gains, posting balances, flexing purchases)

A second structural factor makes crypto uniquely attractive to violent criminals: unlike a bank account, a self-custodied wallet can provide _immediate, irreversible_ access to large transferable value with no institutional approval required. Once stolen, the funds are gone.

---

## The scale (2024 → 2026)

|Period                |Confirmed incidents|Losses|
|----------------------|-------------------|------|
|2024                  |41                 |—     |
|2025                  |72 (+75% YoY)      |$40M+ |
|First 4 months of 2026|rising sharply     |$101M+|

- Kidnapping was the most common tactic in 2025 (25 incidents, up 66% from 2024).
- **Europe accounts for over 40% of global incidents.** France leads, with roughly one crypto-related kidnapping every two to three days at the peak.
- 2026 losses in the first four months alone nearly doubled the _entire_ 2025 total.
- A notable evolution in 2026: **proxy targeting** — attackers going after relatives and elderly family members rather than the primary holder.

---

## Documented case studies

**David & Amandine Balland — Ledger co-founder (France, January 2025)**
With grim irony, the target was a co-founder of a hardware-wallet company. An organized group abducted the couple, held them at separate locations, and tortured them over roughly 48 hours — including severing one of Balland’s fingers — to extract a multi-million-euro ransom. The victims were freed and ten suspects were taken into custody.

**Paymium executive’s family (Paris, May 2025)**
A failed daylight kidnapping attempt targeted the daughter and grandson of a prominent crypto CEO in Paris’s 11th arrondissement.

**Italian tourist (New York, 2025)**
Criminals faced charges of kidnapping, assault, torture, and unlawful imprisonment for an effort to steal a tourist’s Bitcoin worth millions.

**Roman & Anna Novak (Dubai, October 2025) — fatal**
A couple was lured to a fake investor meeting near the Oman border, then kidnapped in an attempt to force access to funds including cryptocurrency. The case became one of the most widely cited wrench attacks with fatal consequences.

**Yong Wang (Istanbul, January 2026) — fatal**
A Chinese entrepreneur was abducted on arrival in Turkey in a case tied to a crypto-asset dispute; funds were extracted before he was killed. Ten suspects were later arrested in China following an Interpol Red Notice.

**Nancy Guthrie (US, January 2026) — proxy targeting**
The 84-year-old mother of journalist Savannah Guthrie was kidnapped as part of a \$6 million Bitcoin ransom demand — a clear example of attackers targeting relatives rather than the holder.

**Tennessee home-invasion ring (US, indicted May 2026)**
A federal grand jury indicted three men over a series of violent home invasions targeting crypto holders across California, with over \$6.5 million in digital assets stolen. Charges included conspiracy to commit robbery and kidnapping.

---

## Countermeasures

Effective defense works on three layers. The technical layer only matters _after_ an attacker has already found you, so the identity layer is the most important and most neglected.

### 1. Identity & exposure (first line of defense)

- Don’t self-identify as a holder; avoid boasting, balance screenshots, or visible crypto-funded spending.
- Break the on-chain ↔ identity link: use fresh addresses, avoid identity-linked name services, never publicly post a wallet holding meaningful funds.
- Assume any exchange holding your ID will eventually leak it.
- Reduce physical exposure: scrub data-broker sites, don’t geotag, guard your home address.
- Treat unsolicited high-value “investor meetings” as a red flag (the fatal Novak case began this way).

### 2. Technical countermeasures (protect you _during_ an attack)

- **Multisignature wallets** — funds require multiple keys held in different places/people, so a single coerced person genuinely cannot move them. (“If an attacker holds you in London but your second key sits in Zurich, the maths doesn’t work in their favour.”)
- **Duress / decoy wallets** — a sacrificial small balance to hand over, with the bulk hidden behind a second passphrase (plausible deniability).
- **Panic PINs** — entering a duress code triggers transfers to a safe address.
- **Geographic / social key-sharding** — splitting a key (Shamir’s Secret Sharing) so no single moment exposes everything.
- **Time-locks and spending limits** — funds can’t move until a delay elapses, removing the point of holding someone hostage.

### 3. Operational security (behavioral layer)

- Compartmentalize spending vs. savings wallets.
- Physical security basics; don’t keep seed phrases or hardware wallets openly accessible.
- Specialized kidnap-and-ransom (K\&R) insurance now exists for crypto holders.

---

## How “trusted institutions” provide security

The protection institutions offer is not better vaults — it is **removing the victim’s ability to comply under duress.** You cannot be coerced into instantly surrendering what you cannot instantly access.

**They raise the attacker’s cost above the payoff.** The governing principle, as one custody executive framed it, is to make the cost of an attack rise exponentially — when it costs $3 million to steal $10 million, the incentive collapses. Third-party custody achieves this by adding time-locks and layers of approval, and by shifting the target from a vulnerable individual to the custodian’s staff.

**The historical analogy is exact.** Self-custody recreates the problem of treasure hoarders throughout history: they were vulnerable to physical attack until they could share that risk with a stronger institution. Robbing a bank is far harder than robbing a person.

**Real holders are already migrating.** One protocol founder moved his holdings out of on-chain self-custody and into physical vaults at four separate institutions, splitting funds across them. Each withdrawal requires a physical signature and a seven-day lock period — accessing the full sum takes a month. He declined to be named, citing kidnapping risk, combining institutional custody _with_ anonymity.

**The market shift is measurable.** Custodians report a growing preference shift from self-custody to institutional control. One executive-security firm went from inquiries about once a quarter to about once a week. Analysts expect the trend to accelerate institutional custody adoption while suppressing the “be your own bank” narrative.

**Regulation is clearing the path.** In January 2025, US regulators rescinded SAB 121, the guidance that had discouraged banks from offering crypto custody — opening the door for traditional financial institutions to enter the custody market.

---

## The honest limitation

Institutional custody is not a clean fix — the same executives who recommend it concede it is “not an optimal solution.” Custody reintroduces exactly what crypto set out to abolish: counterparty risk (FTX-style collapse), surveillance, and a centralized honeypot. It does not end violence; it relocates the target to the custodian’s employees.

The deeper irony is structural: a movement built to escape gatekeepers is being pushed back toward them — not by regulation this time, but by violence. The most security-conscious holders now layer all three defenses — institutional custody, time-locks, and anonymity — which is effectively an admission that “be your own bank” failed as a complete security model.

As one security researcher asked: if Bitcoin is the “Internet of money,” what does it say that it cannot be safely stored on an Internet-connected computer?

---

## Sources

- CertiK, _Skynet Wrench Attacks Report_ (via BeInCrypto, CoinDesk, Moneywise, HOKANEWS)
- TRM Labs, _The Rise of Wrench Attacks and Crypto-related Violent Crime_
- Cointelegraph, _Why wrench attacks are becoming one of the most violent forms of crypto crime_ and _Wrench attacks drive crypto investors to centralized custodians_
- BlackCloak, _Wrench Attacks: How Old Tactics Still Threaten Crypto Owners_
- WTW and Solace Global risk reports (via TheStreet)
- MEXC News, _Crypto Wrench Attacks Drive Executive Security Spending_
- DSHR’s Blog / Nicholas Weaver commentary
- Medium (0NE-CLAVI), _Self-Custody vs. Custodial Wallets: The Complete 2026 Guide_
- CryptoAdventure, _Crypto Wrench Attacks Explained_
- Cryptonews.net and CoinAlertNews case reporting

_This briefing summarizes reporting from the above sources. Figures are as reported and may be revised as investigations conclude._
