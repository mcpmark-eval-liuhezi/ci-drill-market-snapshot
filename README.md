# CI Drill — Market Snapshot

Quarterly on-call drill repository. Public by design so the on-call channel can open it without logging in.

| | |
|---|---|
| **Repo** | `mcpmark-eval-liuhezi/ci-drill-market-snapshot` |
| **Drill date** | 2026-10-25 |
| **Part 1** | Stuck-job drill — manual-trigger soak workflow, trigger → cancel → verify |
| **Part 2** | Market snapshot — Apple (AAPL) & NVIDIA (NVDA) |
| **Part 3** | Model note — most-downloaded FinBERT on Hugging Face |

---

## Part 1 — Stuck-job drill (completed)

`.github/workflows/soak.yml` is a manual-trigger-**only** workflow (`on: workflow_dispatch`, never on push). Its single job (`soak`) idles for ~30 minutes (`sleep 1800`) to simulate a hung deploy.

| Field | Value |
|---|---|
| Workflow | `Soak - Hung Deploy Simulation` (`.github/workflows/soak.yml`) |
| Trigger used | `workflow_dispatch` (manual) — 2026-10-25 05:30 UTC |
| Cancelled at | 2026-10-25 05:31 UTC |
| **Run id** | **40165764358** |
| **Final conclusion reported by GitHub** | **cancelled** |
| Left running / queued | Nothing — the single job (`soak`) is `completed` with conclusion `cancelled` |

---

## Part 2 — Market snapshot

*Data pulled 2026-10-25 (Yahoo Finance). Analyst actions cover the trailing 12 months.*

### Apple (AAPL)

#### Corporate profile
| | |
|---|---|
| **Official website** | https://www.apple.com |
| **Headquarters city** | **Cupertino, California** (One Apple Park Way, Cupertino, CA 95014, United States) |
| Sector / Industry | Technology / Consumer Electronics |

#### Analyst upgrades & downgrades — trailing 12 months
**Most recent action:** **MoffettNathanson (2026-10-20)** — maintained **Neutral**, price target cut **$304 → $283**. Direction: rating unchanged, target lowered.

| Date | Firm | Direction | Rating change | Price target |
|---|---|---|---|---|
| 2026-10-20 | MoffettNathanson | Maintained | Neutral → Neutral | $304 → $283 (cut) |
| 2026-10-20 | Loop Capital | **Downgrade** | Buy → Hold | $370 → $330 (cut) |
| 2026-10-12 | JP Morgan | Maintained | Overweight → Overweight | $340 → $360 (raise) |
| 2026-10-01 | Morgan Stanley | Maintained | Overweight → Overweight | $360 → $355 (cut) |
| 2026-10-01 | Needham | Reiterated | Hold → Hold | — |
| 2026-09-23 | B of A Securities | Reiterated | Buy → Buy | $370 (maintained) |
| 2026-09-18 | Evercore ISI Group | Maintained | Outperform → Outperform | $365 → $380 (raise) |
| 2026-09-10 | TD Cowen | Reiterated | Buy → Buy | $400 (maintained) |
| 2026-09-10 | Rosenblatt | Maintained | Neutral → Neutral | $303 (maintained) |
| 2026-09-08 | HSBC | Reiterated | Buy → Buy | $366 (maintained) |
| 2026-09-02 | DA Davidson | Maintained | Neutral → Neutral | $270 (maintained) |
| 2026-08-17 | Rothschild & Co | **Upgrade** | Neutral → Buy | $260 → $400 (raise) |
| 2026-08-10 | Jefferies | **Downgrade** | Hold → Underperform | $285.56 → $263.66 (cut) |
| 2026-08-04 | China Renaissance | **Downgrade** | Buy → Hold | $280 (new target) |
| 2026-07-31 | Wells Fargo | Maintained | Overweight → Overweight | $310 → $350 (raise) |
| 2026-07-31 | Barclays | Maintained | Underweight → Underweight | $253 → $245 (cut) |
| 2026-07-31 | Goldman Sachs | Maintained | Buy → Buy | $370 → $360 (cut) |
| 2026-07-30 | Baird | Maintained | Outperform → Outperform | $330 (maintained) |
| 2026-07-30 | Argus Research | Maintained | Buy → Buy | $375 (maintained) |
| 2026-07-15 | Bernstein | Maintained | Buy → Buy | $350 (maintained) |
| 2026-07-14 | Keybanc | **Downgrade** | Sector Weight → Underweight | $250 (new target) |
| 2026-07-13 | Citigroup | Maintained | Buy → Buy | $315 → $365 (raise) |
| 2026-06-25 | Wedbush | Maintained | Outperform → Outperform | $400 (maintained) |
| 2026-06-22 | KGI Securities | **Downgrade** | Outperform → Hold | $315 (new target) |
| 2026-06-09 | Maxim Group | Maintained | Buy → Buy | $310 → $350 (raise) |
| 2026-05-14 | Tigress Financial | Maintained | Strong Buy → Strong Buy | $305 → $375 (raise) |
| 2026-05-01 | UBS | Maintained | Neutral → Neutral | $287 → $296 (raise) |
| 2026-04-17 | BNP Paribas | **Upgrade** | Neutral → Outperform | $300 (new target) |
| 2025-12-05 | CLSA | Maintained | Outperform → Outperform | $265 → $330 (raise) |

Tally: 2 upgrades (Rothschild & Co, BNP Paribas) and 5 downgrades (Loop Capital, Jefferies, China Renaissance, Keybanc, KGI Securities) in the window.

#### Latest annual income statement — FY2025 (fiscal year ended 2025-09-30)
| Line item | Value (USD millions) |
|---|---:|
| **Total Revenue** | **416,161** |
| Cost of Revenue | 220,960 |
| Gross Profit | 195,201 |
| Research & Development | 34,550 |
| Selling, General & Administration | 27,601 |
| Operating Income | 133,050 |
| Pre-Tax Income | 132,729 |
| Tax Provision | 20,719 |
| **Net Income** | **112,010** |
| Diluted EPS | $7.46 |

#### Biggest institutional holders (top 10, reported 2026-06-30)
| Holder | Shares | % held | Value |
|---|---:|---:|---:|
| BlackRock Inc. | 1,162,996,939 | 7.97% | $404.40B |
| Vanguard Capital Management LLC | 959,107,911 | 6.57% | $333.51B |
| State Street Corporation | 615,129,929 | 4.21% | $213.90B |
| Geode Capital Management, LLC | 371,336,543 | 2.54% | $129.12B |
| Vanguard Portfolio Management LLC | 334,119,156 | 2.29% | $116.18B |
| FMR, LLC (Fidelity) | 325,348,754 | 2.23% | $113.13B |
| Morgan Stanley | 242,614,238 | 1.66% | $84.36B |
| JPMorgan Chase & Co. | 228,762,008 | 1.57% | $79.55B |
| Berkshire Hathaway, Inc. | 227,917,808 | 1.56% | $79.25B |
| Norges Bank | 190,726,866 | 1.31% | $66.32B |

*Institutions hold ~66.3% of shares outstanding.*

---

### NVIDIA (NVDA)

#### Corporate profile
| | |
|---|---|
| **Official website** | https://www.nvidia.com |
| **Headquarters city** | **Santa Clara, California** (2788 San Tomas Expressway, Santa Clara, CA 95051, United States) |
| Sector / Industry | Technology / Semiconductors |

#### Analyst upgrades & downgrades — trailing 12 months
**Most recent action:** **Needham (2026-10-22)** — reiterated **Buy**, price target held at **$300**. Direction: no change (steady hand).

| Date | Firm | Direction | Rating change | Price target |
|---|---|---|---|---|
| 2026-10-22 | Needham | Reiterated | Buy → Buy | $300 (maintained) |
| 2026-10-01 | Cantor Fitzgerald | Reiterated | Overweight → Overweight | $350 (maintained) |
| 2026-09-29 | Rosenblatt | Maintained | Buy → Buy | $390 (maintained) |
| 2026-09-10 | Piper Sandler | **Initiated** | — → Overweight | $300 |
| 2026-08-27 | Citigroup | Maintained | Buy → Buy | $300 → $315 (raise) |
| 2026-08-27 | Mizuho | Maintained | Outperform → Outperform | $300 → $315 (raise) |
| 2026-08-27 | JP Morgan | Maintained | Overweight → Overweight | $280 → $320 (raise) |
| 2026-08-27 | Bernstein | Maintained | Outperform → Outperform | $315 → $400 (raise) |
| 2026-08-27 | RBC Capital | Maintained | Outperform → Outperform | $300 → $330 (raise) |
| 2026-08-27 | UBS | Maintained | Buy → Buy | $280 → $300 (raise) |
| 2026-08-27 | Oppenheimer | Maintained | Outperform → Outperform | $265 → $315 (raise) |
| 2026-08-27 | Morgan Stanley | Maintained | Overweight → Overweight | $288 → $300 (raise) |
| 2026-08-27 | Wedbush | Maintained | Outperform → Outperform | $330 → $345 (raise) |
| 2026-08-27 | DA Davidson | Maintained | Buy → Buy | $300 (maintained) |
| 2026-08-27 | Benchmark | Reiterated | Buy → Buy | $335 (maintained) |
| 2026-08-27 | Truist Securities | Maintained | Buy → Buy | $307 → $346 (raise) |
| 2026-08-27 | Evercore ISI Group | Maintained | Outperform → Outperform | $413 → $465 (raise) |
| 2026-08-27 | Keybanc | Reiterated | Overweight → Overweight | $330 (maintained) |
| 2026-08-27 | Raymond James | Maintained | Strong Buy → Strong Buy | $352 → $515 (raise) |
| 2026-08-21 | BMO Capital | **Initiated** | — → Outperform | $340 |
| 2026-08-11 | Wells Fargo | Reiterated | Overweight → Overweight | $315 (maintained) |
| 2026-06-05 | China Renaissance | **Initiated** | — → Buy | $319 |
| 2026-05-27 | Tigress Financial | Maintained | Strong Buy → Strong Buy | $360 → $425 (raise) |
| 2026-05-21 | Stifel | Maintained | Buy → Buy | $250 → $282 (raise) |
| 2026-05-21 | Jefferies | Maintained | Buy → Buy | $275 → $300 (raise) |
| 2026-05-21 | B of A Securities | Maintained | Buy → Buy | $320 → $350 (raise) |
| 2026-05-21 | Baird | Maintained | Outperform → Outperform | $300 → $500 (raise) |
| 2026-05-19 | HSBC | Maintained | Buy → Buy | $295 → $325 (raise) |
| 2026-05-15 | TD Cowen | Maintained | Buy → Buy | $235 → $275 (raise) |
| 2025-11-20 | Barclays | Maintained | Overweight → Overweight | $240 → $275 (raise) |
| 2025-11-20 | Susquehanna | Maintained | Positive → Positive | $230 → $250 (raise) |
| 2025-11-20 | Argus Research | Reiterated | Buy → Buy | $220 (maintained) |
| 2025-11-20 | Melius Research | Maintained | Buy → Buy | $300 → $320 (raise) |
| 2025-11-20 | Deutsche Bank | Maintained | Hold → Hold | $180 → $215 (raise) |
| 2025-11-03 | Goldman Sachs | Maintained | Buy → Buy | $210 → $240 (raise) |
| 2025-11-03 | Loop Capital | Maintained | Buy → Buy | $250 → $350 (raise) |

Tally: 0 upgrades and 0 downgrades in the window — every action was a maintenance, reiteration, or fresh initiation (3 initiations: Piper Sandler, BMO Capital, China Renaissance).

#### Latest annual income statement — FY2026 (fiscal year ended 2026-01-31)
| Line item | Value (USD millions) |
|---|---:|
| **Total Revenue** | **215,938** |
| Cost of Revenue | 62,475 |
| Gross Profit | 153,463 |
| Research & Development | 18,497 |
| Selling, General & Administration | 4,579 |
| Operating Income | 130,387 |
| Pre-Tax Income | 141,450 |
| Tax Provision | 21,383 |
| **Net Income** | **120,067** |
| Diluted EPS | $4.90 |

#### Biggest institutional holders (top 10, reported 2026-06-30)
| Holder | Shares | % held | Value |
|---|---:|---:|---:|
| BlackRock Inc. | 1,941,918,386 | 8.06% | $409.67B |
| Vanguard Capital Management LLC | 1,540,816,358 | 6.39% | $325.05B |
| FMR, LLC (Fidelity) | 1,026,051,548 | 4.26% | $216.46B |
| State Street Corporation | 1,009,783,437 | 4.19% | $213.02B |
| Geode Capital Management, LLC | 606,216,492 | 2.52% | $127.89B |
| Vanguard Portfolio Management LLC | 517,816,949 | 2.15% | $109.24B |
| JPMorgan Chase & Co. | 449,404,578 | 1.86% | $94.81B |
| Price (T. Rowe) Associates Inc | 369,829,781 | 1.53% | $78.02B |
| Morgan Stanley | 356,420,089 | 1.48% | $75.19B |
| Invesco Ltd. | 329,593,488 | 1.37% | $69.53B |

*Institutions hold ~71.4% of shares outstanding.*

---

## Part 3 — Model note: FinBERT

Most-downloaded FinBERT model on Hugging Face:

| | |
|---|---|
| **Repo id** | **`ProsusAI/finbert`** |
| **Downloads** | **125.2M** |
| **Likes** | **1,290** |
| Task | Text classification (financial sentiment: positive / negative / neutral) |
| Architecture | BERT base with a sequence classification head (109.5M params) |
| License | CC BY-NC-SA 4.0 |
| Link | https://hf.co/ProsusAI/finbert |

**From the model card:** "FinBERT is a pre-trained NLP model to analyze sentiment of financial text."

---

*Sources: Yahoo Finance (analyst actions, annual income statements, institutional holders, corporate profiles) and Hugging Face (model search & model card), retrieved 2026-10-25.*
