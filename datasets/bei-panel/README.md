# BEI panel — sample notes

## Source

Indonesia Stock Exchange (IDX) public financial-statistics endpoint
(`DigitalStatistic/GetApiDataPaginated`, `urlName=LINK_FINANCIAL_DATA_RATIO`),
collected programmatically. No manual transcription.

## How this sample was selected

- 25 tickers chosen for recognisability across sectors (banks, telco, consumer, energy,
  materials, technology).
- One row per ticker: the latest year available at snapshot time (2025).
- All 22 columns retained, unmodified.

The paid panel contains 4,408 rows (2021–2025, all sectors, 975 tickers) plus a codebook
and ready-to-run R/Stata/SPSS syntax.

## Snapshot

- Collected: 2026-11-07
- Source bucket: IDX financial ratio statistics
- Currency: IDR billion for statement figures; percent for ratios

## Known caveats

1. Dominant statement basis is Q3 (30 September), usually unaudited.
2. 2021–2022 ratio values were normalized ×100 from decimal source format and remain
   preliminary.
3. 2025 is a trailing year.
4. `per` and `pbv` are trailing and depend on the share price at snapshot time.
5. Blank cells mean the source did not publish the value — not zero.

Do not use this sample to estimate market-wide statistics: 25 rows cannot represent
975 tickers.
