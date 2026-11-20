# Limitations

This document outlines the known limitations of the **Washington Apples: A Curated Dataset of Commercial Varieties, Flavor, Crispness, Skin Color, Harvest, and Origins** (`washington_apples.csv` and `washington_apples.xlsx`) to ensure its proper use in research and development.

## 1. Scope of Coverage

This dataset is strictly limited to a **curated reference table of 37 commercial apple varieties** (`WA_APP_001` to `WA_APP_037` across 13 distinct origins) and the seven variables defined in its schema (`apple_id`, `variety_name`, `flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, and `origin`).
* It does NOT include quantitative sensory measurements (such as Brix/sugar levels, titratable acidity, or firmness in pounds/kilograms), orchard acreage or production volume statistics, storage shelf-life metrics, or pricing data.
* Users requiring agronomic yield figures, laboratory sensory assays, or commercial production volumes should consult specialized horticultural databases and producer reports.

## 2. Categorical Classifications and Origin Semantics

Categorical attributes (`flavor_profile`, `crispness_level`, `skin_color`, `harvest_window`, and `origin`) are represented as discrete labels suitable for exploratory analysis, teaching, and classification workflows, rather than continuous or multi-dimensional measurements.
* **Qualitative categories:** Attributes such as *flavor_profile* (`Balanced Sweet-Tart`, `Sweet`, `Tart`), *crispness_level* (`Crisp`, `Extremely Crisp`, `Medium`), *skin_color* (`Bi-color Red/Yellow`, `Red`, `Yellow/Gold`, `Green`), and *harvest_window* (`Early Season`, `Mid Season`, `Mid-to-Late Season`, `Late Season`) reflect high-level groupings rather than fine-grained sensory scales or exact harvest dates.
* **Origin vs. commercial production location:** The `origin` variable documents where each cultivar was originally developed or discovered (e.g., *Washington, US*, *New Zealand*, *Minnesota, US*, *Australia*, *Japan*, and other recorded origins), which may differ from where the variety is grown commercially or harvested in a given season.

## 3. Temporal Snapshot

The dataset reflects a curated snapshot compiled and validated for release `1.0.0` (**2026-11-20**) based on Washington apple reference sources.
* Any subsequent updates, newly introduced commercial cultivars, or updated cultivar classifications will be addressed in future versioned releases following Semantic Versioning conventions.

## 4. Language and Orthographic Conventions

Both variable names (using `snake_case`) and categorical values are standardized in English, while preserving cultivar naming conventions and diacritics such as *Piñata* in UTF-8 encoding.
* Users working in Spanish or other languages who need localized category labels or cultivar notes will need to apply their own translation or mapping layer.

## 5. Non-Official Status

Although this dataset was compiled and cross-checked against Washington apple reference sources (*Washington Apples*, *WA Grown*, and *Borton Fruit*), this curated version is maintained by an **independent researcher**.
* It should be treated as a curated technical standardization for research and educational purposes, and not as an official publication of any state agricultural agency, grower association, or commercial orchard.