# Data Sources

This document outlines the reference sources used to compile, validate, and curate the **Washington Apples: A Curated Dataset of Commercial Varieties, Flavor, Crispness, Skin Color, Harvest, and Origins** (`washington_apples.csv` and `washington_apples.xlsx`).

## 1. Primary Sources

The 37 commercial apple varieties (`WA_APP_001` to `WA_APP_037`), along with their variety names, flavor profiles, crispness levels, skin colors, harvest windows, and geographic origins, were compiled and cross-checked across Washington apple reference sources:

* **Washington Apples – All Varieties**
  * **Description:** Official Washington Apple resource listing commercial apple varieties and cultivar characteristics.
  * **URL:** [https://waapple.org/varieties/all/](https://waapple.org/varieties/all/)

* **WA Grown – Washington's Incredible Long-Lasting Apples**
  * **Description:** Reference article covering Washington apple varieties, storage/longevity traits, and commercial profiles.
  * **URL:** [https://www.wagrown.com/blog/apples/item/washingtons-incredible-long-lasting-apples](https://www.wagrown.com/blog/apples/item/washingtons-incredible-long-lasting-apples)

* **Borton Fruit – Apples**
  * **Description:** Commercial orchard and fruit producer catalog providing variety descriptions, flavor/texture attributes, and seasonal availability.
  * **URL:** [https://bortonfruit.com/fruit/apples/](https://bortonfruit.com/fruit/apples/)

### Specific Source Notes

* **Geographic Origin (`origin`):** The `origin` field reflects where each cultivar was originally developed or discovered (covering 13 distinct origins, such as *Washington, US*, *New Zealand*, *Minnesota, US*, *Australia*, *Japan*, and European/North American origins), rather than solely where it is grown commercially today.
* **Completeness and Formatting:** All 37 records and 7 columns (`apple_id`, `variety_name`, `flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, `origin`) are populated with zero missing values and zero duplicate records, preserving cultivar names such as *Piñata* in UTF-8 encoding.

## 2. Access Date

All sources were consulted and validated during **November 2026** (release `1.0.0` dated **2026-11-20**).

## 3. Citation of Sources

When using this dataset, users are encouraged to acknowledge both this curated version and the reference sources:

> *Data compiled and cross-checked against Washington apple reference sources (Washington Apples, WA Grown, and Borton Fruit), curated and standardized by Renzo Caceres Rossi.*

For academic purposes, please cite this curated version using the DOI and metadata provided in the `CITATION.cff` file included in this repository.