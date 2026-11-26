# CSIX CCISO v4 — Writing Standard (approved 26 Nov 2026)

This file is the contract for every article in this repo. The approved reference
implementation is `csix-ecsa/en/fundamentals/pentest-methodology.md` (~5,449
words) in the sibling ECSA repo. Read it before writing. Match or exceed its
depth and structure; never copy its sentences or cases.

## Hard format rules

- Pure Markdown, **no front matter**.
- First line is exactly `# <title from topics.json>`. No text before it.
- Last `##` heading is exactly `## See also` (EN) or `## Lihat juga` (ID).
- **4,200–5,500 words** per article. Shorter is a regression.
- No HTML except `<details>` / `<summary>` for answer keys.

## Required content blocks

1. **Learning objectives** — 5–8 measurable outcomes.
2. **Deep explanation** — prose plus **at least 2 tables**; define terms when first used.
3. **ASCII flow diagram** in a fenced code block whenever the topic has a process,
   including decision/stop branches.
4. **At least 2 fictional worked case studies** with context, constraints,
   explicit decisions, and a "what this teaches" lesson. No technical procedure.
5. **Practice by section** — at least 8 scenario questions with answer keys inside
   `<details>` blocks. Rehearse decisions, not vocabulary.
6. **Common mistakes** — a memorable list.
7. **Reusable templates / checklists** — something the reader can copy into notes.
8. **Glossary** — at least 8 terms in plain language.
9. **References and verification** — official and public framework sources with
   "verify current version" caveats.

## Safety and accuracy rules

- Independent, **unofficial** study resource. EC-Council, CCISO, CISSP, CISM and
  other credential names are trademarks of their owners. No affiliation, no
  official courseware, no exam dumps.
- Content is **defensive, governance and leadership education**. No offensive
  procedure, exploit steps, payloads, or evasion.
- The brand used across this site is **CSIX CCISO v4**. EC-Council's current
  materials reference **CCISO v4 / AI-Enhanced** as of 26 Nov 2026. Do not assert
  exam duration, question count, pass mark, price, retake rules, eligibility
  exceptions, CPD figures, or domain weights as fact without a dated official
  source. Vendor statistics are **marketing claims**, not guarantees.
- Education, **not legal, financial, tax, regulatory, or investment advice**.
  Board/risk/finance examples are fictional and illustrative.
- Companion CSIX links MUST use `https://siedysoes.github.io/...` placeholders.
  Never hardcode a GitHub owner.
- Internal relative Markdown link **text** must exactly match a title in
  `topics.json` for the same language; the **path** must be the target article's
  path from `topics.json`.

## Exact article titles

Read `topics.json` for the authoritative list. Never paraphrase a title.

### English

1. What Is CCISO v4
2. The Five Domains: Govern to Strategize
3. CCISO vs CISSP & Other Leader Creds
4. The CISO Role: From Technical to Executive
5. Eligibility: Full CCISO & Associate Path
6. CCISO Exam Format & Blueprint
7. A Practical Study Plan
8. Frameworks & Tools for the Executive
9. Costs, Validity & CPD
10. Board Communication & Executive Presence
11. Risk, Finance & Vendor Governance
12. AI Governance: Reality Check
13. Careers After CCISO

### Bahasa Indonesia

1. Apa Itu CCISO v4
2. Lima Domain: Govern hingga Strategize
3. CCISO vs CISSP & Kredensial Leadership Lain
4. Peran CISO: Dari Teknis ke Eksekutif
5. Syarat: CCISO Penuh & Jalur Associate
6. Format Ujian & Blueprint CCISO
7. Rencana Belajar Praktis
8. Framework & Tool untuk Eksekutif
9. Biaya, Masa Berlaku & CPD
10. Komunikasi Dewan & Executive Presence
11. Risiko, Keuangan & Tata Kelola Vendor
12. Tata Kelola AI: Realita Lapangan
13. Karier Setelah CCISO

## Indonesian articles

- Write natural, professional Bahasa Indonesia — not literal translation.
- First line exactly matches the `id_lang.title` in `topics.json`.
- Final H2 exactly `## Lihat juga`.
- Link text uses the Indonesian titles from `topics.json`.
