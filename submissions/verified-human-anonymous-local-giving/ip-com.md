# IP.com Defensive Publication Submission Package — Verified-Human Anonymous Local Gratitude Transfer

This document contains the submission form fields, classification codes, license declaration, and operational flow for submitting paper #1 to the IP.com Prior Art Database.

**Source paper**: [`../../verified-human-anonymous-local-giving.md`](../../verified-human-anonymous-local-giving.md)
**Canonical URL**: <https://thonly.org/research/verified-human-anonymous-local-giving>
**License**: CC0 1.0 Universal (public domain)

IP.com's Prior Art Database is the venue most directly searched by USPTO and EPO patent examiners during examination. Submissions here are explicitly indexed for prior-art discovery; they are the strongest single defense against subsequent patent claims on the disclosed mechanism.

---

## Submission form fields

### Title (longer than arXiv version — examiners search by keyword)

```
Verified-Human Anonymous Local Gratitude Transfer: A Combined Mechanism for Bot-Resistant, Proximity-Bounded, Recipient-Anonymous Digital Payment
```

### Author

```
Thon Ly
HeartBank® (heartbank.net)
Kâmpôt, Cambodia
Contact: research@thonly.org
```

### Disclosure date

```
2 May 2026
```

### Keywords (comma-separated; maximize examiner search-query coverage)

```
defensive publication, prior art, FIDO2, WebAuthn, biometric attestation, proof-of-personhood, proof-of-humanity, anonymous payment, anonymous tipping, gratitude payment, recipient anonymity, proximity attestation, Bluetooth Low Energy, BLE ranging, Ultra-Wideband, UWB ranging, NearbyInteraction, peer-to-peer payment, local payment, hyperlocal commerce, community currency, demurrage, time bank, TimeBanking, LETS, Wörgl, dāna, anonymous giving, almsgiving, bot-resistant, agent-resistant, secure enclave, deepfake resistance, social capital, loneliness epidemic, gratitude economy, dignity infrastructure, smart contract, Base L2, Coinbase, autonomous AI, bodhisattva, Buddhist economics, Theravāda, Tipiṭaka
```

### Abstract / Summary

```
This disclosure describes a digital-payment primitive that combines three structural properties not previously composed in any single mechanism known to the author: (1) per-action biometric attestation that the sender is a human present at the moment of the transfer, implemented via FIDO2/WebAuthn signing gated on local biometric authentication; (2) cryptographic physical-radio proximity attestation that the recipient is within a density-tunable geographic radius of the sender at the moment of the transfer, implemented via Ultra-Wideband (UWB) ranging with Bluetooth Low Energy (BLE) and signed GPS as fallbacks; and (3) recipient-side anonymity, in which the recipient receives the gratitude expression and any attached monetary value but is not informed of the sender's identity, with the verifying party retaining the sender's identity for adversarial-pattern detection and audit purposes only.

The combination is, to the author's knowledge, not previously published as a unified mechanism. Existing systems possess at most two of the three properties: cash has anonymity and proximity but no humanity verification; Worldcoin and similar proof-of-personhood systems verify humanity but not at action time and not with recipient anonymity; contactless payment systems verify proximity but not anonymity or per-action humanity; privacy-preserving cryptocurrencies provide anonymity but not proximity and not humanity verification.

Disclosed mechanism elements include: density-tunable radius derived from public population-density data; three-layer proximity attestation with rejection of GPS-only attestation when UWB or BLE is available; FIDO2 signature verification including the user-presence and user-verified flag bits; per-recipient deterministic pseudonyms allowing relational continuity without identity disclosure; adversarial-pattern detection for collusion, coded-message via amount, stalking, GPS spoofing, and replay; per-jurisdiction configurable thresholds for AML/regulatory compliance.

Use cases include local-business gratitude, conference and event tipping, religious almsgiving (operationalizing the canonically higher form of dāna in the Pāli canon), honoring service workers, cross-cultural travel, and supporting strangers in need.

This document is offered under Creative Commons CC0 1.0 Universal as a defensive publication establishing prior art as of 2 May 2026. The author and HeartBank® expressly disclaim and will not seek patent rights on the specification or any portion thereof in any jurisdiction at any time. Any subsequent patent application claiming the combined mechanism described herein should be considered to be filed against established prior art and should be denied on grounds of obviousness in light of this publication.
```

### Full disclosure text

Upload the **markdown file converted to PDF**:

```bash
cd ~/Desktop/HeartBank®/thonly.org/research
pandoc verified-human-anonymous-local-giving.md \
  --from markdown \
  --to pdf \
  --pdf-engine=xelatex \
  --output verified-human-anonymous-local-giving-ip-com.pdf \
  --variable=geometry:margin=1in \
  --variable=fontsize:11pt
```

The full markdown is already structured exactly as IP.com prefers: explicit prior-art statement, abstract, numbered body sections with detailed mechanism description, system architecture, reference implementation pseudocode, edge-case analysis, use cases, citations.

### Classification codes (USPC / CPC)

When prompted for classification during submission, suggest these codes — they ensure examiners searching adjacent patent territory will find the disclosure:

| Code | Description |
|---|---|
| **G06Q 20/00** | Payment architectures, schemes or protocols |
| **G06Q 20/02** | Payment architectures involving security |
| **G06Q 20/40** | Authorisation, e.g., identification of payer or payee, verification of customer or shop credentials |
| **G06F 21/32** | User authentication using biometric data |
| **H04W 12/06** | Authentication |
| **H04W 4/02** | Services making use of location information |

### License declaration

When prompted for license terms in the IP.com submission form, paste:

```
This disclosure is dedicated to the public domain under Creative Commons CC0 1.0 Universal. The author and HeartBank® will not seek patent on this specification or any portion thereof, in any jurisdiction, at any time. Any party may freely implement, modify, redistribute, or build upon the disclosed mechanism without permission, attribution, or royalty. This disclosure is intended to function as defensive prior art against subsequent patent applications claiming the same or substantially similar mechanism.
```

---

## Practical submission flow

1. Create an account at <https://priorart.ip.com> (or use existing)
2. Initiate a **"Defensive Publication"** submission (different from "Patent Application Disclosure")
3. Pay submission fee (~$155–200 depending on plan)
4. Paste Title, Author, Keywords, and Summary fields above
5. Upload the converted PDF as the full disclosure
6. Select classification codes (the six suggested above)
7. Paste the License declaration in the appropriate field
8. Submit. IP.com indexing typically completes within 24–72 hours.
9. Once an IP.com identifier is assigned (format: `IPCOM00NNNNNNXXNN`), update the Cross-Venue References section in:
   - `../../verified-human-anonymous-local-giving.md` (this repository)
   - `thonly.org/thonly.org/src/pages/research/verified-human-anonymous-local-giving.ts`
   - `heartbank.net/heartbank.net/src/pages/research/verified-human-anonymous-local-giving.ts`

After updating the cross-references, **re-trigger Internet Archive snapshots** of all updated venues so the cross-referenced versions are also archived.

---

## Why IP.com matters most for prior-art purposes

Among the cross-venue redundancy strategy:
- **Internet Archive snapshots** prove the URL existed at a given date but are not actively searched by patent examiners
- **arXiv** is searched by examiners but is biased toward academic abstract structure
- **GitHub** is searched but is biased toward code rather than mechanism disclosure
- **IP.com Prior Art Database** is *built specifically for examiners*, indexed by classification code, searched by default during patent examination

For a defensive publication, IP.com is therefore the venue with the highest expected per-dollar protective value. The ~$155–200 fee is the cheapest patent-blocking insurance available.

---

## Order of operations within the publication wave

A practical sequencing for the multi-venue publication of paper #1:

1. **Day 0** — Deploy thonly.org and heartbank.net (`npm run deploy` in each); make canonical and institutional-mirror URLs live.
2. **Day 0 (immediately after deploy)** — Trigger Internet Archive snapshots manually for both URLs (web.archive.org/save/, archive.today, perma.cc).
3. **Day 0** — Commit and push GitHub repo: `cd ~/Desktop/HeartBank®/thonly.org/research && git add . && git commit -m "publish: verified-human-anonymous-local-giving" && git push`. The GitHub commit timestamp is itself a tamper-evident record.
4. **Day 1–3** — Submit to IP.com (the most consequential prior-art venue for patent-blocking; $155–200; indexed within 72 hours).
5. **Day 1–7** — Submit to arXiv (request endorsement if needed, then submit; moderation 1–3 days).
6. **Once each venue is live** — Edit the Cross-Venue References section in the canonical page, the institutional mirror, and the markdown, with each venue's assigned identifier. Re-trigger Internet Archive snapshots so cross-referenced versions are also archived.

The goal: all five venues (thonly.org, heartbank.net, GitHub, IP.com, arXiv) live within roughly one week, each with independent tamper-evident timestamps falling within the same week. After that, anyone trying to file a patent claiming the same mechanism faces a five-venue prior-art wall dated within days of each other.
