---
sidebar_position: 1
---

# Data Collection Guidelines

This document outlines general principles, sources, procedures and quality control requirements for data collection.

## Data Collection Process

### Data Sources

Data can be collected from the following types of public literature and materials:

- **Research Papers**: Journal articles, conference papers (recommended platforms: Elsevier, Springer, ACS, CNKI, Google Scholar)
- **Engineering Manuals**: Such as "Chemical Engineering Design Manual", "Chemical Process Manuals"
- **Corporate Environmental Impact Reports**: Including EIA reports, feasibility studies, cleaner production audit reports
- **Government & Industry Publications**: Statistical yearbooks, industry standards, energy statistics, industry development bluebooks
- **Patents & Standards**: National/industry standards, patent databases (e.g., CNIPA, WIPO)
- **Field Survey Data**: Actual measurement data from factories, enterprises or research institutions

Data collection must follow two fundamental principles:

- Each data point must be **fully traceable**, with source clearly documented (literature/report/database)
- All entered information should be **complete and detailed** to ensure data quality and reproducibility

### Process Flow Analysis

Before data collection begins, identify the unit process-level industry flow diagram.

### Literature Search & Selection

Use keywords to search data on platforms like CNKI, WoS, Scopus and Google Scholar. Recommended keyword combinations:

- "Methanol life cycle assessment"
- "Inventory analysis"
- "Environmental impact" etc.

Prioritize original or high-quality studies with clear input-output data and system boundaries.

### Collection Content

Main data categories to collect:

- Material inputs (raw materials, water, additives)
- Energy consumption (electricity, fuels)
- Product & byproduct outputs (methanol, byproduct gases, waste heat)
- Emission data (CO₂, NOₓ, wastewater, solid waste)

## Data Processing

### Unit Standardization & Conversion

Convert units from different sources to standard units to ensure consistency and reusability in the database. Examples:

- Energy conversion: kcal → MJ
- Volume-mass conversion: Nm³ → kg (based on density or standard conditions)

> Important Note:
When required units differ from existing flow units, perform **unit conversion** rather than creating new Flow items.

### Missing Value Handling

Available strategies:

- Average values from similar processes
- Typical values from LCA databases
- Engineering estimates (e.g., heat balance, material balance)
- Clearly document assumptions or uncertainty ranges

### Special Notes & Remarks

For lifecycle modeling, document the following in remark fields to ensure standardized dataset structure, clear system boundaries and transparent data processing:

- **UUID Conflict Notes**: Input/output should not contain duplicate flow items (platform distinguishes by UUID). If literature shows same substance in different forms/phases, merge into single flow item and document rationale.

- **Internal Recycling Notes**: For flows like steam that are internally recycled without additional environmental burden, note: "Internal platform recycling flow, not counted as output emissions".

- **Excluded Emission Notes**: For items like catalyst loss that involve material flow but are contained within system, note: "Catalyst operates in closed loop, not included in material balance output".

- **Estimation/Completion Notes**: For items completed based on material balance or engineering experience (e.g., wastewater, exhaust), note: "Estimated based on material balance, original data not provided in literature".
