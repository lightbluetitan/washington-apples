# Washington Apples: A Curated Dataset of Commercial Varieties, Flavor, Crispness, Skin Color, Harvest, and Origins

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24405374.svg)](https://doi.org/10.5281/zenodo.24405374)

## Description

This **curated dataset** provides a structured and verified reference of **37 commercial apple varieties** marketed in Washington State (`WA_APP_001` to `WA_APP_037`), documenting their variety name, flavor profile, crispness level, skin color, harvest window, and geographic origin.

This resource is the result of a systematic process of **research, curation, and standardization**. It consolidates commercial apple variety records into a clean tabular format suitable for horticulture, agriculture, food and sensory analysis, and data science workflows.

A core value of this curated collection is its **consistency and completeness**: all 37 records and 7 variables are completely populated with zero missing values and zero duplicate entries, while preserving cultivar naming conventions (such as *Piñata* and *Cosmic Crisp*) and origin designations across 13 distinct origins.

The purpose of this resource is to serve as a **clean, reliable reference table** for researchers, educators, and data practitioners working with Washington apple varieties across R, Python, and other analytical environments.

## Language and Encoding

To ensure maximum technical compatibility and international reach, this dataset follows these standards:
1. **English Metadata and Values:** All variable names (column headers) are in English using `snake_case` (`apple_id`, `variety_name`, `flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, `origin`), and categorical data values are standardized in English.
2. **Data Integrity:** The dataset contains 37 rows (`WA_APP_001` to `WA_APP_037`) and 7 columns with zero missing values (`0` nulls) and zero duplicate records (`0` duplicates).
3. **Encoding:** The CSV file was validated in R using `readr::guess_encoding()`, which detected **UTF-8 encoding (confidence = 0.8)** (above `ISO-8859-1` at `0.32` and `ISO-8859-2` at `0.27`), ensuring full support for special characters (such as `ñ` in *Piñata*) across Windows, macOS, and Linux.
4. **Cross-Platform Compatibility (R and Python):** Both `.csv` (`washington_apples.csv`) and `.xlsx` (`washington_apples.xlsx`) formats were tested in R and Python without errors or warnings. In **R**, both formats were imported using `readr::read_csv()` and `readxl::read_excel()`, parsing all 37 rows and 7 character columns (`apple_id`, `variety_name`, `flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, `origin`). In **Python**, both formats were imported via `pandas.read_csv()` and `pandas.read_excel()`, returning `(37, 7)` DataFrames with zero missing values.

## Data Structure

The dataset is provided in `washington_apples.csv` and `washington_apples.xlsx` formats, containing the following variables:

| Variable | Type | Description |
| :--- | :--- | :--- |
| `apple_id` | Character | Alphanumeric identifier for each apple variety record (Format: `WA_APP_001` to `WA_APP_037`). |
| `variety_name` | Character | Official commercial or cultivar name of the Washington apple variety. |
| `flavor_profile` | Character | Primary taste profile classification (`Balanced Sweet-Tart`, `Sweet`, or `Tart`). |
| `crispness_level` | Character | Texture and crunchiness classification (`Crisp`, `Extremely Crisp`, or `Medium`). |
| `skin_color` | Character | Predominant exterior peel coloration (`Bi-color Red/Yellow`, `Red`, `Yellow/Gold`, or `Green`). |
| `harvest_window` | Character | Typical seasonal harvesting period (`Early Season`, `Mid Season`, `Mid-to-Late Season`, or `Late Season`). |
| `origin` | Character | Geographic origin (state/country or country) where the variety originated across 13 distinct origins. |

## Methodology and Quality

1. **Data Source:** Compiled and cross-checked across Washington apple reference sources:
   - [Washington Apples – All Varieties](https://waapple.org/varieties/all/)
   - [WA Grown – Washington's Incredible Long-Lasting Apples](https://www.wagrown.com/blog/apples/item/washingtons-incredible-long-lasting-apples)
   - [Borton Fruit – Apples](https://bortonfruit.com/fruit/apples/)
2. **Critical Data Notes and Caveats:** Column names use `snake_case` for consistent access in R, Python, and SQL, and `apple_id` is stored as a `Character` code (`WA_APP_001` to `WA_APP_037`). The `origin` field reflects where each cultivar was originally developed or discovered (such as *Washington, US*, *New Zealand*, or *Minnesota, US*), rather than solely where it is grown commercially today.
3. **Interoperability:** Both `.csv` and `.xlsx` formats were verified in R and Python without errors. See *Language and Encoding, item 4* for details.

## License

This dataset is distributed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. You are free to share and adapt the material as long as appropriate credit is given.

## Author

**Renzo Caceres Rossi**
* **ORCID:** [0009-0005-0744-854X](https://orcid.org/0009-0005-0744-854X)
* **GitHub:** [washington-apples](https://github.com/lightbluetitan/washington-apples)
