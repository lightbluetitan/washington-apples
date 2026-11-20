# Methodology

This document describes the systematic process used to create the **Washington Apples: A Curated Dataset of Commercial Varieties, Flavor, Crispness, Skin Color, Harvest, and Origins** (`washington_apples.csv` and `washington_apples.xlsx`).

## 1. Data Acquisition

The 37 commercial apple varieties (`WA_APP_001` to `WA_APP_037`)—spanning 13 distinct origins—were compiled and cross-checked across Washington apple reference sources:

* [Washington Apples – All Varieties](https://waapple.org/varieties/all/)
* [WA Grown – Washington's Incredible Long-Lasting Apples](https://www.wagrown.com/blog/apples/item/washingtons-incredible-long-lasting-apples)
* [Borton Fruit – Apples](https://bortonfruit.com/fruit/apples/)

## 2. Data Curation and Normalization

To ensure consistency and technical interoperability, the following criteria were applied:

* **Naming and Standardization:** Variable names and categorical values are standardized in English, while preserving cultivar naming conventions (such as *Piñata* and *Cosmic Crisp*) and origin labels across 13 distinct origins.
* **Header Standardization:** All variable names were defined using `snake_case` (`apple_id`, `variety_name`, `flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, `origin`) for consistent access in R, Python, and SQL.
* **ID and Categorical Formatting:** The `apple_id` field follows the alphanumeric format `WA_APP_001` to `WA_APP_037`, paired with standardized categories for `flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, and `origin`.
* **Completeness and Origin Semantics:** All 37 records contain zero missing values and zero duplicates, with `origin` recording where each cultivar was originally developed or discovered rather than solely where it is grown commercially today.
* **Encoding:** The CSV file was validated with **UTF-8 encoding (confidence = 0.8)** in R using `readr::guess_encoding()` (above `ISO-8859-1` at `0.32` and `ISO-8859-2` at `0.27`), supporting special characters such as `ñ` in *Piñata* across Windows, macOS, and Linux.

## 3. Quality Control (QA)

The final dataset underwent a multi-step validation process:

1. **Completeness Check:** Verified the presence of exactly 37 records (`WA_APP_001` to `WA_APP_037`) across 13 distinct origins.
2. **Schema Validation:** Confirmed 7 character columns (`apple_id`, `variety_name`, `flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, `origin`) across both `.csv` and `.xlsx` formats.
3. **Missing Value and Duplicate Check:** Confirmed zero missing values (`0` nulls) across all 7 columns and zero duplicate records.
4. **Cross-Source Validation:** Cross-checked entries across the Washington apple reference sources.
5. **Encoding Verification:** Tested the CSV file using `readr::guess_encoding()` in R, confirming UTF-8 encoding with `confidence = 0.8` (above `ISO-8859-1` at `0.32` and `ISO-8859-2` at `0.27`).

## 4. Compatibility Testing

Both dataset formats (`washington_apples.csv` and `washington_apples.xlsx`) were imported and verified in R and Python without errors or warnings:

* **R:** Both files imported via `readr::read_csv()` and `readxl::read_excel()`, parsing all 37 rows and 7 character columns (`apple_id`, `variety_name`, `flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, `origin`).
* **Python:** Both files imported via `pandas.read_csv()` and `pandas.read_excel()`, returning `(37, 7)` DataFrames with zero missing values.

## 5. Software and Tools

* **Data Processing:** Spreadsheet / CSV
* **Validation:** R (`readr`, `readxl`) and Python (`pandas`)
* **Documentation:** Markdown and Citation File Format (`CITATION.cff`)
* **Version Control & Archiving:** Git / GitHub (`washington-apples`) and Zenodo