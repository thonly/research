# arXiv Submission Package — Verified-Human Anonymous Local Gratitude Transfer

This document contains the submission form fields, conversion notes, and operational flow for submitting paper #1 to arXiv as a defensive-publication preprint.

**Source paper**: [`../../verified-human-anonymous-local-giving.md`](../../verified-human-anonymous-local-giving.md)
**Canonical URL**: <https://thonly.org/research/verified-human-anonymous-local-giving>
**License**: CC0 1.0 Universal (public domain)

---

## Submission form fields

### Title

```
Verified-Human Anonymous Local Gratitude Transfer: A Defensive Publication
```

### Authors

```
Thon Ly (HeartBank®)
```

If arXiv requires an institutional email for endorsement, use a `thonly.org` or `heartbank.net` address. arXiv requires endorsement for first-time submitters in `cs.CR` — request endorsement through the arXiv "endorsement request" form citing this paper's defensive-publication purpose; alignment-research or cryptography colleagues can serve as endorsers.

### Primary category

```
cs.CR  (Cryptography and Security)
```

### Cross-list categories

```
cs.CY  (Computers and Society)
cs.HC  (Human-Computer Interaction)
```

### Abstract (1,892 characters, plain text)

Copy the block below directly into the abstract field. No markdown, no italics — Unicode (including Pāli diacritics) is fine.

```
We specify a digital-payment primitive in which a sender expresses gratitude (with optional monetary attachment) to a recipient who is physically nearby in real space, with two structurally novel properties operating in combination: (1) verified-human attestation at the moment of the action, achieved via FIDO2/WebAuthn biometric-gated cryptographic signing, ensuring that the sender is a human present at the moment of the action rather than a bot or automated process; and (2) physical-radio proximity attestation via Bluetooth Low Energy or Ultra-Wideband ranging, ensuring that the recipient is geographically nearby within a density-tunable radius. These two attestations are then composed with (3) recipient-side anonymity: the recipient receives the thank-you and any monetary value but is not informed of the sender's identity. The resulting primitive is, to the authors' knowledge, not previously published as a unified mechanism. Properties include the structural restoration of cash's local-circulation property to digital money, the operational feasibility of anonymous giving (dāna) at scale, the rebuilding of local-economic social capital eroded by globalized digital payment platforms, and a category of bot-resistant gratitude infrastructure suited to an age of pervasive autonomous agents. We provide system architecture, reference implementation patterns, edge-case and adversarial analysis, use cases, and citations to prior art across digital payments, proof-of-personhood, community currencies, and Buddhist economic traditions. This document is offered under CC0 1.0 Universal as a defensive publication establishing prior art; the author and HeartBank will not seek patent on this specification or any portion thereof.
```

### Comments field

```
13 sections, 12 references. Defensive publication; CC0 1.0 Universal (public domain). Canonical version at https://thonly.org/research/verified-human-anonymous-local-giving with mirrors at heartbank.net and github.com/thonly/research.
```

### License selection

On the arXiv submission form, select: **`CC0: Creative Commons Public Domain Declaration`**

This is the most permissive license arXiv offers and matches the defensive-publication intent. arXiv will display "CC0 1.0 Universal" alongside the paper.

---

## Converting the paper to LaTeX/PDF for upload

The source paper exists in markdown (`../../verified-human-anonymous-local-giving.md`). Two routes to arXiv-acceptable form:

### Route A (recommended) — pandoc to LaTeX

```bash
cd ~/Desktop/HeartBank®/thonly.org/research
pandoc verified-human-anonymous-local-giving.md \
  --from markdown \
  --to latex \
  --standalone \
  --output verified-human-anonymous-local-giving.tex \
  --metadata title="Verified-Human Anonymous Local Gratitude Transfer: A Defensive Publication" \
  --metadata author="Thon Ly" \
  --metadata date="2026-05-02"
```

Verify it compiles locally before submitting:

```bash
pdflatex verified-human-anonymous-local-giving.tex
```

Submit the `.tex` file plus any auxiliary files (no figures in this paper, so the `.tex` alone suffices).

### Route B — direct PDF

If LaTeX conversion produces issues (Unicode handling, table rendering), generate a PDF directly:

```bash
pandoc verified-human-anonymous-local-giving.md \
  --from markdown \
  --to pdf \
  --pdf-engine=xelatex \
  --output verified-human-anonymous-local-giving.pdf
```

arXiv accepts PDFs but prefers LaTeX. PDF is acceptable here given the defensive-publication purpose; reviewer scrutiny is lower than for research papers.

---

## Practical submission flow

1. Get an arXiv account if not already; log in at <https://arxiv.org>
2. **Request endorsement** for `cs.CR` if first-time submission in this category (arXiv's endorsement system; takes 1–7 days)
3. Start a new submission; select primary category `cs.CR`, cross-list `cs.CY` and `cs.HC`
4. Paste the abstract above into the abstract field
5. Upload the `.tex` (or PDF) file
6. Set license to **CC0**
7. Paste the Comments text above into the Comments field
8. Submit. arXiv moderation typically takes 1–3 business days for a clearly-formatted preprint.
9. Once an arXiv identifier is assigned (format `arXiv:2605.NNNNN` or similar), update the Cross-Venue References section in:
   - `../../verified-human-anonymous-local-giving.md` (this repository)
   - `thonly.org/thonly.org/src/pages/research/verified-human-anonymous-local-giving.ts`
   - `heartbank.net/heartbank.net/src/pages/research/verified-human-anonymous-local-giving.ts`

After updating the cross-references, **re-trigger Internet Archive snapshots** of all updated venues so the cross-referenced versions are also archived.

---

## Notes

- **Endorsement timing**: if you don't already have an arXiv submission history in `cs.CR`, the endorsement step adds 1–7 days. Plan to start the endorsement request before you intend to submit.
- **First-submission moderation**: first papers in a category sometimes get held for moderator review (1–3 extra days). Defensive publications with clear structure usually pass without issue.
- **Title length**: arXiv has no hard title length limit but very long titles render badly in listings. The title above is 73 characters, comfortably within the practical limit.
- **No DOI required**: arXiv issues its own identifier; you do not need a separate DOI before submission.
