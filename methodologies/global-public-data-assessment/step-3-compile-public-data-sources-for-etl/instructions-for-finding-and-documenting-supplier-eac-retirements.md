# Instructions for Finding and Documenting Supplier EAC Retirements

This document provides comprehensive, step-by-step instructions for analysts to identify, verify, and document Energy Attribute Certificate (EAC) retirements for each qualifying supplier-region pair (e.g., from a spreadsheet of utilities/suppliers by country/state). The process is designed for the Granular Registry SSS Reporting platform, aligning with GHG Protocol Scope 2 updates (as of September 13, 2025). EAC retirements refer to the formal cancellation or redemption of certificates (e.g., RECs in the U.S., GOs in the EU, I-RECs globally) that convey renewable energy attributes, thereby preventing double claiming. Focus on supplier-specific retirements tied to SSS categories (e.g., for RPS compliance under Non-Bypassable Charges), including volume (MWh), type (e.g., solar REC), retirement date, vintage year, and public claims/audits. Prioritize public data for the most recent years (2023–2025), emphasizing granular details like hourly matching where available (e.g., post-2025 updates in systems like PJM-GATS).

Analysts must process one pair at a time, documenting in a standardized template (see Section 6). Aim for >70% coverage of the supplier's regional EAC activities; flag incomplete data (e.g., aggregated only). Re-evaluate annually or upon events like policy shifts (e.g., RE100 2025 requirements for mandatory EAC cancellation in common markets). Allocate 3–5 hours per pair, depending on region.

## 1. Preparation

* **Review Pair Details**: From the spreadsheet, note supplier name, region (e.g., EDF - France), qualifying SSS categories (from Step 2), and related data (e.g., resource mix from prior steps for linkage).
* **Define Scope**: Target retirements associated with the supplier's generation or procurement in the region; include bundled/unbundled EACs. Exclude non-retired (active) certificates or non-electricity attributes (e.g., carbon credits unless Scope 2-linked).
* **Gather Tools**: Use web browsers, PDF readers, and analysis software (e.g., Excel for aggregation, Python/Pandas for trend analysis if needed). No proprietary tools; focus on open registries.
* **Ethical Note**: Rely solely on public sources; do not contact suppliers, registries, or access restricted data. Note RE100 2025 updates requiring cancellation for claims in mature markets.

## 2. Initial Search and Data Identification

* **Step 2.1: Keyword Formulation**: Craft targeted queries, e.g., "\[Supplier] EAC retirements \[Region] 2025" or "\[Supplier] REC cancellation report \[Year]". Include variants: "GO redemption", "I-REC retirement statistics", "RPS compliance filings".
* **Step 2.2: Primary Source Search**:
  * Start with supplier's website: Navigate to sustainability/ESG reports, compliance disclosures, or investor sections (e.g., search "EAC retirement summary 2025").
  * Check regulatory bodies: E.g., U.S. state PUCs for RPS reports; EU national energy agencies for GO data.
* **Step 2.3: Secondary Database Query**:
  * Use global aggregators for context: RE100 Reporting Guidance 2025 (there100.org/sites/re100/files/2025-06/2025%20RE100%20reporting%20guidance%20%28June%20update%29.pdf) for EAC criteria; I-TRACK Foundation statistics (trackingstandard.org/resource/2025-i-rece-market-statistics-january-2025/) for I-REC overviews.
  * If supplier-specific unavailable, use as proxy but note limitations (e.g., aggregate market data from Ember or IEA).
* **Step 2.4: Explore Alternatives**: If initial searches fail, try semantic variations (e.g., "attribute certificate redemption" for non-U.S.); check news/NGO sources for indirect data (e.g., via S\&P Global or EcoHZ blogs on 2025 market updates).

## 3. Regional-Specific Guidance

Adapt searches to regional EAC ecosystems; prioritize supplier-level retirements where possible. Note 2025 updates: e.g., RE100 mandates cancellation in common markets; China prohibits I-REC mutual recognition post-NEA policy.

* **United States**:
  * Primary: EPA Status and Trends Report 2025 (epa.gov/system/files/documents/2025-01/status\_and\_trends\_report\_us\_energy\_attribute\_tracking\_systems.pdf) for aggregated retirements; regional registries like M-RETS (mrets.org/public-reports) for REC data (hourly tracking ready by 2025).
  * Systems: PJM-GATS (gats.pjm-eis.com) for hourly RECs (tradable since August 2024); NAR (nar.recstrack.com); WREGIS (wregis.org); ERCOT (18-month hourly process ongoing); others via EPA tracking list (epa.gov/green-power-markets/energy-attribute-tracking-systems).
  * RPS Compliance: DSIRE (dsireusa.org) for state filings; EEI data (eei.org/resources-and-media/industry-data).
  * Verification: Cross-check with CRS reports (resource-solutions.org); note ZECs for nuclear (e.g., emission-free EACs).
* **European Union**:
  * Primary: AIB National Datasheets (aib-net.org/facts/national-datasheets-gos-and-disclosure) for GO retirements by country; ENTSO-E Transparency Platform (transparency.entsoe.eu) for attribute data.
  * Registries: AIB Hub (aib-net.org) for cross-border; national (e.g., TGE Register in Poland at tge.pl/guarantee-of-origin-register; Ofgem in U.K. for REGOs).
  * Updates: EN 16325:2025 standard (cencenelec.eu/news-events/news/2025/eninthespotlight/2025-08-14\_en16325\_energyorigin/); CA-RES Task Force (ca-res.eu/highlights/task-force-guarantees-of-origin) for directive impacts.
  * Note: Post-RED III (2025), enhanced granularity; RE100 excludes U.K. from EU boundary but allows vintage-aligned EACs.
* **China**:
  * Primary: NEA (nea.gov.cn) for GEC (Green Electricity Certificates) retirements; I-TRACK Foundation (trackingstandard.org) for historical I-REC data (mutual recognition prohibited post-2024 NEA policy).
  * Challenges: Limited public supplier-specific; use aggregated stats (trackingstandard.org/china-introduces-new-eac-policy/); CEC reports for trends.
  * Note: Issuance restricted to 2024 vintage for pre-2025 requests; focus on GECs for domestic claims.
* **India**:
  * Primary: REC Registry India (recregistryindia.nic.in) for REC retirements; CEA (cea.nic.in) for compliance reports.
  * Aggregators: IRENA profiles; RECCPEDIA (reccessary.com/en/reccpedia/i-rec) for I-REC overlaps.
  * Note: Growing I-REC adoption; check POSOCO for grid-linked data.
* **Brazil**:
  * Primary: ANEEL (aneel.gov.br) for REC-like certificates; EPE (epe.gov.br) for energy reports.
  * Global Fallback: I-TRACK/Evident Registry (evident.app) for I-REC retirements.
* **Australia**:
  * Primary: Clean Energy Regulator (cleanenergyregulator.gov.au) for LGC/REC retirements; AEMO (aemo.com.au) for market data.
  * AER (aer.gov.au) for state disclosures.
* **Other Regions (e.g., Southeast Asia, Africa)**: Default to I-TRACK Foundation (trackingstandard.org) and Evident Registry (evident.app) for I-REC data; national ministries (e.g., PLN in Indonesia). For emerging markets, use World Kinect (world-kinect.com/blog/buyers-guide-energy-attribute-certificates-eacs) or Climate Impact Partners (climateimpact.com/business-solutions/energy-attribute-certificates-eacs/) summaries.
* **Global Fallbacks**: RECS Public Info (recs.org/public-information/); S\&P Global reports (spglobal.com/commodity-insights/en/news-research/latest-news/energy-transition/091724-us-rec-tracking-systems-inch-towards-hourly-trading); Ember Global Review 2025 (ember-energy.org/latest-insights/global-electricity-review-2025/); EPA EACs (epa.gov/green-power-markets/energy-attribute-certificates-eacs).

## 4. Data Extraction and Analysis

* **Step 4.1: Extract Raw Data**: Download PDFs/CSVs; parse retirements (e.g., MWh by type/vintage). Note reasons (e.g., compliance vs. voluntary per EPA 2025 report).
* **Step 4.2: Calculate if Needed**: Compute coverage ratios (e.g., retired EACs / renewable generation from resource mix); use tools like Excel or Python (e.g., df\['ratio'] = df\['retired'] / df\['generation']).
* **Step 4.3: Link to SSS**: Tie retirements to categories (e.g., RPS-linked under Non-Bypassable Charges).
* **Step 4.4: Assess Claims**: Check for audits (e.g., RE100 validations); note 2025 RE100 requirements for cancellation starting 2027 disclosures.

## 5. Verification and Quality Assurance

* **Multi-Source Cross-Check**: Compare at least three sources (e.g., registry data vs. supplier report vs. RE100 guidance). Flag discrepancies >10% (e.g., due to vintage mismatches).
* **Mathematical Validation**: Verify totals (e.g., retired MWh ≤ generated); perform sensitivity analysis (±15% on volumes).
* **Challenge Assumptions**: Assume data is comprehensive—probe for underreporting (e.g., search "\[Supplier] EAC controversy 2025"). Consider improbables: Hidden double-claiming? Verify via NGO critiques (e.g., Montel or S\&P). Account for policy shifts (e.g., China's I-REC ban).
* **Triple-Verify**: Re-search independently; use alternative methods (e.g., aggregate stats from IEA vs. supplier-specific). Document uncertainties (e.g., "Aggregated only; no hourly data pre-2025").
* **Logical Scrutiny**: Review for biases (e.g., overclaimed renewables in EU); seek counter-evidence (e.g., EcoHZ blogs). Confirm alignment with GHG Protocol (e.g., no re-issuance per NEA).
* **Final Reconsideration**: After drafting, re-process the pair from Step 2 to confirm no oversights.

## 6. Documentation

Use this template for each pair (e.g., in Excel/Google Sheets):

| Field                     | Description                                   | Example                                                                                                                                                                                                |
| ------------------------- | --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Supplier                  | Name                                          | EDF                                                                                                                                                                                                    |
| Region                    | State/Country                                 | France                                                                                                                                                                                                 |
| Qualifying SSS Categories | From Step 2                                   | Customer Funding                                                                                                                                                                                       |
| EAC Retirements Breakdown | Table of MWh by type/vintage (2023–2025 avg.) | GO: 500,000 MWh (Solar: 300,000, 2024 vintage)                                                                                                                                                         |
| Coverage Ratio            | Retired / Renewables (%)                      | 95%                                                                                                                                                                                                    |
| Data Vintage              | Years covered                                 | 2023–2024 (2025 partial)                                                                                                                                                                               |
| Sources                   | List with URLs                                | AIB Datasheets (aib-net.org/facts/national-datasheets-gos-and-disclosure, accessed 09/13/2025); EDF ESG Report (edf.fr/en/the-edf-group/dedicated-sections/investors-analysts/esg-documents, PDF p.67) |
| Uncertainties/Notes       | Gaps, assumptions                             | Limited to voluntary retirements; Pending RED III impacts may require hourly by 2026                                                                                                                   |
| Completeness Score        | % coverage                                    | 80% (supplier-specific)                                                                                                                                                                                |

Compile into a master report; include visuals (e.g., bar charts of retirements by type).

## 7. Risks and Mitigations

* **Risk: Data Unavailability**: Emerging markets lack public retirements. _Mitigation_: Use I-TRACK aggregates as proxy; flag and advocate for transparency (e.g., via RE100).
* **Risk: Inaccuracy/Staleness**: Pre-2025 data may ignore updates (e.g., hourly in U.S.). _Mitigation_: Prioritize 2025 reports; average recent vintages.
* **Risk: Regional Variations**: Systems differ (e.g., no mutual recognition in China). _Mitigation_: Standardize per RE100 criteria; note exclusions.
* **Risk: Double-Claiming**: Unaudited data. _Mitigation_: Cross-check audits; use Evident Registry for chain-of-custody.
* **Pitfalls Addressed**: Assumed universal access—mitigated by public-only rule. Logical gaps (e.g., ignoring vintage rules)—adjust via RE100 guidance (±1 year allowance). Oversights (e.g., non-EAC instruments)—include via EPA definitions.
