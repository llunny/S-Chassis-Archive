# Data Pipeline (High-Level)

## Inputs
- OEM EPC/catalog data
- Nissan chassis/option/paint code tables
- Community-verified references

## Steps
1. Parse EPC artifacts into structured records (Python)
2. Standardize code formats and naming
3. Reconcile trim/options across markets and years
4. Aggregate production counts by:
   - grade/trim
   - market
   - option packages
   - paint colour
5. Export datasets (CSV/JSON) for web usage

## Outputs
- VIN decode lookup tables
- Production/rarity datasets
- Option + colour availability matrices
