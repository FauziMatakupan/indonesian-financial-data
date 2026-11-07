# Indonesian Financial Panel — IDX/BEI 2021–2025 (Sample)

Open notes and a real sample of the financial-ratio panel for companies listed on the
Indonesia Stock Exchange (IDX/BEI). The full panel covers **4,408 company-year
observations**, **975 tickers**, **11 IDX-IC sectors**, and **22 columns** for 2021–2025.

This repository holds a small, free sample so you can inspect the schema before buying
anything. It is a snapshot, not a live feed.

## The sample

| File | Rows | Content |
|---|---|---|
| [CSV](datasets/bei-panel/sample-2026-11-07.csv) | 25 | One row per well-known ticker, latest year (2025) |

Every row keeps the full 22-column shape used by the paid panel. Values are copied
verbatim from the dataset — decimal places and negative numbers are not rounded.

## Columns

| Column | Meaning |
|---|---|
| `kode_saham` | Ticker code (IDX) |
| `nama_emiten` | Listed company name |
| `sektor`, `subsektor` | IDX-IC classification |
| `tahun` | Fiscal year of the snapshot |
| `fs_date` | Financial-statement date published by the source |
| `audit(U/A)` | `A` audited, `U` unaudited, `LR` limited review |
| `sharia` | Sharia-compliant flag (`S`/`N`) |
| `roa_pct`, `roe_pct`, `npm_pct` | Profitability ratios, percent |
| `der` | Debt-to-equity, times |
| `eps_idr`, `book_value` | Per-share figures, IDR |
| `pbv`, `per` | Valuation multiples, times |
| `assets_miliar_idr` … `profit_attr_owner_miliar_idr` | Statement figures, IDR billion |
| `firm_size_lnassets` | Natural log of total assets |

## Limitations (read before using)

- **Most rows are Q3 (30 September) unaudited**, following what IDX publishes per bucket.
  Do not treat the panel as audited full-year statements.
- **2021–2022 ratios are preliminary.** Those years were normalized ×100 to percent scale
  and have not been fully reconciled against audited reports.
- **2025 is a trailing year** as published at snapshot time.
- **Missing means missing.** Empty cells are values the source did not publish; they are
  never zero.
- **Not investment advice.** The data is descriptive and may contain source errors.

## Related

The complete panel (annual + quarterly + per-sector files, codebook, and R/Stata/SPSS
syntax) is sold as a dataset on Fastwork:
<https://fastwork.id/user/fauzimatakupan/data-analysis-11054397>

**Disclosure:** the sample and this documentation are free; the full panel is paid.
Nothing here is affiliated with or endorsed by IDX.

## License

- Documentation and code: [MIT](LICENSE)
- Data sample: [sample notice](LICENSE-DATA) — rights in the underlying data remain
  with the Indonesia Stock Exchange; provided for schema evaluation only.

Read [ETHICS.md](ETHICS.md) before redistributing.
