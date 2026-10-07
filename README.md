# Logistics Delivery Analysis — EBAC

**Python • Pandas • Matplotlib • Nested JSON • Operations analytics**

An educational script exploring regional vehicle capacity and delivery data from the EBAC course dataset.

## Problem

How can regional capacity and delivery volumes be organized to support questions about resource allocation in logistics?

## Data

The script reads the public [EBAC deliveries JSON](https://raw.githubusercontent.com/andre-marcos-perez/ebac-course-utils/main/dataset/deliveries.json). It uses the `region`, `vehicle_capacity`, and nested `deliveries` fields.

## Methodology and technologies

1. Load JSON with **Pandas**.
2. Expand nested deliveries using `explode()` and `apply(pd.Series)`.
3. Sum vehicle capacity by region.
4. Calculate delivery counts using the script's current index-based grouping.
5. Display regional bar charts with **Matplotlib**.

## Analysis and current limitations

The script produces regional capacity and delivery-count visualizations, providing a starting point for operations questions. It does not measure route optimization, cost savings, seasonality, or business impact.

**The delivery-count grouping requires validation:** it groups the expanded rows using the original region series, relying on index alignment. Regional labels should be explicitly retained during expansion and the totals reconciled before the delivery-count chart is used for decisions.

The narrative in the script suggests possible business explanations; these are hypotheses, not measured relationships in the current implementation.

## Explore

See [untitled28.py](untitled28.py). Running it requires Python, Pandas, Matplotlib, and internet access to load the JSON. This README documents the current script; it does not change its logic.
