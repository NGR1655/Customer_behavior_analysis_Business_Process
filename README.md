# Business Analysis Documentation Package
### Customer Shopping Behavior Analysis — Retail Customer Retention & Personalization Initiative

This folder contains a full Business Analyst documentation set built from the `customer_shopping_behavior.csv` dataset (3,900 customer transaction records covering demographics, product category, pricing, discounting, subscription status, shipping, payment method, and review ratings).

It simulates a complete BA lifecycle — from requirement gathering through process modeling and gap analysis — as it would be delivered for a retail client seeking to improve customer retention and personalize the shopping experience.

## Key Data Findings Driving This Package
- Only **27%** of customers (1,053 of 3,900) are enrolled in the subscription/loyalty program.
- **100%** of subscribed customers received a discount, but only **28%** of non-subscribed customers did (624 of 2,847) — discounting is applied inconsistently rather than as a deliberate conversion lever.
- **Clothing (44.5%)** and **Accessories (31.8%)** dominate purchases; **Footwear (15.4%)** and **Outerwear (8.3%)** represent cross-sell headroom.
- Average review rating is **3.75/5**; average previous purchases per customer is **~25** — an engaged base that isn't being systematically nurtured.
- Payment method, shipping type, and purchase frequency are each spread evenly across 6–7 options — the opportunity is in personalization/targeting, not logistics.

## Contents

| # | File | Description |
|---|---|---|
| 1 | [01_stakeholder_interviews.md](01_stakeholder_interviews.md) | Simulated stakeholder interviews & requirement-gathering approach |
| 2 | [02_BRD.md](02_BRD.md) | Business Requirements Document — the "what" and "why" |
| 3 | [03_FRD.md](03_FRD.md) | Functional Requirements Document — the "how" at system/feature level |
| 4 | [04_user_stories.md](04_user_stories.md) | Agile user stories with acceptance criteria |
| 5 | [05_use_case_diagram.md](05_use_case_diagram.md) | Use case diagram + actor/use-case descriptions |
| 6 | [06_process_maps_as_is_to_be.md](06_process_maps_as_is_to_be.md) | As-Is vs To-Be process flowcharts |
| 7 | [07_gap_analysis.md](07_gap_analysis.md) | Gap analysis across capability dimensions |
| 8 | [08_swot_analysis.md](08_swot_analysis.md) | SWOT analysis |
| 9 | [09_root_cause_analysis.md](09_root_cause_analysis.md) | Fishbone diagram + Five Whys root-cause analysis |
| — | [diagrams/](diagrams/) | All diagram image assets (PNG) referenced by the docs above |

## Suggested Reading Order
Stakeholder Interviews → BRD → FRD → User Stories → Use Case Diagram → Process Maps → Gap Analysis → SWOT → Root Cause Analysis

## Data Source
`customer_shopping_behavior.csv` — 3,900 rows, 18 columns (Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount, Location, Size, Color, Season, Review Rating, Subscription Status, Shipping Type, Discount Applied, Promo Code Used, Previous Purchases, Payment Method, Frequency of Purchases).

---
*Prepared by: Business Analysis Team · Date: July 29, 2026*
