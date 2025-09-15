# Instructions for Finding and Documenting Supplier Resource Mix

This document provides comprehensive, step-by-step instructions for analysts to identify, verify, and document the resource mix for each qualifying supplier-region pair (e.g., from a spreadsheet of utilities/suppliers by country/state). The process is designed for the Granular Registry SSS Reporting platform, aligning with GHG Protocol Scope 2 updates (as of September 13, 2025). Resource mix refers to the composition of a supplier's electricity generation sources in the region, expressed as percentages by fuel type (e.g., coal: 40%, renewables: 30%), including subcategories (e.g., wind vs. solar), associated emissions factors (gCO2e/kWh), and any SSS-specific allocations (e.g., tied to regulated cost recovery). Focus on public data for the most recent years (2023–2025), prioritizing supplier-specific over aggregated data.

Analysts must process one pair at a time, documenting in a standardized template (see Section 6). Aim for >70% coverage of the supplier's regional operations; flag incomplete data. Re-evaluate annually or upon events like regulatory changes (e.g., post-IRA extensions). Allocate 2–4 hours per pair, depending on region.

## 1. Preparation

* **Review Pair Details**: From the spreadsheet, note supplier name, region (e.g., Duke Energy - North Carolina), qualifying SSS categories (from Step 2), and any prior data (e.g., from Step 3 outputs).
* **Define Scope**: Target generation mix (not consumption); include owned/controlled assets and purchased power if allocated to SSS. Exclude non-electricity (e.g., steam unless Scope 2-relevant).
* **Gather Tools**: Use web browsers, PDF readers, and analysis software (e.g., Excel for aggregation, Python/Pandas for modeling if needed). No proprietary tools.
* **Ethical Note**: Rely solely on public sources; do not contact suppliers or access paywalled data without approval.

## 2. Initial Search and Data Identification

* **Step 2.1: Keyword Formulation**: Craft targeted queries, e.g., "\[Supplier] electricity generation mix \[Region] 2025" or "\[Supplier] fuel sources emissions factor \[Year]". Include variants: "resource portfolio", "power supply mix", "integrated resource plan (IRP)".
* **Step 2.2: Primary Source Search**:
  * Start with supplier's website: Navigate to sustainability/ESG reports, IRPs, or investor filings (e.g., search "sustainability report 2025").
  * Check regulatory bodies: E.g., U.S. PUC/FERC for tariffs/IRPs; EU national regulators for disclosures.
* **Step 2.3: Secondary Database Query**:
  * Use global aggregators for context: IEA Data and Statistics (iea.org/data-and-statistics) for country-level mixes; Ember Global Electricity Review 2025 (ember-energy.org/latest-insights/global-electricity-review-2025) for source trends.
  * If supplier-specific unavailable, use as proxy but note limitations.
* **Step 2.4: Explore Alternatives**: If initial searches fail, try semantic variations (e.g., "energy portfolio" for non-U.S.); check news/academic sources for indirect data (e.g., via Google Scholar for studies on supplier mix).

## 3. Regional-Specific Guidance

Adapt searches to regional data ecosystems; prioritize supplier-level where possible.

* **United States**:
  * Primary: EIA Electricity Data Browser (eia.gov/electricity/data/browser/) for plant-level generation; eGRID (epa.gov/egrid) for subregional mixes and emissions (2023 data released 2025).
  * Forms: EIA-860 (annual generator data) and EIA-861 (sales/utility-specific) at eia.gov/electricity/data.php.
  * State PUC sites (e.g., dsireusa.org for RPS ties); EEI Industry Data (eei.org/resources-and-media/industry-data) for aggregates.
  * Verification: Cross-check with Annual Energy Outlook 2025 (eia.gov/outlooks/aeo/).
* **European Union**:
  * Primary: ENTSO-E Transparency Platform (transparency.entsoe.eu) for generation by unit/operator (hourly granularity; export as CSV).
  * Eurostat Energy Balances (ec.europa.eu/eurostat/web/energy/data) for country mixes; AIB for attribute data.
  * National: E.g., Ofgem (U.K.) or BNetzA (Germany) for utility reports.
  * Note: Post-RED III (2025), more granular disclosures expected.
* **China**:
  * Primary: National Energy Administration (nea.gov.cn) for provincial data; CEC (China Electricity Council) reports.
  * Aggregators: IEA China profiles; Ember for trends.
  * Challenges: Less supplier-specific; use state-owned enterprise reports (e.g., State Grid sustainability PDFs).
* **India**:
  * Primary: Central Electricity Authority (cea.nic.in) for monthly reports; POSOCO for grid data.
  * Our World in Data (ourworldindata.org/electricity-mix) for stacked charts; IRENA Country Profiles.
  * State utilities: E.g., DISCOM annual reports.
* **Brazil**:
  * Primary: ANEEL (aneel.gov.br) for generation concessions; ONS (ons.org.br) for system data.
  * EPE (epe.gov.br) for energy planning reports.
* **Australia**:
  * Primary: AEMO (aemo.com.au) for market data; Clean Energy Regulator (cleanenergyregulator.gov.au) for renewables.
  * AER (aer.gov.au) for state reports.
* **Other Regions (e.g., Southeast Asia, Africa)**: Default to IEA/IRENA country profiles; national ministries (e.g., Indonesia's PLN reports). For emerging markets, use World Bank Energy Data (databank.worldbank.org).
* **Global Fallbacks**: Energy Institute Statistical Review (energyinst.org/statistical-review); REN21 GSR 2025 (ren21.net/gsr-2025); RFF Global Energy Outlook (rff.org/publications/reports/global-energy-outlook-2025).

## 4. Data Extraction and Analysis

* **Step 4.1: Extract Raw Data**: Download PDFs/CSVs; parse mixes (e.g., % by fuel). Note units (GWh vs. %).
* **Step 4.2: Calculate if Needed**: If raw generation provided, compute percentages (e.g., coal GWh / total GWh). Use tools like Excel formulas or Python (e.g., df\['percentage'] = (df\['generation'] / df\['generation'].sum()) \* 100).
* **Step 4.3: Link to SSS**: Allocate portions to categories (e.g., RPS-funded renewables under Non-Bypassable Charges).
* **Step 4.4: Emissions Factors**: Derive from mix using standard factors (e.g., IPCC for coal: \~820 gCO2e/kWh); or source from eGRID/IEA.

## 5. Verification and Quality Assurance

* **Multi-Source Cross-Check**: Compare at least three sources (e.g., supplier report vs. EIA vs. IEA). Flag discrepancies >5% (e.g., due to imports).
* **Mathematical Validation**: Verify totals sum to 100%; perform sensitivity analysis (±10% on renewables).
* **Challenge Assumptions**: Assume data is self-reported—check for audits (e.g., search "\[Supplier] mix audit 2025"). Consider improbables: Hidden fossil subsidies skewing mix? Verify via IMF reports.
* **Triple-Verify**: Re-search independently; use alternative methods (e.g., satellite data from Carbon Monitor if ground-truthing needed). Document uncertainties (e.g., "2024 data preliminary; 2025 estimates based on trends").
* **Logical Scrutiny**: Review for biases (e.g., overreported renewables in EU); seek counter-evidence (e.g., NGO critiques like Ember).
* **Final Reconsideration**: After drafting, re-process the pair from Step 2 to confirm no oversights.

## 6. Documentation

Use this template for each pair (e.g., in Excel/Google Sheets):

| Field                     | Description                           | Example                                                                                                               |
| ------------------------- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Supplier                  | Name                                  | Duke Energy                                                                                                           |
| Region                    | State/Country                         | North Carolina                                                                                                        |
| Qualifying SSS Categories | From Step 2                           | Regulated Cost Recovery                                                                                               |
| Resource Mix Breakdown    | Table of % by source (2023–2025 avg.) | Coal: 35%, Gas: 40%, Nuclear: 15%, Renewables: 10% (Wind: 6%, Solar: 4%)                                              |
| Emissions Factor          | Avg. gCO2e/kWh                        | 450 (location-based)                                                                                                  |
| Data Vintage              | Years covered                         | 2023–2024 (2025 projected)                                                                                            |
| Sources                   | List with URLs                        | EIA eGRID (epa.gov/egrid, accessed 09/13/2025); Duke Sustainability Report (duke-energy.com/sustainability, PDF p.45) |
| Uncertainties/Notes       | Gaps, assumptions                     | Excludes imports (10% of mix); Pending IRA impacts may increase renewables by 5% in 2026                              |
| Completeness Score        | % coverage                            | 85% (supplier-specific)                                                                                               |

Compile into a master report; include visuals (e.g., pie charts).

### 7. Risks and Mitigations

* **Risk: Data Unavailability**: Emerging markets lack granularity. _Mitigation_: Use national averages as proxy; flag and recommend advocacy for disclosures.
* **Risk: Inaccuracy/Staleness**: Pre-2025 data may not reflect transitions. _Mitigation_: Prioritize latest reports; average last two years.
* **Risk: Regional Variations**: Definitions differ (e.g., hydro as renewable). _Mitigation_: Standardize per GHG Protocol (include hydro in low-carbon).
* **Risk: Overlaps/Multi-Region Suppliers**: Double-counting if supplier operates multi-state. _Mitigation_: Allocate by regional sales (from EIA-861).
* **Pitfalls Addressed**: Assumed universal access—mitigated by public-only rule. Logical gaps (e.g., ignoring T\&D losses)—adjust via IEA factors (5–15%). Oversights (e.g., biomass classification)—cross-check IPCC guidelines.

This process ensures robust, verifiable resource mix data to support SSS reporting and Scope 2 integrity.
