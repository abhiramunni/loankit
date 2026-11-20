# LoanKit — Borrow Smart. Know the Real Cost.

A single-file web app that shows the true cost of a loan in plain words: EMI, total interest, amortisation, prepayment savings, loan comparison and an affordability check. No backend, no sign-up — everything is saved in your browser's localStorage.

**Live:** https://abhiramunni.github.io/loankit/

## What it does

- **EMI calculator** — amount (₹1L–₹50L), rate (6–18%) and tenure (1–30 years) sliders; one-tap presets for education, home, car and personal loans. EMI, total payable, total interest and debt-free date update live.
- **Where the money goes** — principal-vs-interest donut plus a year-by-year stacked bar chart. Early EMIs are mostly interest; the chart shows the balance flip.
- **Repayment schedule** — yearly amortisation table (EMI paid, principal, interest, balance left), expandable to all years.
- **Prepayment simulator** — extra ₹/month slider (₹0–₹20,000). On the seeded education loan, +₹5,000/month finishes 35 months early and saves ₹2,66,029 in interest.
- **Loan comparison** — three seeded scenarios (education ₹15L @ 9.5% / 10y, car ₹8L @ 9.25% / 5y, personal ₹3L @ 12.5% / 3y) with a lowest-rate badge and interest-per-₹1-lakh for fair comparison. Add your own scenarios, load one into the calculator, or remove any.
- **Affordability gauge** — your EMI as a percentage of in-hand income against the 40% rule banks use, with a plain-words verdict (Comfortable / Tight / Too much).
- **Education-loan spotlight** — moratorium explainer (two quiet years add ~₹3 lakh to a ₹15L loan), interest-subsidy (CSIS) note, an 8-item documents checklist, and indicative lender rate ranges (labelled indicative — confirm with the lender).
- **Six plain-language guides** — EMI maths, reducing vs flat rate, moratorium, prepayment, collateral vs unsecured, hidden fees.
- **Privacy** — copy a plain-words loan summary, remove samples, or erase everything (two-tap). 3-step onboarding tour; 4-second cinematic intro with tap-to-skip (quick on return visits).

## Verified numbers (seeded education loan)

| Loan | EMI | Total interest |
| --- | --- | --- |
| ₹15,00,000 @ 9.5%, 10 yrs | ₹19,410 / mo | ₹8,29,156 |
| ₹8,00,000 @ 9.25%, 5 yrs | ₹16,704 / mo | ₹2,02,235 |
| ₹3,00,000 @ 12.5%, 3 yrs | ₹10,036 / mo | ₹61,299 |
| ₹40,00,000 @ 8.75%, 20 yrs | ₹35,348 / mo | ₹44,83,623 |

Prepayment on the education loan: +₹5,000/month → 85 months (35 early), interest ₹5,63,127, saves ₹2,66,029. +₹2,000/month → 103 months.

## Tech

- One self-contained `index.html` (~980 KB, two embedded AI-generated photos, no build step).
- Fraunces + Inter, warm editorial palette (ivory paper, espresso ink, bronze/amber/terracotta).
- Reducing-balance EMI maths in vanilla JS; canvas chart and SVG donut/gauge; localStorage persistence.
- QA: headless jsdom test suite (`qa-test.js`) — run with `node qa-test.js`.
